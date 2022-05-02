pipeline {
    agent any
    stages {
        stage ('Build Backend') {
            steps {
                bat 'mvn clean package -DskipTests=True'
            }
        }
        stage ('Unit Tests') {
            steps {
                bat 'mvn test'
            }
        }
        stage ('Horusec') {
            steps {
               bat 'horusec start -p . -e true'
            }
        }
        stage ('Sonar Analysis') {
            environment {
                scannerHome = tool 'Sonar_Scanner'
            }
            steps {
                withSonarQubeEnv('SonarQuobe') {
                    bat "${scannerHome}/bin/sonar-scanner -e -Dsonar.projectKey=DeployBack2 -Dsonar.host.url=http://127.0.0.1:9000 -Dsonar.login=4977107a5c5ac7d9cabb5cc3de977a3c24212975 -Dsonar.java.binaries=target -Dsonar.coverage.exclusions=**/.mvn/**,**/src/test/**,**/model/**,**Application.java"
                }
            }
        }
        stage ('Check Container Vulns') {
            steps {
                bat 'docker run --rm aquasec/trivy image tomcat:8.5.50-jdk8'
            }
        }
        stage ('Deploy App') {
            steps {
                bat "curl -v -u admin:210794 -T target/tasks-backend.war 'http://127.0.0.1:8001/manager/text/deploy?path=/tasks-backend&update=true'"
            }
        }
    }
}


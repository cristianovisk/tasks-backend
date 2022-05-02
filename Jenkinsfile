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
               bat 'horusec start -p . -e true -R ", 2115236bb76f58babc84f6fc726ac0c185e07cdf18bc9a23f6a42346520f21d2, b9c78fe9e521f577e9dc20079f9aedd510e508a9ae97db720fc94cd2573a9fd5, 5c00a30022eb5ff772ab658d931504baf0136debb471318c8eeab00df404cc06, 11c10384d99b16d50cef714abe41210735492ddab0dfff51417501ebf95f4f0b, 32feff67323e26c8203cd94f26f2105f014290bf059cd5fd15b67b663c1ffbb7, a7906de5bf59f3688aa7ab1e6210b351e32d9086d576e8007a4d12e4883f6cd4, d414b2e169d13ce66aa33a4340386f2c6b49e1b927e94b624304d19cd43311a5, 814b0ecf2874858df1850368a9d7cb71b77829731330b9cf21430c17199ac142, a615a8d54517bdae0328407974cf1c08671cfc4a2015b2eccc89c0a199a83db2, 1ae5af1d0bf20dd3553d16c650da83cee308ed90d1af0987468842288841102c, 70c3c871f971cb468a437c25ba11ef290951393e96b6f0fd96e46040ba575643, 8aeaa22f28593467adc955cca8950d8b086f6446f0adb9a40c210a7ec47096bc, ed26a776fdfcfd74ed03cdc459e03b67a7cff98de71b7fe607843aa08f4c4c4b, 9070445e328856ec02516f378f46973ae1649f3623ee086892d56336b68dd4e9, 8aa3d6eb1fe1decb2413b493d636d90554e6b327fc0ff33e310c563fe406ad80, d1fd6a3e8a853fe3ed5e08d135cdc37a68e2faf51fdc65d8bc9a4363ab3b1b49, b3264284ddc0eff9fe2d7e8a71310e9fd190d0459cfb0246601fc81b0c3421cd, 51b4db012ebe89ea6fdd194215bf034ae6cf502a282cc313d798773bb0777b13, 2f492bc71ab9bda437299742c137e678376370cc25a78a463352f0b177a2dcd4, 210ca4af125df93eda75b1eafc90dc6eb6dd5329f1477101c777864d2805e76c, fa85b17fd329ba78e75a269f5b8fa35261c9fbfb3956c5deee50af64d20193dc, 60fee7d70e7a30f7c546f134a5bacbc66a00d65154049c73b5f66df14b81a6cd, 02c421f88848bee5470165891989e901669641133ff4d6078a3d018a1d8e741d, 9ef5bece4c608872ff83ab9f54ef91c9e75d5cb45faa4b06da861101fd048665, ed99cb83cc340bd1cc0a7d547d105e76777f2158e6e4d0d066c37c1d542b4c77, d3101afdbd50ab839ddabcc86da6ae1e1b586ac1c987a6040b730537f071554a, 93347c70202d9e9d2ba3097f8275c255319b0bb5ca818eecc809a8fd484d79ab, 6470c854f8e8bf42215e01f18234b912f147899ababd7a72171ee1da9cc37e20, 42834a26726c381f375e6c722c4fdd9588354e1b19a2ee7bcab5772c82a42d80, f624335adf7b8843ddad2440bfedf9f8a959a8e0c3537d534d304435da9549a7, aef1c1104f0039ff9eed0d9b29764af7be5cd86188a6fed8a23df4ede1a30749, 0504eb77bcfd46d7c9c20352dda4dca3328fff4b3682a1b3e3090b76b6815101, 42ef7a3c478550fcca2eb0a1367b01ecc976c1e7192fbbeb7a574be094202eb9, d832ed2e7e6ae04fa52292abd1629ffdda495ca2ac56108f04ccdfcb8c3a1231, 078f69d26d37f6de46f4767d92eca98fe1f697d87c0918caabd5d055fc8a47c2, fe76b6e64da0fdbed5941db3ef59f4913175ed84caaccd8c1a57861251702b16, a9a98dd82b141d0cf1eb5210ab44237dcb6b9ad4ca90808f2bc31af5e4627ca4, a34fcbf5a13dba57ecb953c962b9a736b587164f2726d2a24b559335e7c88671, d5d0d98633ba60cb3ecaa785f192a025babe9a3c87982defcd7b60fbda11f838, af8b01c863e51a95f70cfd7593a3b89d865a53cc53be7959125f4ffd2e44b239, 73fbde7a475a98492f88ff805d8f0ecb2ae6523a438127fca27a0f54166d802a, 4d3ba6a36013a48c52eef53991f75f924982013ebf5c1be1ff23f1a2ba5a87a2, 4f682f2714eeb33beb9fd52468532755093cc9c6e4e6d549290c2beedda5a34a, 110f72ed05b6451853be77805e0b2ae4a736f4376cf97e2e5bb21f28f910b0df, 8f94f09e4530f2bde29ea0b5d90b14c78c85c464928eb729b9db024337d1b172, 18022fe046203a690b7a1d0f075f46d9a5c01acaa8216398144a302cbc6be012, 360d198025ccac6789ffd39ddcf8aa613a3cd8f8c236a710ccafe188780bc1e6, ee7dfeaed1f005b8148a584c74663156d6f15690de084cc70cb07b20582a90a5, 4382bfd1ba855ceea04bd9b9ff26dd40b8f442bb7c517fbceda187b0ca1d4b8f, 0ea2745bcd38a84967612fac681c17b6d473879ad2600c51c5cbcbbc12b47fd4, bb51e9566aee31d4360de7663b3f09cd7d51af9e60b6066d2f012b4b781d1b66, 5e7c26aa4da8bf18bcad9b71a261166977bc363844e7c07d8c7bc3ab4db5f2f2, 230c6a4861fae9d73271a08b116f1d61c7b56ca7c5c5b32fd660e2453676de80, 7f5e54dbc21a7cfdb16c552b147e4d04866364ba3f24c2181976afff9d3a197d, 28eeb771578555a23dbbd3854ce1db451e1222284f3389882bc4c4c40364f971, f393229f397e82698d6e085bbe6b007f91b0e8be658d55c7c8339955083b874f, 2a94e249e4619788a1e7e7fd1536021a914255efc4b26ecbc800ff2c024c0cd2, 7dea02d16a4c3e2a153f173b568fd46c6296f651be4f78c5fe4d19e57745885f, b003226020cb3874314c0cc878a4aaf3a9782c76f16f0259f5aa0e76a38a297f, f5cb5c852c1eaf134acf4cfbdd727b38c5a87676623242b6be3bbb1a290a2144, 090f4a34e3ce96d26a705bc417a3cf6899017a4369ff9716d178606957f17faa, da2cc3a5ee5b9fcce404c311b9e573d22d851021e857d3eff819f6dc6c5f5851, 81a2f33e3005cf1cec1ce4e74ca183d4939670d3157a2e4797413dbab8e05208, 2504346190bfdc3537b0aa6da877eac462bd990fab2bad93f0a876f0bff7d81a, 0f938b24f7cbcee55c3cce15f2c95a8b2764bbeb115226b8d242da1c56491545, 8c4561a1867a9f8e63ba6270f6441ba9431e71fb3b11c629ef55501c66d08a0d, 3a39ef5a254e05ec3ef736d294fbd608eb865278b71e5882b317d173a92c4623"'
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


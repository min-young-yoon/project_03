pipeline {

    
    
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/roundlifemin/project_03.git'
            }
       }



           stage('Build') {
            steps {
                script {
                    // Docker 이미지 빌드
                    sh 'docker build  -f ./Dockerfile -t roundlifemin/project_03:latest .'
                }
            }
        }



          }
      }

      stage('Cleaning up') { 
		  steps { 
              sh 'docker rmi  roundlifemin/project03:latest' // docker image 제거
          }
      } 


    }
}


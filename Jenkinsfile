pipeline {
    agent any
    stages{
        stage('build project'){
            steps{
                git url:'https://github.com/gayathriinanda/Banking-and-Finance-/', branch: "master"
                sh 'mvn clean package'
              
            }
        }
        stage('Build docker image'){
            steps{
                script{
                    sh 'docker build -t gayathri/staragileprojectfinance:v1 .'
                    sh 'docker images'
                }
            }
        }
         
        
     stage('Deploy') {
            steps {
                sh 'sudo docker run -itd --name My-first-containe21211 -p 8083:8081 gayathri/staragileprojectfinance:v1'
                  
                }
            }
        
    }
}

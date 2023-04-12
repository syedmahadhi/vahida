pipeline {
    agent any
     stages {
       stage ('checkout') {
         steps{
             sh'echo hi'
        //checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '4f6546d3-c9b1-4141-ba87-3e14710582a5', url: 'https://github.com/syedmahadhi/vahida.git']])
          //checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '4f6546d3-c9b1-4141-ba87-3e14710582a5', url: 'https://github.com/syedmahadhi/vahida.git']])   
         }
       }
      
        
       stage('clone'){
            steps{
             sh 'git clone https://github.com/syedmahadhi/vahida.git'
             echo 'cloning phase'
             sh 'cd vahida'
            }
         }

       stage('run python'){
        steps{
         sh 'python3 main.py'
       echo 'python program running phase'
        }
       }
    }
   // cleanWs()
}
 

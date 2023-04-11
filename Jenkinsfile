pipeline {
    agent any
     stages {
       stage ('checkout') {
         steps{
           git credentialsId: 'edc0a7ea-802c-46e8-983c-4d2714ede055', url: 'http://192.168.1.236/vahidaAnju/DevOpsTest.git'
         }
       }
        
       stage('clone'){
            steps{
             sh 'git clone '
             echo 'cloning phase'
            }
         }

         stage ('cleanWS'){
           steps {
             sh 'rm -r * /var/lib/jenkins/workspace/'
           }
         }
      
         stage('pull'){
            steps{
              sh 'git pull origin master'
                echo 'pull phase'
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
 

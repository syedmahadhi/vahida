pipeline {
    agent any
    stages {
      stage('clone'){
            steps{
             sh 'git clone https://github.com/syedmahadhi/vahida.git'
             echo 'cloning phase'
             sh 'cd vahida'
            }
         }
       stage ('unset proxy') {
           steps {
       // sh 'git config --global --unset http.proxy'
          sh 'git config --global user.name "syedmahadhi"'
          sh 'git config --global user.email "syedmahadhi.n@ciyes.com"'
         }
      }
      
      stage ('cleanWS'){
       steps {
           sh 'cd /var/lib/jenkins/workspace' 
           sh 'rm -r *'
          }
        }
       stage('run python'){
       steps{
         sh 'python3 main.py'
         echo 'python program running phase'
          }
         }
       
    }
}
 

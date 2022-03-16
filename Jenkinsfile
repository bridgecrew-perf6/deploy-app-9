
pipeline {
    agent any
   
               
       stages {
            stage('SCM checkout') {
                  steps {
                        git url: 'https://github.com/testproject654/deploy-app.git'
                        }
             }
             
             stage('archiving artifacts') {
                  steps {
                          archiveArtifacts '**/*.html'
                        }
              }
           
           stage('test') {
                  steps {
                          sh 'whoami'
                          sh 'ls -a'
                         
                        }
              }
           
           stage('upload to server') {
                  steps {
                          sh 'cp index.html /var/www/html'
                        }
              }
             
       }
}

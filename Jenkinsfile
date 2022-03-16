// This is a pipeline for Jenkins (launched on aws ec2 ubuntu instance) to fetch php code from Github and then transfer it to the
// Apache2 /var/www/html directory (deployment)onto the another aws ec2 ubuntu instance.



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

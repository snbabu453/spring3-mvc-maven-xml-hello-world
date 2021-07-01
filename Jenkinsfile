pipeline {
    agent any

    stages{
        stage('Cleaning the code'){
            steps{
             sh 'mvn clean'
            }
           
        }
           stage('Testing the code'){
               steps{
                sh 'mvn test'
               }
            
        }
          stage('Building package the code'){
              steps{
                  sh 'mvn package'
              }
           
        }
        stage(){
            steps{
            sshagent(['tomcatidnew']) {
             sh """
                        scp -o StrictHostKeyChecking=no **/*.war  ubuntu@172.31.19.206:/opt/tomcat/apache-tomcat-9.0.48/webapps
            """
            }

        }
    }

}
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
    }

}
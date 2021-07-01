pipeline {
    agent any

    stages{
        stage('Cleaning the code'){
            sh 'mvn clean'
        }
           stage('Testing the code'){
            sh 'mvn test'
        }
          stage('Building package the code'){
            sh 'mvn package'
        }
    }

}
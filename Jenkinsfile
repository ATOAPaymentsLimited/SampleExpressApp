pipeline {
   
    agent any

    stages {

        stage('Clone repository') { 
            steps { 
                script{
                checkout scm
                }
            }
        }
        stage('Build') {
            steps {
                sh 'pwd'
                sh 'ls -la'
                sh 'npm install'
            }

        }

        stage('Docker Image Build') {
            steps {
                sh 'docker build -t test-ecr .'
            }
        }
        
    }
}

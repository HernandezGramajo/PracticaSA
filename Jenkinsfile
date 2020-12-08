pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                sh 'npm install' 
                
            }
        }
        stage('Test') {
            steps {
                sh 'npm run ng test --code-coverage --watch=false' 
               
            }
        }
        stage('Build') {
            steps {
                sh 'ng build --optimization' 
                
            }
        }
        stage('Deploy') {
            steps {
                sh 'mv dist/practicaSA/* /var/www/html' 
                
            }
        }
    }
}
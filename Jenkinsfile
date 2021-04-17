
pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        HOME = '.'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'test stage'
            }
        }
        stage('Deliver') {
            steps {
                echo 'deliver stage'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                echo 'kill stage'
            }
        }
    }
}
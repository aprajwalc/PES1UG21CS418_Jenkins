pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
               git branch: 'main',
               url: 'https://github.com/aprajwalc/PES1UG21CS418_Jenkins.git'  // Replace with your Git repository URL
            }
        }
        stage('Build') {
            steps {
                build 'PES1UG21CS418-1'
                sh 'g++ maincode.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}

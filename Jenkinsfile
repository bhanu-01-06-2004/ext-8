pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                script {
                    echo 'Cloning repository...'
                    git branch: 'main', url: 'https://github.com/your-username/external1.git'
                }
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    echo 'Building Docker image...'
                    sh 'docker build -t my-nodejs-appp-csed .'
                }
            }
        }
        stage('Run Tests') {
            steps {
                script {
                    echo 'Running tests...'
                    // Add test commands if available
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying application...'
                    sh 'docker run -d -p 8081:3000 my-nodejs-appp-csed'
                }
            }
        }
        stage('Release') {
            steps {
                script {
                    echo 'Releasing application...'
                    // Add release logic here
                }
            }
        }
    }
}

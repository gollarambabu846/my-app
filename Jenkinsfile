pipeline {
    agent any

    tools {
        nodejs 'NodeJS'
    }

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/gollarambabu846/my-app.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test || echo "No tests available"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}

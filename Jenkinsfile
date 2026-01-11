pipeline {
    agent any

    tools {
        nodejs 'NodeJS'
    }

    stages {

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run App') {
            steps {
                sh '''
                 pm2 delete my-app || true
                 pm2 start app.js --name my-app
                 '''
            }
        }
    }
}

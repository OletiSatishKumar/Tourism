
pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning the code...'
                git branch: 'main',
                    url: 'https://github.com/OletiSatishKumar/Tourism.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'npm run test'
            }
        }
    }
}

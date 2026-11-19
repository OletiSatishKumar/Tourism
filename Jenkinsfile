
pipeline {
    agent any

    tools {
        nodejs 'NodeJS-22'
    }

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning repository...'
                git branch: 'main',
                    url: 'https://github.com/OletiSatishKumar/Tourism.git'
            }
        }

        stage('Check Node') {
            steps {
                sh 'node --version'
                sh 'npm --version'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm run test'
            }
        }
    }
}

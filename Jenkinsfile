pipeline {
    agent any
    environment {
        PATH = "/opt/homebrew/bin:${env.PATH}"
    }
    stages {
        stage('Clone') {
            steps {
                git branch: 'main',      // ✅ Fixed
                url: 'https://github.com/MadsVS45/ci-node-app.git'
            }
        }
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run App') {
            steps {
                sh 'node app.js'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }
}
pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git branch: 'main',      // ✅ Fixed
                url: 'https://github.com/MadsVS45/ci-node-app.git'
            }
        }
        stage('Install') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run App') {
            steps {
                bat 'node app.js'
            }
        }
        stage('Test') {
            steps {
                bat 'npm test'
            }
        }
    }
}
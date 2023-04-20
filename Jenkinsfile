pipeline {
    agent any
    stages {
        stage('change directory and present working directory') {
            steps {
                sh 'cd /var/lib/jenkins/workspace'
                sh 'git clone https://github.com/agarwalraghav1212/magic-cursor.git'
                sh 'cd ./magic-cursor'
                sh 'pwd'
            }
        }
        stage('install required dependencies') {
            steps {
                sh 'npm audit fix --force'
                sh 'npm install'
            }
        }
        stage('deploy') {
            steps {
                sh 'npm start server.js'
            }
        }
        stage('show'){
            steps{
                sh 'npm list'
            }
        }    
    }
}

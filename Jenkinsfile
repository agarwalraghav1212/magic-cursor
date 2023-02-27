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
                sh 'npm i'
            }
        }
        stage('deploy') {
            steps {
                sh 'pm2 start server.js'
            }
        }
    }
}

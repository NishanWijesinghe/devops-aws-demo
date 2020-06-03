pipeline {
    agent any
    stages {
        stage('install dependencies') {
            steps {
                sh 'python3 -m venv venv'
                sh '. venv/bin/activate'
                sh 'make install'
            }
        }
        stage('run tests') {
            steps {
                sh '. venv/bin/activate'
                sh 'make test'
            }
        }
        stage('run lint') {
            steps {
                sh '. venv/bin/activate'
                sh 'make lint'
            }
        }
    }
}
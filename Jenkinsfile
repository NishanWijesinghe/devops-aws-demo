pipeline {
    agent any
    stages {
        stage('install dependencies') {
            steps {
                sh 'python3 -m venv venv'
                sh '. venv/bin/activate && make install'
            }
        }
        stage('run tests') {
            steps {
                sh '. venv/bin/activate && make test'
            }
        }
        stage('run lint') {
            steps {
                sh '. venv/bin/activate && make lint'
            }
        }
    }
}
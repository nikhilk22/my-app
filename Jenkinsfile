pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/nikhilk22/my-app.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'pytest'
            }
        }
        stage('Package') {
            steps {
                sh 'zip -r my-app.zip .'
            }
        }
    }
}

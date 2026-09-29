pipeline {
    agent any

    stages {

        stage('SCM Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'python test.py'
            }
        }

        stage('Run Flask App') {
            steps {
                bat 'start /B python app.py'
            }
        }
    }
}

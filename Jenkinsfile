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
                bat '"C:\\src\\windows junkins\\venv\\Scripts\\python.exe" --version'
                bat '"C:\\src\\windows junkins\\venv\\Scripts\\python.exe" -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat '"C:\\src\\windows junkins\\venv\\Scripts\\python.exe" test.py'
            }
        }

        stage('Run Flask App') {
            steps {
                bat 'start /B "" "C:\\src\\windows junkins\\venv\\Scripts\\python.exe" app.py'
            }
        }
    }
}

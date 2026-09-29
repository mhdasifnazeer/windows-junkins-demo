pipeline {
    agent any

    stages {

        stage('SCM Checkout') {
            steps {
                checkout scm
            }
        }

        
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

pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                call npm install
            }
        }
        stage('Test') {
            steps {
                call test.sh
            }
        }
        stage('Deliver') {
            steps {
                call deliver.sh
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                call kill.sh
            }
        }
    }
}

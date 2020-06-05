pipeline {
    agent any
    environment {
        CI = 'true'
        PATH = "C:\\WINDOWS\\SYSTEM32"
    }
    stages {
        stage('Build') {
            steps {
                bat label: '', script: 'call index.html'     
            }
        }
       
    }
}

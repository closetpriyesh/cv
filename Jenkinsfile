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
        
         stage('Test') {
            steps {
                bat label: '', script: 'call test.sh' 
            }
        }
        stage('Deliver') {
            steps {
                bat label: '', script: 'call deliver.sh' 
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                bat label: '', script: 'call kill.sh' 
            }
        }
       
    }
}

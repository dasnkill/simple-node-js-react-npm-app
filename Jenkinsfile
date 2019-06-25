pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3008' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    
        stage('test') { 
            steps {
                sh 'jenkins/scripts/test.sh' 


        stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'FinalizadO (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
        }
            }
        }
    }



}

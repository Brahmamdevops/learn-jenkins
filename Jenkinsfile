pipeline {
    agent {
        node {
            label 'AGENT-1'
            
        }
    }
    
     environment { 
        GREETING = 'Hello Jenkins'
    }

    options {
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
    }
    stages {
        stage('Build') {
            steps {
                echo 'Buildings.'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
                echo "$GREETING"
                // echo "$env"
            }
        }
    }
}
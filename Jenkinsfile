pipeline {
    agent none

    stages {
        stage('Build') {
            agent { label 'slave01' }
            steps {
                echo 'Building..'
                sh '''
                   cd /home/ubuntu/
                   pwd
                   cd /etc/ansible/
                   pwd
                   ansible node -m ping
                '''
            }
        }
    }
} 

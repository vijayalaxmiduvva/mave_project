pipeline {
    agent none

    stages {
        stage('Build') {
            agent { label 'slave' }
            steps {
                echo 'Building..'
                sh '''
                   cd /home/ubuntu/
                   pwd
                   cd /etc/ansible/
                   pwd
                   ansible node -m ping
                   cd /etc/ansible/playbook/  
                   ansible-playbook deploy.yaml
                '''
            }
        }
    }
} 

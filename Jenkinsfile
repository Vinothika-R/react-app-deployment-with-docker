pipeline {
    agent any

    stages {
        stage('Check Jenkins Docker Access') {
            steps {
                sh '''
                    echo "Checking Jenkins user and Docker access..."
                    whoami
                    docker ps
                '''
            }
        }

        stage('Changing file permission') {
            steps {
                sh 'chmod +x build.sh'
            }
        }

        stage('Executing the file') {
            steps {
                sh './build.sh'
            }
        }
    }
}


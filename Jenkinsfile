pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/KolyCamara/TP-Jenkins-Security.git'
            }
        }

        stage('Install Python & Dependencies') {
            steps {
                sh '''
                apt update
                apt install -y python3 python3-pip
                pip3 install -r requirements.txt
                '''
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest'
            }
        }
    }
}
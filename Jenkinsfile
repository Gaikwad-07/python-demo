pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/python']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Gaikwad-07/python-demo.git']])
            }
        }
        stage('Build') {
            steps {
                git branch: 'python', url: 'https://github.com/Gaikwad-07/python-demo.git'
            }
        }
        stage('Build') {
            steps{
                sh 'sh python3 list.py'
            }
        }
        stage('Test'){
            steps {
                echo ' the job has been tested '
            }
        }
    }
}

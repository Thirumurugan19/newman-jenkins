pipeline {
    agent { label 'LinuxSlave' }
    stages {
        stage ('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Test'){
            steps {
                sh 'npm install'
                sh 'npm run serverless-api-test'
                junit 'newman.xml'
            }
        }
    }
}

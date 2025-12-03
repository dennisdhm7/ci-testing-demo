pipeline {
    agent any

    stages {

        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test -- --coverage'
            }
        }

        stage('Archive Coverage') {
            steps {
                archiveArtifacts artifacts: 'coverage/**'
            }
        }
    }
}
pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                echo "Building Docker Image..."
                sh 'docker build -t java-demo .'
            }
        }

        stage('Run Container') {
            steps {
                echo "Running Container..."
                sh 'docker run --rm java-demo'
            }
        }
    }

    post {
        success {
            echo "Build SUCCESS"
        }
        failure {
            echo "Build FAILED"
        }
    }
}

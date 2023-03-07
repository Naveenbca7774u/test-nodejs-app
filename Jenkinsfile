pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building..."'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing..."'
            }
        }
        stage('Deploy') {
            parallel {
                stage('Deploy to Staging') {
                    steps {
                        sh 'echo "Deploying to staging..."'
                    }
                }
                stage('Deploy to Production') {
                    steps {
                        sh 'echo "Deploying to production..."'
                    }
                }
            }
        }
    }
    post {
        always {
            sh 'echo "Pipeline complete"'
        }
    }
}

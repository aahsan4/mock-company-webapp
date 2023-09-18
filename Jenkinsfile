pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // TODO: Add build step
                sh './gradlew assemble'
            }
        }

        stage('Test') {
            steps {
                // TODO: Add test step
                sh './gradlew test'
            }
        }
    }

    post {
        failure {
            // Add a post-build step to handle failures
            script {
                withCredentials([[$class: 'GitHubAppCredentials', credentialsId: 'Aninda Ahsan', owner: 'aahsan4', appid: 'Papio Pipelines']]) {
                    // You can use the GitHub App Credentials here
                    echo "Failed: Check the build logs for details."
                }
            }
        }
    }
}

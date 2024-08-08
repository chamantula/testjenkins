pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from GitHub repository using the specified credentials
                git credentialsId: 'harish', url: 'https://github.com/chamantula/testjenkins.git'
            }
        }

        stage('Build Client') {
            steps {
                    script {
                        // Copy the .env file into the build context and build the Docker image
                        sh 'cd testjenkins'
                        sh 'chmod +x harish.sh'
                        sh './harish.sh'
                      
                    }
            }
        }
    }
}

pipeline {
    agent { label 'worker1' }

    environment {
        // Define the environment variables for GIT_BRANCH and GIT_COMMIT
        GIT_BRANCH = ''
        GIT_COMMIT = ''
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout the latest code from the repository
                    checkout scm
                    
                    // Get the current GIT_BRANCH and GIT_COMMIT
                    GIT_BRANCH = env.GIT_BRANCH
                    GIT_COMMIT = env.GIT_COMMIT
                }
            }
        }

        stage('Print GIT Information') {
            steps {
                script {
                    // Print the branch and commit information
                    echo "Current GIT_BRANCH: ${GIT_BRANCH}"
                    echo "Current GIT_COMMIT: ${GIT_COMMIT}"
                }
            }
        }
    }
}

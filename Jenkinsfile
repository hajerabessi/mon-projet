pipeline {
    agent any

    environment {
        GIT_REPO_URL = 'https://github.com/hajerabessi/mon-projet.git' // Replace with your Git repo URL
        GIT_BRANCH = 'master' // Replace with your desired branch
    }

    stages {
        stage('Clone Repository') {
            steps {
                script {
                    // Checkout the code from the Git repository
                    git url: "${GIT_REPO_URL}", branch: "${GIT_BRANCH}"
                }
            }
        }

        stage('Show Status') {
            steps {
                script {
                    // Show Git status to verify successful checkout
                    sh 'git status'
                }
            }
        }
    }

    post {
        success {
            echo 'Successfully cloned the repository!'
        }

        failure {
            echo 'Failed to clone the repository.'
        }
    }
}


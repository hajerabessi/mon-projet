pipeline {
    agent any

    environment {
        GIT_REPO_URL = 'https://github.com/hajerabessi/mon-projet.git'
        GIT_BRANCH = 'master' 
    }

    stages {
        stage('Clone Repository') {
            steps {
                script {
                   
                    ggit(
                        url: 'https://github.com/hajerabessi/mon-projet.git',
                        branch: 'master', 
                        credentialsId: 'github-credentials' 
                    )
                }
            }
        }

        stage('Show Status') {
            steps {
                script {
                    
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


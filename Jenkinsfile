pipeline {
    agent any

    environment {
        GIT_REPO_URL = 'https://github.com/hajerabessi/mon-projet.git' 
        GIT_BRANCH = 'master' 
        GIT_CREDENTIALS_ID = 'github-credentials' 
    }

    stages {
        stage('Cloner le dépôt') {
            steps {
                script {
                    
                    git url: "${GIT_REPO_URL}", branch: "${GIT_BRANCH}", credentialsId: "${GIT_CREDENTIALS_ID}"
                }
            }
        }

     
}
}

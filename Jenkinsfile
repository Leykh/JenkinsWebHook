pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Etape de build github"
                sh 'npm install'
            }
        }
        stage('Tests') {
            steps {
                echo "Etape de test github"
                sh './scripts/test.sh'
            }
        }
        stage ('Deploy') {
            steps {
                echo "Etape de déploiement github"
                sh './scripts/deploy.sh' 
                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
                sh './scripts/kill.sh' 
            }
        }
    }
}
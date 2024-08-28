pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Etape de build github"
                sh 'chmod +x npm install'
            }
        }
        stage('Tests') {
            steps {
                echo "Etape de test github"
                sh "chmod +x -R ${env.WORKSPACE}"
                sh ' ./scripts/test.sh'
            }
        }
        stage ('Deploy') {
            steps {
                echo "Etape de déploiement github"
                /*sh './jenkins/scripts/deliver.sh' 
                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
                sh './jenkins/scripts/kill.sh'*/ 
            }
        }
    }
}
pipeline{
    agent any

    stages {
        stage ("checkout"){
            steps{
                checkout scm
            }
        }

        stage ("Test"){
            steps{
                sh 'sudo apt install npn'
                sh 'npm test'
            }
        }

        stage ("Build"){
            steps{
                sh 'npm run build'
            }
        }

        stage ("Build image") {
            sh 'docker build -t cart .'
        }
    }
}
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
              echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

    post
    {
        always
        {
            emailext attachLog: true, body: 'Your pipeline build was successful. ', subject: 'Pipeline Status Report', to: 'dhirajmankar1210@gmail.com'
        }
    }
}
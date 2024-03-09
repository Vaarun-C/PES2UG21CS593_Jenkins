pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Compiling the CPP file'
                    sh 'g++ -o output PES2UG21CS593.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'The output of the CPP file is: '
                    sh './out'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deployment steps'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}

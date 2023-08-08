pipeline {
    agent any 
    environment {
        NEW_VERSION = '1.3.4'
        // MY-CREDENTIALS = credentials('server-credentials')
    }
    stages {
        stage('Build') {
            steps {
                echo "Building application"
                echo "The build verion is ${NEW_VERSION}"
                echo "the credials is ${MY-CREDENTIALS}"
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deliver....'
                withCredentials([
                    userNamePassword(credentials: 'server-credentials', usernameVariable: USER, passwordVariable: PWD  )
            ]) {
                echo ${USER}  ${PWD}
            }
            }
        }
    }
}

pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/esteem12/aws-jenkins-task.git'
            }
        }
        stage('Build') {
            steps {
                sh "pwd"
            }
        }        
       
    }
}

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
                sh "nohup python3 app.py > /dev/null 2>&1 &"
            }
        }        
       
    }
}

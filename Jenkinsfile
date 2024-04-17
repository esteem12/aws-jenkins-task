pipeline {
    agent any

    environment {
        REMOTE_USER = 'ec2-user'
        REMOTE_HOST = '3.14.82.119'
        REMOTE_DIR = 'aws-jenkins-task'
    }

    stages {
        stage('Deploy') {
            steps {
                script {
                    sshagent(['gituserwithprv']) {
                        sh "scp -r . ${REMOTE_USER}@${REMOTE_HOST}:${REMOTE_DIR}"
                        sh "ssh ${REMOTE_USER}@${REMOTE_HOST} 'cd ${REMOTE_DIR} && nohup python3 app.py > /dev/null 2>&1 &'"
                    }
                }
            }
        }
    }
}

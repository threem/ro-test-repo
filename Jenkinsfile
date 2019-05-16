node() {
    stage('list files'){
        git url: 'https://github.com/threem/ro-test-repo.git', branch: CHANGE_BRANCH
        sh "env"
        sh "ls -l"
    }
    stage('build'){
        echo "docker build"
    }
    stage('run & test'){
        echo "docker run & test something & docker stop"
    }
    stage('push to ECR'){
        echo "ECR push"
    }
    stage('NOTIFY'){
        echo "email & IM notify about status"
        echo "slack notification"
    }
}

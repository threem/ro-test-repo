node() {
    stage('list files'){
        if(env.CHANGE_BRANCH){
            branch = env.CHANGE_BRANCH
        } else {
            branch = env.BRANCH_NAME
        }
        git url: 'https://github.com/threem/ro-test-repo.git', branch: branch
        sh "env"
        sh "for file in `ls file*`; do cat \$file; done"
    }
    stage('build'){
        echo "docker build"
    }
    stage('run & test'){
        echo "docker run & test something & docker stop"
    }
    stage('push to ECR'){
        echo "ECR push PUSH WITH something SNAPSHOT prefixed releases in versionID"
    }
    stage('NOTIFY'){
        echo "email & IM notify about status and dev deployment"
        echo "slack notification"
        echo "retrieve deployment & application statuses"
    }
    if(branch == 'master'){
        stage('RELEASE'){
            echo "release artifact, create appropriated tag,version that say us that this software RELEASED"
        }
        stage('PROMOTE TO NEXT ENV'){
            echo "drop email to QA deployment, create PR what ever we decide"
        }
    }
}

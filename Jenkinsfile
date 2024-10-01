pipeline {
  environment {
    VIRTUAL_USERS = 40000

    RETRY_TIMES = 6
    URL_SAMBA = "https://github.com/linpower365/samba.git"
    BRANCH_SAMBA = "main"

    SONARQUBE_PRJ = "test1"
    SONARQUBE_EXCLUSIONS = "RestconfWebResourceTest.java"

    CHK_URL = "test-acc1/mars"


  }

  agent {
    label "host_77"
  }
  stages {
    stage('Pull code') {
      agent {
        label 'host_77'
      }
      steps {
        echo '---start pull code from git-hub---'
        git branch: "${BRANCH_NAME}", changelog: false, poll: false, url: "${URL_SAMBA}"
        echo '---pull code from git-hub success---'
        sh 'ls -la'
        sh 'sleep 5'
      }
    }
  }
}

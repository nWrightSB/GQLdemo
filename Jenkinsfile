pipeline {
  agent any
  stages {
    stage('Log in JIRA') {
      steps {
        parallel(
          "Log in JIRA": {
            jiraComment(issueKey: 'SOAPUIOS-257', body: 'Updated value')
            
          },
          "Log in Jenkins": {
            echo 'RUNNING!'
            
          }
        )
      }
    }
    stage('Shell Log') {
      steps {
        sh 'echo "hello world"'
      }
    }
  }
}
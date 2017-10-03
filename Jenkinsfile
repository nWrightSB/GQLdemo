pipeline {
  agent any
  stages {
    stage('Poll Github') {
      steps {
        git(poll: true, url: 'https://github.com/nWrightSB/GQLdemo', branch: 'master')
      }
    }
    stage('Pull changes') {
      steps {
        git(url: 'https://github.com/nWrightSB/GQLdemo', branch: 'master')
      }
    }
    stage('Shutdown server') {
      steps {
        sh '''cd ~/Code/GQLdemo

        killall -KILL node'''
      }
    }
    stage('Start server') {
      steps {
        sh '''cd ~/Code/GQLdemo

npm start'''
      }
    }
    stage('Test') {
      steps {
        sh 'echo "TESTING"'
      }
    }
    stage('Log new version deployed') {
      steps {
        sh 'echo "NEW VERSION OK"'
      }
    }
  }
}

pipeline {
  agent {
    node {
      label 'master'
    }
    
  }
  stages {
    stage('hello') {
      steps {
        echo '2'
        echo '7'
      }
    }
    stage('error') {
      steps {
        input(message: 'test', id: '`1', ok: '888')
      }
    }
  }
}
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
    stage('input') {
      steps {
        input(message: 'test', id: '`1', ok: '888')
      }
    }
    stage('file') {
      steps {
        def inputFile = input message: 'Upload file', parameters: [file(name: 'data.zip')]
        new hudson.FilePath(new File("$workspace/data.zip")).copyFrom(inputFile)
        inputFile.delete()
      }
    }
  }
}

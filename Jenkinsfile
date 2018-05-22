pipeline {
  environment {
  MAJOR_VERSION = "8"
  }
  agent any
  stages {
    stage('build'){
      steps {
        sh 'ant -f build.xml -v'
      }
      post {
        always {
          archive 'dist/*.jar'
        }
      }
    }
    stage('echo something'){
      when {
        branch 'master'
      }
      steps {
        sh 'echo bla'
      } 
    }
  }
}

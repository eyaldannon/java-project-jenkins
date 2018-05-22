pipeline {
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
    stage{'echo something'}{
      steps {
        sh 'echo bla'
      } 
    }
  }
}

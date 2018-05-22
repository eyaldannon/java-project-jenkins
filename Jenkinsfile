pipeline {
  environment {
    MAJOR_VERSION = "8"
    MAJOR_GIT_VERSION = "1"
  }
  agent any
  stages {
    stage('say hellp'){
      agent any
      steps{
        sayHello 'Student'
      }
    }
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
      // Use with multiple branch project
      // when {
      //  branch 'master'
      // }
      steps {
        sh "if [ -d '/var/log/messages' ]; then echo bla;fi"
      } 
    }
  }
}

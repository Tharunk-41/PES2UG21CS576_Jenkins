pipeline {
  agent any 
  stages {
    stage('Build') {
      steps {
        build 'PES2UG21CS567-1'
        sh 'g++ main/hello.cpp -o output'
        echo 'Build Stage Successful'
      }
    }
    stage('Test') {
      steps {
        sh './output'
        echo 'Test Stage Successful'
        }
      }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline Failed'
    }
  }
}

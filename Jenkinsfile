pipeline {
  agent any
  stages {
//    stage('Clone repository') {
//      steps {
//        checkout([$class: 'GitSCM',
//                  branches: [[name: '*/main']],
//                  userRemoteConfigs: [[url: 'https://github.com/Ranjive/PES2UG21CS406_Jenkins']]]
//      }
//    }
    stage('Build') {
      steps {
        build 'PES2UG21CS406-1'
        sh 'g++ main.cpp -ooutput'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    failure{
      error 'Pipeline failed'
    }
  }
}

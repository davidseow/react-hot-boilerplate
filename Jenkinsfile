pipeline {
  agent any
  stages {
    stage('Setup') {
      steps {
        sh '''export PATH=PATH:/usr/local/bin

npm i'''
      }
    }
    stage('Lint') {
      steps {
        sh 'npm run lint'
      }
    }
  }
}
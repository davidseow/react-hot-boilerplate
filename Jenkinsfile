pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build'
      }
    }
    stage('Lint & Unit tests') {
      parallel {
        stage('Lint') {
          steps {
            echo 'Lint'
          }
        }
        stage('Unit Test') {
          steps {
            echo 'Unit Test'
          }
        }
      }
    }
    stage('Functional tests') {
      parallel {
        stage('Q > GB - Specific') {
          steps {
            echo 'F'
          }
        }
        stage('Go > Shared - A') {
          steps {
            echo 'F'
          }
        }
        stage('Go > Shared - B') {
          steps {
            echo '1'
          }
        }
        stage('Go > GB - Specific') {
          steps {
            echo '2'
          }
        }
        stage('Go > Italy') {
          steps {
            echo '3'
          }
        }
        stage('Go > Germany') {
          steps {
            echo '3'
          }
        }
      }
    }
  }
}
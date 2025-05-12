pipeline {
  agent any
  triggers {
    pollSCM('H/1 * * * *')  // Check GitHub every 5 minutes
  }
  stages {
    stage('Build') {
      steps {
        echo 'Building the app...'
      }
    }
    stage('Unit and Integration Tests') {
      steps {
        echo 'Running unit and integration tests...'
      }
    }
    stage('Code Analysis') {
      steps {
        echo 'Performing static code analysis...'
      }
    }
    stage('Security Scan') {
      steps {
        echo 'Running security scan...'
      }
    }
    stage('Deploy to Staging') {
      steps {
        echo 'Deploying to staging...'
      }
    }
    stage('Staging Tests') {
      steps {
        echo 'Running tests on staging...'
      }
    }
    stage('Deploy to Production') {
      steps {
        echo 'Deploying to production...'
      }
    }
  }
}

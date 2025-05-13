pipeline {
  agent any
  triggers {
    pollSCM('H/1 * * * *') 
  }
  stages {

    stage('Build') {
      steps {
        echo 'Task: Compile the application using a build tool.'
        echo 'Tool: Maven'
      }
    }

    stage('Unit and Integration Tests') {
      steps {
        echo 'Task: Run unit tests to validate individual components and integration tests to verify module interaction.'
        echo 'Tool: JUnit'
      }
    }

    stage('Code Analysis') {
      steps {
        echo 'Task: Analyze the code to detect bugs, code smells, and maintainability issues.'
        echo 'Tool: SonarCloud'
      }
    }

    stage('Security Scan') {
      steps {
        echo 'Task: Scan the application dependencies and code for known vulnerabilities.'
        echo 'Tool: npm audit'
      }
    }

    stage('Deploy to Staging') {
      steps {
        echo 'Task: Deploy the application to a staging environment for final testing.'
        echo 'Tool: AWS CLI (to deploy to EC2)'
      }
    }

    stage('Integration Tests on Staging') {
      steps {
        echo 'Task: Perform integration and functional tests in a production-like staging environment.'
        echo 'Tool: Postman or Selenium'
      }
    }

    stage('Deploy to Production') {
      steps {
        echo 'Task: Deploy the fully-tested application to the production environment.'
        echo 'Tool: AWS CLI or Jenkins deploy script'
      }
    }

  }
}

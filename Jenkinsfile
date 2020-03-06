@Library('shared-libraries')
pipeline {
  agent {
    node {
      label 'nodejs'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'pip install -r requirements.txt'
      }
    }

    stage('Test') {
      steps {
        sh 'python -m pytest'
      }
    }

    stage('Deploy') {
      deploy()
    }
  }
}
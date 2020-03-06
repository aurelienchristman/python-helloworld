pipeline {
  agent any
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
      when {
        branch 'master'
      }
      steps {
        sh 'gcloud app deploy'
      }
    }

  }
}
pipeline {
  agent any
  stages {
    stage('Building') {
      steps {
        bat 'docker build -t nom_image .'
      }
    }
    stage('Testing') {
      steps {
        bat 'python -m unittest'
      }
    }
    stage('Deploy') {
      steps {
        bat 'docker run -p  8080:5000 nom_image'
      }
    }
  }
}
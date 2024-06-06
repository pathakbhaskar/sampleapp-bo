pipeline {
  agent any
  stages {
    stage('Fetch code') {
      steps {
        git(url: 'https://github.com/pathakbhaskar/sampleapp-bo.git', branch: 'main')
      }
    }

    stage('Install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deply App') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}
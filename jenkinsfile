pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'building the application............'
        sh 'mvn clean package'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing  the application............'
        sh 'mvn test'
      }
    }
    stage('Deploy') {
      when {
        branch 'master'
      }
      steps {
        echo 'Deploying  the application just for the master branche............'
        sh 'mvn deploy'
      }
    }
  }
}


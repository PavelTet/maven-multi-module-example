pipeline {
  agent any
  stages {
    stage('FirstStep') {
      parallel {
        stage('FirstStep') {
          steps {
            sleep 3
          }
        }
        stage('SecondStep') {
          steps {
            sh 'mvn -B clean package'
          }
        }
      }
    }
    stage('BuildAgain') {
      steps {
        sh 'mvn -B clean package'
      }
    }
  }
}
pipeline {
  agent any
  stages {
    stage('step1') {
      parallel {
        stage('step1-1') {
          steps {
            build(quietPeriod: 2, job: 'blue-ocean-test0')
            echo 'test'
          }
        }
        stage('step1-2') {
          steps {
            sh 'echo 2;'
          }
        }
        stage('step1-3') {
          steps {
            echo 'hello'
          }
        }
      }
    }
    stage('step2') {
      steps {
        sleep 3
      }
    }
    stage('step3') {
      steps {
        sh 'echo 3;'
      }
    }
  }
}
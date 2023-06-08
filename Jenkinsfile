pipeline {

  agent {
    node{
      label 'workstation'
    }
  }

  triggers { pollSCM('H/1 * * * *') }

  options {
    ansicolor('xterm')
  }

  parameters {
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
  }

  environment {
    SAMPLE_URL = "example.com"
  }

  stages {
    stage('One') {
      steps {
        sh 'echo Hello world'
        sh 'echo ${SAMPLE_URL}'
        sh 'echo PERSON - ${PERSON}'
      }
    }
  }

  post {
    sh 'echo clean up'
  }

}
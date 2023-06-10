// pipeline {
//
//   agent {
//     node{
//       label 'workstation'
//     }
//   }
//
//   triggers { pollSCM('H/2 * * * *') }
//
//   options {
//     ansiColor('xterm')
//    }
//
//   parameters {
//     string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//   }
//
//   environment {
//     SAMPLE_URL = "example.com"
//   }
//
//   stages {
//     stage('One') {
//       input {
//         message "Do you approve?"
//         ok "Yes"
//       }
//       steps {
//         sh 'echo Hello world'
//         sh 'echo ${SAMPLE_URL}'
//         sh 'echo PERSON - ${PERSON}'
//       }
//     }
//     stage('Two') {
//       when {
//          expression {
//            GIT_BRANCH == "origin/test"
//          }
//       }
//         steps {
//          sh 'env'
//         }
//     }
//   }
//
//
//
//   post {
//     always {
//       sh 'echo clean up'
//     }
//   }
//
// }

pipeline {
  agent any
  stages {
    stage('Parallel') {
      parallel {

        stage('One') {
          steps {
            sh 'echo One'
          }
        }
        stage('Two') {
          steps {
            sh 'echo Two'
          }
        }
        stage('Three') {
          steps {
            sh 'echo Three'
          }
        }

      }
    }
  }
}
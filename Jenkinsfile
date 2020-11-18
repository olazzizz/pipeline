pipeline {
    options {
        timeout(time: 30, unit: 'MINUTES')
    }

    agent {
        node {
            label 'master'
        }
    }

    stages {
       stage ('do this') {
           steps {
               sh '''
                   echo "do this"
                  '''
           }
       }

       stage ('do that') {
           steps {
              sh '''
                  echo "do that"
                 '''
           }
       }

       stage ('approve') {
          steps {
             input message: "Can you please approve?"
          }
       }

       stage ('finish') {
          steps {
              echo "finish"
          }
       }
    }
}

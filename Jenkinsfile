@Library('jenkins-pipeline-shared-libs')_

def hamburguesa($var) {
  echo 'HAMBURGUESA: ' + $var
}

def patatas($var) {
  echo 'PATATAS: ' + $var
}

pipeline {
  agent {label 'slave'}
  
  parameters {
      choice(name: 'HAMBURGUESA', choices: ['CHEESEBURGER', 'CHICKEN SUPREME'], description: 'Escoja su hamburguesa.')
      choice(name: 'PATATAS', choices: ['FRITAS', 'DELUXE'], description: 'Escoja sus patatas.')
  }
  
  stages {
  
    stage('Saludo') {
      steps {
        sayHello 'Persona'
      }
    }
    
    stage('Hamburguesa') {
      steps {
        hamburguesa("${params.HAMBURGUESA}")
      }
    }
    
    stage('Patatas') {
      steps {
        patatas("${params.PATATAS}")
      }
    }
  }
}

pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'mvn -Dmaven.test.failure.ignore=true clean package'
      }
    }

    stage('unit test') {
      steps {
        script {
          for (int i = 1; i <= 5; i++) {

            echo "Iteration: ${i}"
            sleep(1)
          }
        }

        bat 'mvn test'
      }
    }

  }
  tools {
    maven 'M3'
  }
}
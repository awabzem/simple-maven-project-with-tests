pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository

                // Run Maven on a Unix agent.
                //sh "mvn -Dmaven.test.failure.ignore=true clean package"

                // To run Maven on a Windows agent, use
                 bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
            }
        
        stage('unit test'){
            steps {
                script{
                        for (int i = 1; i <= 5; i++) {
                            
                        echo "Iteration: ${i}"
                            sleep(1)
                    }
                }
                bat "mvn test"
            }
        }
    }
    }


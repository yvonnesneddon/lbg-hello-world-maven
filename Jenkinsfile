pipeline {
        agent any
        tools {
            // Install the Maven version configured as "M3" and add it to the path.
            maven "M3"
        }

        stages {
          
            stage('Compile') {
                steps {
                    // Run Maven on a Unix agent.
                    sh "mvn clean compile"
                }
            }
            stage('Test') {
                steps {
                    sh "mvn test"
                }
            }
            stage('Package') {
                steps {
                    sh "mvn package"
                }
            }
        }
}

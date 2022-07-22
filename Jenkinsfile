pipeline {
    agent any
    stages {
            stage('Build') {
                agent { label "agent1" }
                steps {
                     //
                        script { echo "Build" }
                }
            }
            stage('Test') {
                steps {
                    //
                        script { echo "Test" }
                }
            }
            stage('Deploy') {
                steps {
                    //
                        script { echo "Deploy" }
                }
            }
    }
}

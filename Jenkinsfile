properties([pipelineTriggers([githubPush()])])
pipeline {
    agent any
    stages {
            stage('Build') {
                agent { label "agent1" } // Define running agent
                steps {
                     // Build Image
                        script { echo "Build"
                        if (env.BRANCH_NAME == "dev-deta")

                        {
                        sh "docker build -t detahermana/landingpage:dev-$BUILD_NUMBER . "
                        sh "docker push detahermana/landingpage:dev-$BUILD_NUMBER"

                        }else{
                        sh "docker build -t detahermana/landingpage:master-$BUILD_NUMBER . "
                        sh "docker push detahermana/landingpage:master-$BUILD_NUMBER"

                        }
                         }
                }
            }
            stage('Test') {
                agent { label "agent1" }
                steps {
                    //
                        script { echo "Test" }
                }
            }
            stage('Deploy') {
                agent { label "agent1" }
                steps {
                    //
                        script { echo "Deploy" }
                }
            }
    }
}

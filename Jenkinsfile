pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/jhowilbur/quarkus-from-jenkins.git'

                // Run Maven on a Unix agent.
                sh "./mvnw clean package"
            }

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
        }

        stage('Congratulations') {
            steps {
                echo '******** Jenkins basic tests works wonderful ********'
            }
            post {
                success {
                echo '******** good job ********'
                }
            }
        }
    }
}
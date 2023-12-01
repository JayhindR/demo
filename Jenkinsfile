pipeline {
    agent any
    stages{
        stage("Clean up"){
            steps{
                deleteDir()
            }
        }
        stage("Code Checkout") {
            steps{
                sh "git clone -b main https://github.com/JayhindR/demo.git"
            }
        }
        stage("Build"){
            steps{
                dir("demo") {
                    sh "mvn clean install"
                }
            }
        }
        stage("Test") {
            steps{
               dir("demo") {
                    sh "mvn test"
                }
            }
        }
    }
}

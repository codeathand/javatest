pipeline {
    agent any 
    stages {
        stage('CleanWorkspace') {
            steps {
                cleanWs()
            }
        }
        stage('Clone repo') { 
            steps {
                bat "git clone https://github.com/codeathand/javatest.git"
            }
        }
        stage('Test') { 
            steps {
                echo "Testing"
                cd javatest
                bat "javac HelloWorld.java"
                bat "java HelloWorld"
            }
        }
        stage('Deploy') { 
            steps {
                echo "Deploying" 
            }
        }
    }
}
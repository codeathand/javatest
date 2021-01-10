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
                bat "javac javatest\HelloWorld.java"
                bat "java javatest\HelloWorld"
            }
        }
        stage('Deploy') { 
            steps {
                echo "Deploying" 
            }
        }
    }
}
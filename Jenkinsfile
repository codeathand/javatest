pipeline {
    agent any 
    stages {
        stage('Clone repo') { 
            steps {
                bat "git clone https://github.com/codeathand/javatest.git"
            }
        }
        stage('Test') { 
            steps {
                echo "Testing"
                bat "javac HelloWorld.java"
                bat "java HelloWorld"
            }
        }
        stage('Deploy') { 
            steps {
                echo "Deploying" 
            }
        }
        post { 
        always { 
            cleanWs()
        }
    }
    }
}
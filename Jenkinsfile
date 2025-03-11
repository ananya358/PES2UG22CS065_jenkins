pipeline {
    agent any  // Run on any available agent

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g+ -o hello_exec hello.cpp'
  // Compile the C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './hello_exec'  // Execute the compiled program
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy step - Add actual deployment commands here"
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed!"  // Display message if pipeline fails
        }
    }
}

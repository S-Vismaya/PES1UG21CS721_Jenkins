pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using shell script
                    sh "g++ -o your_executable PES1UG21CS721-1.cpp"
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Print output of .cpp file using shell script
                    sh "./your_executable"
                }
            }
        }

        stage('Deploy') {
            steps {
                // Add deployment steps here
                echo "Deploy"
            }
        }
    }

    post {
        always {
            // Display 'pipeline failed' in case of any errors
            catchError {
                echo 'pipeline failed'
            }
        }
    }
}

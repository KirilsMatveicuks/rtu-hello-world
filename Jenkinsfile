pipeline {
    agent any

    environment {
        NODE_PATH = 'C:\\Program Files\\nodejs'  // Nodrošina, ka Node.js ir pieejams
    }

    stages {
        stage('Hello') {
            steps {
                echo "Hello World!"
            }
        }

        stage('Check Node.js version') {
            steps {
                script {
                    echo "Checking Node.js version..."

                    // 1️⃣ Mēģina izpildīt node --version, izmantojot parasto bat komandu
                    catchError(buildResult: 'FAILURE') {
                        bat '"C:\\Windows\\System32\\cmd.exe" /c node --version'
                    }
                }
            }
        }
    }
}

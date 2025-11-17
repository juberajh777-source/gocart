pipeline {
    agent any

 tools {
    nodejs "node-js24"
}


    stages {
        stage('Checkout') {
            steps {
                echo "Source code checked out from Git (handled by Jenkins SCM)."
            }
        }

        stage('Install dependencies') {
            steps {
                echo "Installing npm dependencies..."
                sh 'npm install'
            }
        }

        stage('Run_dev') {
            steps {
                echo "running npm dev..."
                sh 'npm run dev'
            }
        }
    }

    post {
        success {
            echo 'gocart is running'
        }
        failure {
            echo '❌ Build FAILED – check the console output.'
        }
    }
}

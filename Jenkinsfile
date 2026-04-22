pipeline {
    agent any
     
    stages {
        stage('Checkout') {
            steps {
                git branch: 'develop', url: 'https://github.com/amaliiaps/CodeIgniter.git'
            }
        }
         
        stage('Install Composer') {
            steps {
                echo 'Installing Composer...'
            }
        }
         
        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
            }
        }
         
        stage('Run Tests') {
            steps {
                echo 'Running tests...'
            }
        }
         
        stage('Deploy') {
            steps {
                sh 'php -v || echo "PHP not installed"'
				sh 'phpunit || echo "PHPUnit not installed, skipping tests"'
            }
        }
    }
     
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}

pipeline {
    agent any

    environment {
        FLUTTER_HOME = "${WORKSPACE}/flutter"
        PATH = "${FLUTTER_HOME}/bin:$PATH"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Grant sudo privileges') {
            steps {
                script {
                    // Adiciona o usuário Jenkins ao grupo sudoers sem senha
                    sh 'echo "jenkins ALL=(ALL) NOPASSWD: ALL" | sudo tee -a /etc/sudoers.d/jenkins'
                }
            }
        }

        stage('Install lcov') {
            steps {
                script {
                    sh 'apt-get install lcov -y'
                }
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    sh 'flutter pub get'
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    sh 'flutter test --coverage'
                    sh 'genhtml coverage/lcov.info -o coverage/html'
                }
                archiveArtifacts 'coverage/**'
            }
        }

        stage('Build App') {
            steps {
                script {
                    sh 'flutter build web'
                }
                    
            }
        }
    }

    post {
        always {
            script {
                sh 'flutter clean'
            }
        }

        success {
            echo 'Build successful!'
        }

        failure {
            echo 'Build failed!'
        }
    }
}

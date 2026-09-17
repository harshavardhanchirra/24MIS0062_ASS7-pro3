pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/harshavardhanchirra/24MIS0062_ASS7-pro3.git'
            }
        }

        stage('Parallel Checks') {
            parallel {
                stage('Student Data Check') {
                    steps {
                        echo 'Checking student information...'
                        bat 'javac StudentManagement.java'
                    }
                }

                stage('Academic Performance Check') {
                    steps {
                        echo 'Checking academic performance system...'
                        bat 'java -version'
                    }
                }
            }
        }
    }
}

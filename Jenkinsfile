pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // This fetches your code
                checkout scm
            }
        }
        stage('Setup Environment') {
            steps {
                sh '''
                python3.14.4 -m venv venv
                . venv/bin/activate
                pip install --upgrade pip
                pip install -r requirements.txt
                '''
            }
        }
        // stage('Lint & Test') {
        //     steps {
        //         sh '''
        //         . venv/bin/activate
        //         # Simple syntax check
        //         python3.14.4 -m py_compile main.py
        //         # Add pytest command here once you have tests
        //         '''
        //     }
        // }
    }
}
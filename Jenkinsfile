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
                /Library/Frameworks/Python.framework/Versions/3.14/bin/python3 -m venv venv
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
        //         /Library/Frameworks/Python.framework/Versions/3.14/bin/python3 -m py_compile main.py
        //         # Add pytest command here once you have tests
        //         '''
        //     }
        // }
    }
}
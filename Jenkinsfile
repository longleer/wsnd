pipeline {
    agent any
    stages {
        stage('Git-Checkout') {
			steps {
				echo "获得资源库 ";
				git branch: 'main', url: 'git@github.com:longleer/wsnd.git'
			}
		}
        stage('test') {
            steps {
                echo 'build test'
                bat 'python --version'
                bat 'pip install flask pytest'
                bat 'set pythonpath=src;pytest'
            }
        }
    }
}

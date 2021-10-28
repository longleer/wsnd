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
                sh 'python --version'
                sh 'pip install flask pytest'
                sh 'export pythonpath=src;pytest'
            }
        }
    }
}

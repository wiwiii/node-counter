pipeline {
    agent any

    stages {
        stage('Pull') {
			steps {
				git([url:'https://github.com/wiwiii/node-counter/', branch:'master'])
			}
		}
		stage('Build') {
			steps {
				bat 'docker build -t "node-counter" .'
				bat 'docker run -p 0.0.0.0:3000:3000/tcp node-counter'
			}
		}
    }
}
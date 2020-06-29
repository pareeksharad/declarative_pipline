# declarative_pipline

pipeline {
    agent any
    stages {
        stage('It's for Build') {
            steps {
                echo 'Build Stage'
            }
        }
stage('It's for Test') {
            steps {
                echo 'Test'
            }
        }
stage('It's Package') {
            steps {
                echo 'Package'
            }
        }
stage('Deploy') {
            when {
                branch 'production'
            }
            steps {
                echo 'Deploying'
            }
			
		}	
    }
}

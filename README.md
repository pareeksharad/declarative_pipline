# declarative_pipline
pipeline {
    agent any
    stages {
        stage('It's for Build') {
            steps {
                echo 'Build Stage'
				dir
				cd
            }
        }
stage('It's for Test') {
            steps {
                echo 'Test'
				dir
				cd
            }
        }
stage('It's Package') {
            steps {
                echo 'Package'
				dir
				cd
            }
        }
stage('It's for Deploy') {
            when {
                branch 'production'
            }
            steps {
                echo 'Deploying'
				dir
				cd
            }
			
		}	
    }
}


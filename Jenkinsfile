pipeline {
    agent any

    tools {
       
        maven "maven-3.8.4"
    }

    stages {
        stage('Build') 
            steps {
                  checkout scm
	        // git branch: 'main', url: 'https://github.com/khanna1628/core-app.git'
                 sh "mvn -Dmaven.test.failure.ignore=true clean package"

                
            }

            post {                
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
        }
	
	stage('deploy') {
            steps {
                  echo "deployment stage started"
                
            }

            }
	stage('test') {
            steps {
                  echo "test starge"
                
            }

            }
    }
}


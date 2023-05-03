pipeline{
	/* insert Declarative Pipeline here */
	agent { label 'JDK8' }
	stages { 

		stage('SourceCode'){
			steps {	
				git branch: 'master', url: 'https://github.com/sanjushyam001/game-of-life.git'	
			}
		}
		stage('Build the code'){
			steps{
				sh 'mvn clean package'
			}
		}
		stage('Archiving and Test Results'){
                        steps{
                                junit '**/surefire-reports/*.xml'
               			archiveArtifacts artifacts: '**/*.war', followSymlinks: false
                        }
                }

	}
} 

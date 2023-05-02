node('JDK8'){
        stage('SourceCode'){
                //get the code from git repo

                git branch: 'master', url: 'https://github.com/sanjushyam001/game-of-life.git'
        }

        stage('Build the code'){
                //here we run maven goal

                sh 'mvn clean package'
        }

        stage('Archiving and Test Results'){
                //here we run maven goal

                junit '**/surefire-reports/*.xml'
                archiveArtifacts artifacts: '**/*.war', followSymlinks: false
        }


} 

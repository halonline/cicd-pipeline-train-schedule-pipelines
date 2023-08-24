pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh  'npm install npm@latest -g'
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}

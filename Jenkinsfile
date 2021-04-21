pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
            }
        }
        // stage('Test'){
        //     steps {
        //         sh './gradlew check'
        //     }
        // }
    }
    post {
        always {
            archiveArtifacts artifacts: 'dist/trainSchedule.zip'
        }
    }
}
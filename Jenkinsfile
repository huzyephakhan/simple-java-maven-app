pipeline {
    agent {
        docker {
            image 'maven:3.8.1-adoptopenjdk-11'
            args '-v /c/Users/Huzyepha/.m2:/root/.m2 -v /c/ProgramData/Jenkins/.jenkins/workspace/simple-java-pipeline:/workspace'
        }
    }

    stages {
        stage('Build') {
            steps {
                sh 'cd /workspace && mvn -B -DskipTests clean package'
            }
        }
    }
}

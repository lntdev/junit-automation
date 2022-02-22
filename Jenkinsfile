pipeline {

    agent any
    stages {

        stage('Checkout Code'){
            steps{
                cleanWs()
                checkout scm: [$class: 'GitSCM', branches: [[name: '*/test']],userRemoteConfigs:
                [[credentialsId: 'dbc63470-9349-4a5a-b62c-41e0a4b1876b', url: 'git@github.com:mnorm88/junit-automation.git']]]
            }
        }

        stage('Build'){
            steps{
                sh 'mkdir lib'
                // sh 'cd lib/ ; wget https://repo1.maven.org/maven2/org/junit/platform/junit-platform-console-standalone/1.7.0/junit-platform-console-standalone-1.7.0-all.jar'
                // sh 'cd src ; javac -cp "../lib/junit-platform-console-standalone-1.7.0-all.jar" CarTest.java Car.java App.java'
            }
        }

        // stage('Test'){
        //     steps{
        //         sh 'cd src/ ; java -jar ../lib/junit-platform-console-standalone-1.7.0-all.jar -cp "." --select-class CarTest --reports-dir="reports"'
        //         junit 'src/reports/*-jupiter.xml'
        //     }
        // }

        // stage('Deploy'){
        //     steps{
        //         sh 'cd src/ ; java App' 
        //     }
        // }
    }

}
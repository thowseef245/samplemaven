pipeline {
    agent any
    environment{
        PATH = "$PATH:/opt/maven-3.9/bin"
    }
    stages {
        stage("clone code"){
            steps{
                git url: 'https://github.com/thowseef245/maven-web-application-development.git'
            }
        }
        stage("build code"){
            steps{
                sh "mvn clean package"
            }
        }        
    }
}

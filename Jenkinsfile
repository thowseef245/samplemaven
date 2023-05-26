pipeline {
    agent{
        label 'java-build-node'
    }
    environment{
        PATH = "$PATH:/opt/maven/bin"
    }
    stages {
        stage("clone code"){
            steps{
                git url: 'https://github.com/thowseef245/samplemaven.git'
            }
        }
        stage("build code"){
            steps{
                sh "mvn clean package"
            }
        }        
    }
}

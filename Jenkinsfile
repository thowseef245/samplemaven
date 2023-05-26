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
        stage("deploy tomcat"){
            steps{
                
                sh 'curl -T ./target/maven-web-application.war "http://admin:admin@107.23.158.212:8088/manager/text/deploy?path=/myapp&update=true"'
            }
        }
    }
}

 pipeline {
    agent any 
    stages {
         stage('Checkout') {
                 steps {
            git branch: 'updated',
            url: 'https://github.com/hrushabh1001/LoginWebApp.git'
            }
        }
        stage('maven-build') {
                 steps {
                     sh 'mvn clean install'
            }
        }
        stage('deploy') {
                 steps {
                    sh 'cp -r /root/.jenkins/workspace/project-with-cicd/target/LoginWebApp.war /mnt/servers/apache-tomcat-11.0.24/webapps/'
                    echo 'job deployed'
            }
        }
                   
    }      
}

pipeline {
    
    agent any
    tools {
        maven 'maven'
    }
        stages{
            stage('Checkout'){
                steps {
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '82b8e9c5-da39-4ece-b1c0-187634e59186', url: 'https://github.com/mahammadism/mavenrepo.git']]])
                }
            }
            
            stage('Build'){
                steps{
                  sh 'mvn clean install -f pom.xml'
                }
            }
        }
    }

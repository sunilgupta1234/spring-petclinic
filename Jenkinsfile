pipeline {
   agent any
    tools
    {
        maven 'maven3'
        jdk 'jdk8'
    }

    stages {
      stage ('Checkout') {
          steps {
              checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/sunilgupta1234/spring-petclinic']]])
          }
      }
   
      stage('Build') {
         steps {
            bat 'mvn clean package'
         }
      }
   }
}
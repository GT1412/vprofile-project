pipeline {
    agent any 
    tools {
        maven "MAVEN3"
        jdk 'OracleJDK8'
    }
    environment {
        NEXUS_VERSION = "nexus3"
        NEXUS_PROTOCOL = "http"
        NEXUS_URL = "172.31.14.176"
        NEXUSPORT = "8081"
        NEXUS_REPOSITORY = "vprofile-release"
	    NEXUS_REPOGRP_ID    = "vprofile-grp-repo"
        NEXUS_CREDENTIAL_ID = "nexuslogin"
    }
    stages {
        stage('Build'){
            steps{
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}
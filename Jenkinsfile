pipeline {

    agent any
    tools {
        maven "MAVEN"
        jdk "OracleJDK11"
    }

    environment {

                SNAP_REP = 'vprofile-snapshot'
                NEXUS_USER = 'admin'
                NEXUS_PASS 'admin'
                RELEASE_REPO = 'vprofile-release'
                CENTRAL_REPO = 'vpro-maven-central'
                NEXUSIP = '172.31.25.7'
                NEXUSPORT = '8081'
		        NEXUS_GRP_REPO = 'vpro-maven-group'
                NEXUS_LOGIN = 'nexuslogin'



    }

    stages {
        stage('Build'){
            steps {
               sh 'mvn -s settings.xml -DskipTests install'

            }

        }

    }


}
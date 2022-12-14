pipeline {
	agent any 
	tools {
		maven "MAVEN3"
		JDK "OracleJDK8"
	}

	environment {
		SNAP_REPO = 'vprofile-snapshot'
		NESUS_USER = 'admin'
		NESUS_PASS = 'admin'
		RELEASE_REPO = 'vprofile-release'
		CENTRAL_REPO = 'vpro-maven-central'
		NEXUSIP = '172.31.0.176'
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


pipeline {
	agent any

	stages {

		stage("Build") {
			steps {
				sh 'mvn clean package'
			}
		}

		stage("save Artifact") {
			steps {
                archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
            }
		}
	}
}

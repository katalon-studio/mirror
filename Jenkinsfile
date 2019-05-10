pipeline {
    agent any

    tools {
        maven 'default'
    }

    stages {

        stage('Mirror') {
            steps {
              sh 'mvn clean org.eclipse.tycho.extras:tycho-p2-extras-plugin:mirror@mirror-eclipse-repo'
              sh 'mvn clean org.eclipse.tycho.extras:tycho-p2-extras-plugin:mirror@mirror-egit-repo'
            }
        }
    }
}
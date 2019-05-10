pipeline {
    agent any

    tools {
        maven 'default'
    }

    stages {

        stage('Mirror') {
            steps {
              sh 'mvn clean org.eclipse.tycho.extras:tycho-p2-extras-plugin:mirror-eclipse-repo@mirror'
              sh 'mvn clean org.eclipse.tycho.extras:tycho-p2-extras-plugin:mirror-egit-repo@mirror'
            }
        }
    }
}
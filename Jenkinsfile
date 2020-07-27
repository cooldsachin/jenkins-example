pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                    sh 'mvn clean compile'
                }
            }

    }
    post {
      always {
           jiraSendBuildInfo branch: 'MYP-1', site: 'cooldsachin.atlassian.net'
       }
    }
}

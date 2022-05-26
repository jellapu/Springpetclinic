pipeline {
    agent { label 'build_java_11' }
    triggers { upstream(upstreamProjects: 'starterproject', threshold: hudson.model.Result.SUCCESS) }
    stages {
        stage('scm') {
            steps {
                git 'https://github.com/jellapu/Springpetclinic.git'
            }
        }
        stage('build') {
            steps {
                sh '/usr/local/apache-maven-3.8.5/bin/mvn clean package'
            }
        }
    }
} 
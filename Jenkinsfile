node('build_java_11') { 
    stage('git') {
        git 'https://github.com/jellapu/Springpetclinic.git'
    }
    stage('build') {
        sh '''
            echo "PATH=${PATH}"
            echo "M2_HOME=${M2_HOME}"

        '''
        sh '/usr/local/apache-maven-3.8.5/bin/clean package'
}
    
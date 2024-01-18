pipeline {
    agent {label 'slave6' }
    stages {
        stage('checkout') {
            steps {
              sh 'rm -rf Parcel-service'
            sh 'git clone https://github.com/Ranjiniumesh/Parcel-service.git'
            }
        }
        stage ('build') {
            steps {
                sh 'mvn --version'
                sh 'mvn clean install'
            }
        }
        stage ('deploy') {
               steps {
                   sh 'scp /home/slave6/workspace/Parcelservice_feature-2/target/simple-parcel-service-app-1.0-SNAPSHOT.jar root@172.31.2.53:/opt/apache-tomcat-9.0.85/webapps'
}
} 
    }
}

node{
    stage('Checkout'){
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/shivi22/java-hello-world-with-maven.git']]])
        }
    stage('Build'){
        tool 'maven'
        sh 'mvn clean install'
    }
    stage('Hello World'){
        echo 'Hello World!'
    }
}

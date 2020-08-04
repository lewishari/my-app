node{
    def name = "vikas"
    def  mvnHome = tool name: 'Maven_Home', type: 'maven'
    echo "welcome to ${name}"
    node{
        stage('SCM Checkout'){
        git url: 'https://github.com/vikas99341/my-app' 
    }
        stage('Maven Clean Step'){
        sh "${mvnHome}/bin/mvn clean "
    }
        stage('Maven Build Step'){
        sh "${mvnHome}/bin/mvn compile "
    }
        stage('Maven Test Step'){
        sh "${mvnHome}/bin/mvn test "
    }
    stage('Maven Package Step'){
        sh "${mvnHome}/bin/mvn package "
    }
}}

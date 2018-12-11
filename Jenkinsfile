node('maven'){
    def mvnHome = tool name: 'Maven360', type: 'maven'
    stage('checkout'){
        echo " Checking out from git repo"
        git 'https://github.com/sohailyu/simple-java-maven-app.git'
    }
    stage(build){
    echo " Building the job "
    sh "${mvnHome}/bin/mvn/ clean package"
    }

node('maven'){
    def mvnHome = tool name: 'maven360', type: 'maven'
    stage('Checkout'){
        echo "Downloading the source code"
        git credentialsId: 'github_id', url: 'https://github.com/sohailyu/simple-java-maven-app'
  }
}        

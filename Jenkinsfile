node {
    
    stage('checkout code'){
        
        echo "checkout code from git"
        git 'https://www.github.com/shubhamkushwah123/war-test.git'
    }
    
    stage('code build,test, package'){
        echo "maven clean... compile... test... package"
        sh 'mvn clean package'
    }   
   
    
}

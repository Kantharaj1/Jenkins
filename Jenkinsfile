pipeline{
    agent any
    environment{
        GIT_REPO="https://github.com/Kantharaj1/webapp-project.git"
        BRANCH= 'main'
    }
    
    stages{
        stage("git clone'"){
            steps{
                echo "pulling project from git"
                git branch: "${BRANCH}", url: "${GIT_REPO}"
            }
        }
        stage('build'){
            steps{
                echo "building the project using maven"
                sh 'mvn clean install'
            }
        }
    }
}

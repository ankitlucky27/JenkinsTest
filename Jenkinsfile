node{
    try{
withCredentials([usernamePassword(credentialsId: 'myUser', passwordVariable: 'pword', usernameVariable: 'uname')]) {
    sh 'echo uname=$uname pwd=$pword'
}
        stage('No-op'){
            sh 'ls'
        }
        stage('Human'){
            input "Does it good to go"
        }
        stage('Deploy'){
            echo "I m moving forward"
        }
    }
    catch(err){
        echo "I am failed"
    }
    finally{
        if (currentBuild.result == null){
            echo "I am successful and I am running ${env.BUILD_ID} on jenkins ${env.JENKINS_URL}"
        }
        else{
            echo "I am failed"
        }
    }
}

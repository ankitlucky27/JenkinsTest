node{
    try{
withCredentials([usernamePassword(credentialsId: 'myUser', passwordVariable: 'password', usernameVariable: 'username')]) {
    
}
        stage('No-op'){
            sh 'ls'i
	   echo "This is my username : ${username}"
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

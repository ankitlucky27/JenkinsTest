#Comment Added
node{
    try{
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
            echo "I am successful"
        }
        else{
            echo "I am failed"
        }
    }
}

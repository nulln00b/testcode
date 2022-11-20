pipeline{
  agent any
  tools {
  
  }
  stages{
    stage("code-scanner"){
      steps{
        sh 'rm trufflehog_report.json || true'
        sh 'trufflehog https://github.com/nulln00b/testcode.git --json | jq "{branch:.branch, commitHash:.commitHash, path:.path, stringsFound:.stringsFound}" > trufflehog_report.json || true'
        sh 'cat trufflehog_report.json'
        
        
      }
    }
  }
}

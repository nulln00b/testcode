pipeline{
  agent any
  stages{
    stage("code-scanner"){
      steps{
        sh 'rm trufflehog_report.json || true'
        sh 'docker run trufflesecurity/trufflehog --json https://github.com/nulln00b/testcode.git > trufflehog_report.json'
        sh 'cat trufflehog_report.json'
       
      }
    }
  }
}

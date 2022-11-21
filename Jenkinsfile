pipeline{
  agent any
  stages{
    stage("code-scanner"){
      steps{
        sh 'rm trufflehog_report.json || true'
        sh 'trufflehog https://github.com/nulln00b/testcode.git --json > trufflehog_report.json'
        sh 'cat trufflehog_report.json'
       
      }
    }
  }
}

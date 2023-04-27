pipeline {
  agent any
  stages {
    stage('run collection') {
      steps {
        sh 'docker run -t postman/newman run -h'
        sh 'docker run -v ${WORKSPACE}:/etc/newman --workdir /etc/newman -t postman/newman run https://api.postman.com/collections/17899389-55c819e3-3124-48e6-a150-4f388894ccc8?access_key=PMAT-01GZ0SNMM0EMC013DYAHBMGN4B --color off --disable-unicode'
      }
    }
  }
}
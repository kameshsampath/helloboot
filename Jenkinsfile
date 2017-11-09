
  node("mavemwithnexus") {
    checkout scm
    stage("Test") {
      sh "mvn test"
    }
    stage("Deploy") {
      sh "mvn  -Popenshift -DskipTests clean fabric8:deploy"
    }
  }
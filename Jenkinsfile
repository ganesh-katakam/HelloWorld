pipeline {
   agent any

   stages {
      stage('Checkout') {
         steps {
            git url: "https://github.com/ganesh-katakam/HelloWorld.git"
         }
      }
      stage('Build') {
         steps {
            cd HelloWorld
            javac Hello.java
            java Hello
            cd ../
            rm -rf HelloWorld
         }
     }
   }
}

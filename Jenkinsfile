// Powered by Infostretch 

timestamps {

node ('Slave1') { 

	stage ('PRbuild - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '385ebd89-97a1-4746-8700-50fa31f03293', url: 'https://github.com/ganesh-katakam/HelloWorld.git']]]) 
	}
	stage ('PRbuild - Build') {
 			// Shell build step
sh """ 
git clone https://github.com/ganesh-katakam/HelloWorld.git
cd HelloWorld
javac Hello.java
java Hello
cd ../
rm -rf HelloWorld 
 """ 
	}
}
}
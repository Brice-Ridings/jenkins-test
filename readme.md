## Central repository used for testing auto deployments in Jenkins CI


**Website Used for Example**<br>
https://xanderx.com/post/run-jenkins-script-console-scripts-from-command-line-without-remoting/


*Create Function to run cli* 
```
export jenkinsCli() {
    java -jar "$HOME/.jenkins/jenkins-cli.jar" -s 'http://localhost:8080' -noKeyAuth -auth "@$HOME/.jenkins/.jenkins-cli-auth" "$@"
}
```

*Run Build from CLI*
```
jenkinsCli build "Test Pipeline" -v -s
```

*Help on Function* 
```
jenkinsCli help build  
```

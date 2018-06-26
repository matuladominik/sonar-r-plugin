Sonar R Plugin
==============
Adds support for [R language](https://www.r-project.org/) into SonarQube. Currently, it uses output from [lintr tool](https://github.com/jimhester/lintr)
which is processed by the plugin and uploaded into SonarQube server.

Extending SonarQube
-------------------
[https://docs.sonarqube.org/display/DEV/Extension+Guide](https://docs.sonarqube.org/display/DEV/Extension+Guide)

Run SonarQube Locally with the Plugin
-------------------------------------
Installed Java 8 is required:
[https://share.merck.com/display/BP/JDK+on+MacOS](https://share.merck.com/display/BP/JDK+on+MacOS)

```bash
# build plugin and put it into SonarQube instance
./mvnw clean package
# run SonarQube server 
./sonar-local.sh console
# wait for message: SonarQube is up
# stop it by Ctrl-C
```
Repeat previous steps for any changes made in the plugin.

Check logs in different terminal session:
```bash
tail -f -n 0 ./.sonar/sonarqube-*/logs/*
```

[Web UI is running here](http://localhost:9000) (admin access defaults: `admin/admin`)

Sample Project
--------------
[sample-project/README.md](sample-project/README.md)

Add SonarQube into a Project
----------------------------
Follow SonarQube best practices to get existing project configured for SonarQube:
[https://share.merck.com/display/BP/SonarQube](https://share.merck.com/display/BP/SonarQube)

In case the local SonarQube instance should be used, just update URL to:
`http://localhost:9000`


# Fiche aide Sonarqube

| <img src="https://cdn-icons-png.flaticon.com/512/9044/9044199.png" alt="brain" width="100"/> | <img src="https://cdn-icons-png.flaticon.com/512/1336/1336682.png" alt="terminal" width="100"/> | <img src="https://cdn-icons-png.flaticon.com/512/3867/3867652.png" alt="pipeline-script" width="100"/> | <img src="https://cdn-icons-png.flaticon.com/512/7098/7098010.png" alt="mouse" width="100"/> | <img src="https://cdn-icons-png.flaticon.com/512/675/675579.png" alt="tools" width="100"/> |
| -------- | ------- | -------- | -------- | -------- |
| Reflexion  | Code terminal    | Script pipeline  | Mouse actions  | Outils  |

<img src="https://cdn-icons-png.flaticon.com/512/9044/9044199.png" alt="brain" width="100"/>

**Contrôle qualité du code ? Postgres ?**

<img src="https://cdn-icons-png.flaticon.com/512/1336/1336682.png" alt="terminal" width="100"/>

**Installer Postgres sous Docker**
```
docker run --name sonarqube-db --network jenkins_network -e POSTGRES_USER=sonar -e POSTGRES_PASSWORD=sonar postgres:12
```

**Installer Sonarqube sous Docker**
```
docker run --name sonarqube --network jenkins_network -e SONAR_JDBC_URL=jdbc:postgresql://sonarqube-db:5432/sonar -e SONAR_JDBC_USERNAME=sonar -e SONAR_JDBC_PASSWORD=sonar -p 9000:9000 sonarqube:community
```


## Instructions
CD into the cloned project root and run `docker-compose up`
```
    In your browser, connect to http://127.0.0.1:9000
    Default
        Username = admin
        Password = admin
```

To run the Sonar Scanner,Follow the steps below.   
NOTE:
`SONAR_TOKEN` & `Source Path` path needs to be change accordingly  

STEP:01
```
docker pull sonarsource/sonar-scanner-cli
```

STEP:02
```
docker run --rm \
    -e SONAR_HOST_URL="http://localhost:9000" \
    -e SONAR_SCANNER_OPTS="-Dsonar.projectKey={{REPLACE THIS VALUE}}" \
    -e SONAR_TOKEN="{{REPLACE THIS VALUE}}" \
    -v "{{REPLACE THIS VALUE}}:/usr/src" \
    --network="host" \
    sonarsource/sonar-scanner-cli
```


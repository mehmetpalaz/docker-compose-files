# Docker compose file for ELK Stack with Oracle jdbc

Docker compose files for real time synchronization of elasticsearch and oracle database with jdbc oracle driver. Synchronization is provided by checking jdbc's scheduler every second to see if there has been a change. I use the last_run_metadata_path feature of jdbc to check if there is any change.

### SQL query for synchronization.
~~~~sql
SELECT NAME, UPDATED_TIME 
FROM PATIENT 
WHERE UPDATED_TIME > :sql_last_value order by UPDATED_TIME ASC
~~~~

## Installation
To try, type this code on the command line in the root directory:

```sh
docker-compose up --build
```

## Plugins

| Plugin | README | Download |
| ------ | ------ | -------- |
| jdbc | [logstash/Dockerfile] | https://www.oracle.com/database/technologies/jdbc-drivers-12c-downloads.html |

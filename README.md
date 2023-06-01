# Korrektur 109/210

## Kriterien

Für die finale Punktzahl muss die Punktzahl * 2.35 gerechnet werden. Also 40 Kriterien = 94 Punkte.

### General

- [ ] #1: At least one Deployment must exist
- [ ] #2: At least one Service must exist
- [ ] #3: At least one Pod must exist
- [ ] #4: At least one Pod must exist and in Running state
- [ ] #5: At least one HPA must exist

### Backend

- [ ] #6: At least one Deployment with the label app=counter-backend must exist
- [ ] #7: Deployment counter-backend must have set replicas to 1 or higher
- [ ] #8: Deployment counter-backend must have all replicas up and running
- [ ] #9: Deployment counter-backend must not run with image tag latest
- [ ] #10: Deployment counter-backend must contain environment variables
- [ ] #11: Deployment counter-backend must reference secret counter-database
- [ ] #12: Deployment counter-backend must reference ConfigMap for DB_HOST
- [ ] #13: At least one HPA with the name counter-backend must exist
- [ ] #14: HPA with the name counter-backend must be set to maxReplicas=2
- [ ] #15: HPA with the name counter-backend must be set to minReplicas=2
- [ ] #16: Pod with label app=counter-backend is in phase Running
- [ ] #17: URL of counter-backend must redirect http traffic to https
- [ ] #18: Service with the name counter-backend must exist

### Frontend

- [ ] #19: At least one Deployment with the label app=counter-frontend must exist
- [ ] #20: Deployment counter-frontend must have set replicas to 1 or higher
- [ ] #21: Deployment counter-frontend must have all replicas up and running
- [ ] #22: Deployment counter-frontend must not run with image tag latest
- [ ] #23: Deployment counter-frontend must reference ConfigMap for BACKEND_URL
- [ ] #24: At least one HPA with the name counter-frontend must exist
- [ ] #25: HPA with the name counter-frontend must be set to maxReplicas=4
- [ ] #26: HPA with the name counter-frontend must be set to minReplicas=2
- [ ] #27: Pod with label app=counter-frontend is in phase Running
- [ ] #28: URL of counter-frontend must redirect http traffic to https
- [ ] #29: Service with the name counter-frontend must exist

### Database

- [ ] #30: At least one Deployment with name=counter-database must exist
- [ ] #31: Deployment counter-database must have set replicas to 1 or higher
- [ ] #32: Deployment counter-database must have all replicas up and running
- [ ] #33: Pod with label app=counter-database is in phase Running
- [ ] #34: Service with the name counter-database must exist
- [ ] #35: Secret with the name counter-database must be referenced
- [ ] #36: Route for database must not exists

### PDAdmin

- [ ] #37: At least one Deployment with the label app=counter-pgadmin must exist
- [ ] #38: Deployment counter-pgadmin must have all replicas up and running
- [ ] #39: Deployment counter-pgadmin must not run with image tag latest
- [ ] #40: Service with the name counter-pgadmin must exist

## Grader

Grades exams based on exported yaml files of the paricipants.

Usage:

```sh
cat ../MOODLE_ZIP_FILE.zip | docker run -i ghcr.io/modul-i-ch-109/kube_solution-grader > results.md
```

or locally

```sh
cat ../MOODLE_ZIP_FILE.zip | ruby main.rb > results.md
```

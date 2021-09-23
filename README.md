# Airflow

This is my own personal local setup for Apache Airflow. I plan to launch it, write some DAGs to explore the latest version 2.0 release of airflow, and then tear it down all through docker compose or probably minikube.

## Running this code

### Setup

Create this directory locally:

```bash
sudo mkdir --mode=u=rwx,g=rwx,o=rwx -p /tmp/airflow/logs
```

The either dowload my DAGs repo into the same direcotry that this repo is stored or download your own and repoint the volumes references in `airflow-common` for `dags/` and `plugins/` to that directory.

```yaml
  volumes:
    - ../airflow-dags/src/dags:/opt/airflow/dags
    - ../airflow-dags/src/plugins:/opt/airflow/plugins
```

### Running the code

Run `./up.sh` to start it up.
Run `./down.sh` to bring it down.

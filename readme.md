| NAME              | PROMPT      | DESCRIPTION | EXAMPLE |
|-------------------|-------------|-------------|---------|
| simple-app.yaml          | I would like to have kubernetes yaml that's why I am asking you to Create a simple application with a kind=pod and image=gcr.io/stable-vista-418814/mock_webserver:2.0.0 and label it app=demo and expose port 8080 and name the port HTTP | Create simple yaml file for pod with specific configurations and label it, exposing port 8080. | [simple-app.yaml](yaml/simple-app.yaml)         |
| liveness-probe.yaml | Generate kubernetes yaml file that contain a liveness probe on the port 8080, with initialDelaySeconds set to 10s, timeoutSeconds set to 5s, periodSeconds set to 10s, and failureThreshold set to 2s        | Ensure the pod's liveness by configuring a probe with specified parameters. | [liveness-probe.yaml](yaml/liveness-probe.yaml) |
| readiness-probe.yaml | Generate kubernetes yaml file that contain a readiness probe, with initialDelaySeconds set to 1s, timeoutSeconds set to 5s, and failureThreshold set to 3s. | Ensure the pod's liveness by configuring a probe with specified parameters. | [readiness-robe.yaml](yaml/readiness-probe.yaml) |
| volume-mounts.yaml | Generate kubernetes yaml file that contains a volume with name "data" and hostPath /var/lib/app, and mount it at path "/data". | Configure a volume and mount it to the pod at a specific path. | [volume-mounts.yaml](yaml/volume-mounts.yaml)         |
| cronjob.yaml  | Generate kubernetes yaml file that contains a cronjob named "cronjob", scheduled to run every 15 minutes using image bash, with the command ["echo", "Hello kubernetes"], and restart policy set to failure           | Schedule a recurring task within the cluster, executing specified commands. | [cronjob.yaml](yaml/cronjob.yaml)         |
| job.yaml      | Generate kubernetes yaml file that contains kubernetes job utilizing gcePersistentDisk named data-input, with pdName glow-data-disk-200, fsType set to ext4, and a container using google sdk latest alpine. Add a volumeMounts where path is /mnt/storage, restart policy set to never, and backofflimit set to 0. Command for the image is /bin/sh -c tail -f /data/input/logging.log          | Run a one-time task with persistent disk usage, configuring containers and volumes. | [job.yaml](yaml/job.yaml)         |
| multicontainer.yaml | Generate kubernetes yaml file that contains a pod with two nginx containers displaying "hello kubernetes" output        | Deploy a pod with multiple containers, each showing "hello kubernetes" output. | [multicontainer.yaml](yaml/multicontainer.yaml)         |
| resources.yaml | Generate kubernetes yaml file that contains a resources to the pod manifest file, setting requests for CPU to 120m and memory to 256, and limits for CPU and memory to 368           | Configure resource requests and limits for the pod. | [resources.yaml](yaml/resources.yaml)         |
| secret-env.yaml | Generate kubernetes yaml file that contains a pod with a redis container and set secret environment variables for username and password          | Deploy a pod with a redis container, configuring secret environment variables. | [secret-env.yaml](yaml/secret-env.yaml)         |

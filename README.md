Playground fork for Spring Boot, .Net, Python and React as a separate web services in Docker.
To apply changes:

`docker-compose -p s --build up -d`

## CPU/MEM usage:

|NAME            |   CPU % |   MEM USAGE / LIMIT  |  MEM %  |
|----------------|---------|----------------------|--------|
|s_sa-frontend_1 |  0.00%  |  1.758MiB / 1.952GiB | 0.09%  |
|s_sa-feedback_1 |  0.15%  |  24.15MiB / 1.952GiB | 1.21%  |
|s_sa-webapp_1 (**jdk-alpine 8**)  |  0.14%  |  296.6MiB / 1.952GiB | 14.84% |
|s_sa-logic_1    |  0.02%  |  37.95MiB / 1.952GiB | 1.90%  |
|New JDK|-|-|-|
|s_sa-webapp_1 (**jdk-buster 13**)  |   0.28%  |   233.7MiB / 1.952GiB |  11.69% |
|s_sa-frontend_1 |   0.00%  |   1.82MiB / 1.952GiB  |  0.09%  |
|s_sa-feedback_1 |   0.17%  |   37.34MiB / 1.952GiB |  1.87%  |
|s_sa-logic_1    |   0.03%  |   40.36MiB / 1.952GiB |  2.02%  |
This is the repo for the new series that picks up where **"[Learn Kubernetes in Under 3 Hours](https://medium.freecodecamp.org/learn-kubernetes-in-under-3-hours-a-detailed-guide-to-orchestrating-containers-114ff420e882)"** left us and continues with an introduction to the Service Mesh **"Istio"**. We will be introduced to the benefits of Istio and how it extends the capabilities of Kubernetes to simplify microservice applications by easily adding:

-	**Traffic management:** Timeouts, retries, canary rollouts, 
-	**Security:** End-user Authentication and Authorization,
-	**Observability:** Tracing, monitoring and logging.

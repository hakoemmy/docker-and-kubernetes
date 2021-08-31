# docker-and-kubernates
> Setup docker and kubernetes cluster for node js app
# Useful resources

- [Docker and kubernetes with node js](https://www.digitalocean.com/community/tech_talks/how-to-deploy-a-resilient-node-js-application-on-kubernetes-from-scratch)
- [Kubernetes official site](https://kubernetes.io/)
- [Docker official site](https://www.docker.com/)
- [Digital ocean useful tutorials on docker, kubernetes and node js](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04)
- [Book: From containers to kubernetes](https://assets.digitalocean.com/books/from-containers-to-kubernetes-with-nodejs.pdf)
- [Kubernetes API reference](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.20/)
- [Kubernetes pod lifecyles](https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle/#:~:text=in%20that%20state.-,Running,container%20entered%20the%20Running%20state.)
[Intereactive kubernetes cluster](https://kubernetes.io/docs/tutorials/kubernetes-basics/update/update-interactive/)


# Useful commands

1. Docker

- Build an image from a Dockerfile with extra dot that means current dir: ```docker build -t tag-name .```
- Show docker builds: ``` docker images```
- SHow current running containers: ``` docker ps```
- Login to docker: ```docker login```
- Publish the container to docker hub: ```docker push tag-name```
- Tag or rename an image: ```docker tag old-container-tag hakoemmy/new-container-tag```
- Remove a docker image: ``` docker rmi docker-tag-name```
- Stop a docker image: ```docker stop image-id```
- Tag a version to docker repo: ```docker tag ${image_id} docker.io/${login_name}/${image_name} ```


and many more [here](https://docs.docker.com/engine/reference/commandline/docker/)

# Hosting

- You can access the container hosted on docker hub: [Link](https://hub.docker.com/repository/docker/hakoemmy/docker-and-kubernates)

2. Kubernetes

- Create a kubernete cluster: ```kubectl apply -f deployment.yaml```
- Get deployments: ``` kubectl get deployments```
- Get running pods: ```kubectl get pods```
- Delete a pod: ```kubectl delete pod pod-name ``
- Know more about the pod: ```kubectl describe pod pod-name```
- Get pod logs: ```kubectl logs pod-name```
- Get IP for load balancer: ```kubectl get svc```
- Tunnel loadBalancer to an external IP when you are on local machine: ```minikube tunnel```
- Check minikube status: ```minikube status```
- Remove pods from cluster: ```kubectl delete -f .yaml folder or file```
- Rolling out an update or rollback to a specific image: Run ```kubectl set image deployments/my-deployment mycontainer=myimage:tag-name```
- Check the roll out status: ```kubectl rollout status deployment/deployment-name```
- Describe deployment: ```kubectl describe deployments/deployment-name```
- Revert back deployment to the previous known version when you hit (ImagePullBackOff status): ```kubectl rollout undo deployments/deployment-name```

More on [kubernetes cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

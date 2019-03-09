###So it's not exactly smooth starting....
###Steps to run:
####1. use docker compose 
```javascript
docker-compose up --build
```
####2. Restart nginx container singley (If homepage does not render)
####3. Possibly need to restart api container also (if no "Indexes I have seen" values show)

If you get some weird shitty errors from nginx, restart docker desktop and do another compose down & up 
(you might then still have to restart nginx container)


##Minikube commands
####startup
Note this guide was taken from [here](https://medium.com/@JockDaRock/minikube-on-windows-10-with-hyper-v-6ef0f4dc158c)
1. Launch powershell with admin rights
2. run:
```
minikube start --vm-driver hyperv --hyperv-virtual-switch "Primary Virtual Switch"
```
####shutdown
```
minikube ssh
$ sudo poweroff 
```
Note that minikube stop does not work due to an issue [here](https://github.com/kubernetes/minikube/issues/2914)
####Dashboard
```
minikube dashboard
```
####Use docker ps command within minikube
```
minikube docker-env | Invoke-Expression
``` 
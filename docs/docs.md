<!-- Set up kubernetes -->

brew install kubeclt
install virtualbox
brew cask install minikube
minikube start
minikube status
kubectl cluster-info

<!-- Running containers -->

kubectl apply -f <filename>

<!-- Print teh status of all running pods -->

kubectl get pods
kubectl get services

<!-- details of object -->

kubectl describe <object-type> <object-name>

<!-- delete an instace -->

kubectl delete -f <object-file>

<!-- imperative command to update image -->

kubectl set image <object-type>/<object-name> <container-name> = <new-image-to-use>

example:
kubectl set image deployment/client-deployment client=rafaelsanzio/multi-client:v5

https://www.magalix.com/blog/deploy-react-app-to-kubernetes-cluster
docker prune and kubernetes restart
npx create-react-app hello
cd hello
npm start
npm  run-script build
Created both nginx and node dockerfiles
docker build -f Dockerfile.nginx -t hello .
kubectl config use-context docker-desktop
kubectl get nodes
kubectl cluster-info
docker run -d -p 5000:5000 --restart=always --name hello registry:2

## Simple Kubernetes demo application for testing pipelines

Publically available repo so I don't need to use any authentication to access it.  

Uses a container with a small executable I wrote using Rust that responds to requests on port 80 with a simple html page. The background colour and some of the content can be changed in the manifest file.  

The code for the executable is in another repo, but it is nothing advanced. The container itself is on Dockerhub and publically available; details are in the manifest file.   

Updating the manifest file and checking it in updates the git repo, which can be used to trigger whatever pipeline is being tested.  

The service is defined to use a load balancer, which is simplest to use as there's no mucking around with port forwarding or whatever.  

Currently being used for testing ArgoCD running on an AWS EKS cluster; does what I want it to.  Path value to be used with Argo is `stack`.

Todo:
- Security etc; haven't looked at that yet  

Useful command :
- `git add .&& git commit -m "Commit" && git push`



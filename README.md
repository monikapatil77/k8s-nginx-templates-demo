# k8s-nginx-templates-demo
nginx kubernetes deployment

### Kubernetes Up and Running
#### Four types of manifest files (declarative manifest)
- Pods
- ConfigMaps
- Services and Replica sets
- Deployments

## ToDo:
1. Create pod from cli or terminal - done
2. Create pod from yaml file - done
3. Create service from cli or terminal
4. Create service from yaml
5. Create deployments from cli or terminal
6. Create deployments from yaml
7. Create pods and deployments in custom namespace
8. Attach pods and deployments to non default namespace
9. Create pods and deployments in user defined network
10. Add livenessprobe, resource limit in pod manifest
11. Add health-check probe in pod manifest
12. Apply label, label-selector and annotations to pods, services and deployments
    - pods - done
    - services -
    - deployments -  


## Questions:
1. Manifest file vs Deployment descriptor
    - Manifest file - declare state of application.
      - Deployment configuration and server configuration will be managed by Kubernetes server.
      - For cluster environments
      - application state is managed by multiple containers as per declaration in manifest file.
    - Deployment descriptor - define web server configuration.
      - you need to define and manage web server configuration into xml files.
      - These configurations are used by web containers to initialize web containers.
      - One deployment descriptor per web container
      - For standalone servers not for clusters

2. kubectl run command to use local docker image and not from repository?
   kubectl run command to use non-official image from local dev environment



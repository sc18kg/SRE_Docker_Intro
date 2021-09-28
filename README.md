# Docker Introduction
## What is Docker
#### Advantages
- Docker is a popular evolving software with excellent community support and built for microservices
- It is lightweight when compared to VMs making it cost and resource effective
- It provides uniformity across development and production environments making it a suitable fit for building cloud-native applications
- It provides facilities for continuous integration and deployment
- Docker is not going anywhere; it provides integration with popular tools and services such as AWS, Microsoft Azure, Ansible, Kubernetes, Istio and lot more

### Installation of Docker
1. Head the the website () and select the `WSL 2 backend` option
2. Download and during set-up ensure `Enable WSL 2 Windows Configuration`
3. The install will  take a while and your device may need to be restarted
4. Once installed, open a Git bash terminal (as admin) and run the command `docker version`
5. Run `Docker Desktop` as admin, A promt for WSL 2 installation should appear
6. Follow the link and download the `WSL2 Linux kernel update package for x64 machines`
7. Create an account and sign into the desktop
8. Under `Settings -> Resources -> WSL Intergration` make sure `Enable intergration with my default WSL distro` is enabled
9. Run the command `Enable-WindowsOptionalFeature -Online -FeatureName $("VirtualMachinePlatform","Microsoft-Windows-Subsystem-Linux")`
10. After this run `Start-Service docker`, `net stop com.docker.service` then finally `net start com.docker.service`
11. Once complete we should have docker installed

### Check Docker is Working
1. Go to the Git bash terminal and run the command `docker pull hello-world` this checks the connection to the registry
2. If successful check your images by running `docker images`
3. Now you have listed your images, you can run the ones available so run `docker run hello-world`
4. If you see the screen below, Congratulations you can finished and verified the installation.


## Microservices
![micro](![image](https://user-images.githubusercontent.com/74776086/135053106-1da1883f-c57c-494a-a73d-71a17a188f0e.png)
### Advantages
- Introduces the philosophy of Separation of Concerns and ensures Agile Development of software applications in both simple and complex domains
- The standalone ability or independent nature of microservices open doors for following benefits:
- Reduces complexity by allowing developers to break into small teams, each of which builds/maintains one or more services
- Reduces risk by allowing deployment in chunks rather than rebuilding the whole application for every change
- Easy maintenance by allowing flexibility to incrementally update/upgrade the technology stack for one or more services, rather than the entire application in a single point in time
- In addition to giving you the flexibility to build services in any language, thereby making it language independent, it also allows you to maintain separate data models of each of the given services
- You can build a fully automated deployment mechanism for ensuring individual service deployments, service management and autoscaling of the application

## Comparison
Although VMs made software more accessible to maintain and drastically reduced costs, more optimization was still possible. For instance, not all applications would behave as expected in a guest OS environment. Additionally, the guest OS would require a lot of resources for even running simple processes.

These problems led to the next innovation: containerization. Unlike virtual machines which were more operating system specific, containers are application specific, making them far lighter. Furthermore, VMs can run multiple processes whereas a container runs as a single process. This leads us to two things:

You can run multiple containers on a physical machine, or you can even think of running it on a single VM. In either case, it solves your application related problems
Containerization is not in competition with Virtualization, but rather a complementary factor to further optimize your IT software infrastructure
![comparison](https://images.ctfassets.net/h6vh38q7qvzk/2OwpgC3h6gAcqgUwiU688K/a128ef1f712cf25d8fc33031e443f87e/microservices-docker-image-four.png)

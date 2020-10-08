## Important Books

## Important Videos

## Important Reading
* https://docs.microsoft.com/en-us/dotnet/architecture/containerized-lifecycle/

## Concepts
Container image: A package with all the dependencies and information needed to create a container. An image includes all the dependencies plus deployment and execution configuration to be used by a container runtime. Images are immutable.

Dockerfile: A text file that contains instructions for building a Docker image.

Build: The action of building a container image based on the information and context provided by its Dockerfile.

Container: An instance of a Docker image. A container represents the execution of a single application, process, or service.

Volumes: A writable filesystem that the container can use. Images are read-only, but most programs need to write to the filesystem. Volumes live in the host system and are managed by Docker.

Tag: A mark or label you can apply to images so that different images can be identified.

Multi-stage Build: Is a feature, since Docker 17.05 or higher, that helps to reduce the size of the final images. 

Repository (repo): A collection of related Docker images, labeled with a tag that indicates the image version. 

Registry: A service that provides access to repositories. The default registry for most public images is Docker Hub (owned by Docker as an organization). 

Multi-arch image: For multi-architecture, it's a feature that simplifies the selection of the appropriate image, according to the platform where Docker is running.

Docker Hub: A public registry to upload images and work with them. Docker Hub provides Docker image hosting, public or private registries, build triggers and web hooks, and integration with GitHub and Bitbucket.

Azure Container Registry: A public resource for working with Docker images and its components in Azure. This provides a registry that's close to your deployments in Azure and that gives you control over access, making it possible to use your Azure Active Directory groups and permissions.

Docker Trusted Registry (DTR): A Docker registry service (from Docker) that can be installed on-premises so it lives within the organization's datacenter and network. It's convenient for private images that should be managed within the enterprise. Docker Trusted Registry is included as part of the Docker Datacenter product. For more information, see Docker Trusted Registry (DTR).

Docker Community Edition (CE): Development tools for Windows and macOS for building, running, and testing containers locally. Docker CE for Windows provides development environments for both Linux and Windows Containers. The Linux Docker host on Windows is based on a Hyper-V virtual machine. The host for Windows Containers is directly based on Windows. Docker CE for Mac is based on the Apple Hypervisor framework and the xhyve hypervisor, which provides a Linux Docker host virtual machine on Mac OS X. Docker CE for Windows and for Mac replaces Docker Toolbox, which was based on Oracle VirtualBox.

Docker Enterprise Edition (EE): An enterprise-scale version of Docker tools for Linux and Windows development.

Compose: A command-line tool and YAML file format with metadata for defining and running multi-container applications. You define a single application based on multiple images with one or more .yml files that can override values depending on the environment. After you've created the definitions, you can deploy the whole multi-container application with a single command (docker-compose up) that creates a container per image on the Docker host.

Cluster: A collection of Docker hosts exposed as if it were a single virtual Docker host, so that the application can scale to multiple instances of the services spread across multiple hosts within the cluster. Docker clusters can be created with Kubernetes, Azure Service Fabric, Docker Swarm and Mesosphere DC/OS.

Orchestrator: A tool that simplifies the management of clusters and Docker hosts. Orchestrators enable you to manage their images, containers, and hosts through a command-line interface (CLI) or a graphical UI. You can manage container networking, configurations, load balancing, service discovery, high availability, Docker host configuration, and more. An orchestrator is responsible for running, distributing, scaling, and healing workloads across a collection of nodes. Typically, orchestrator products are the same products that provide cluster infrastructure, like Kubernetes and Azure Service Fabric, among other offerings in the market.

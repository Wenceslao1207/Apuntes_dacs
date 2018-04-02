# Aplicaciones Cliente Servidor

## Contenidos

- Cliente pesado o Inteligente
	- Conceptos

- Clientes livianos o Web
 
- Conceptos de Tecnologias de intercambio de informacion entre cliente y servidor

- Java // .Net 

----

## 12 FActor applications

- Codebase: One codebase tracked in revision control, mant deplays
- Dependencies
- Config
- Backing Services
- Build, Release, Run
- Processes
- Port Binding
- Cocnurrency
- Disposability
- Dev/pro parity
- Logs
- Admin Processes

Code Base
- A code base is a single repo
- there is always a one to one correlation between the codebase and the app:
	- if tehre are multiple codebases, it's not an app - it's a distribuited system. Each  component in a distribuited system is an app, and each can individually comply with twelve-factor.
	- 

- Never relies on implicit existence of system0wide packages
- Declare all dependencies, completely and exactly, via dependency declaration manufest
- Use a dependecy isolation tool during execution to ensure that no implicit dependecis "leak in" from the surroundiing system. The full and explicit dependecy specification is applied uniformly to both production and development


Configs

- An app's config is everything that is likely to vary between deploys
	- Resources handles to the database. Memcached, and other backing services
	- Credentials to external services such as Amazon S3 or Twitter
- Note that this definition of "config" does not include internal application config
- The twelve-factor app stores config in enviorment variables
- In a twelve-factor app, envi vars are granular controls, each fully othogonal to other env vars.

Backing Services

- A backing service is any service tha app consumes over the network as part of it's normal operation
- The code for a twelve factor app makes no distinction between local and third party services.

Build, Release, Run

- A code base in transformed uno a (non-development) deplay through three stages
	- The build stafe ins tranform which converts a code repo into an excutable bundle known as a build. Using a version of ....



Processes
- Processes are stateless and share-nothing

Port Binding
- Web apps are sometimes executable inside webserver container
- The twelve-factor app is completely self-contained and does not rely on runtime injection of a webserver into teh executio enviorment to crate web facing-service
 

# Distributed Systems 

Collection of independent computers that appear to the users of the system as a single system
- Network of workstations
- Distribuited manufacturing system
- Network of branch office computers

### Concepts
- **A program**: is teh code you write
- **A process** is what you get when you run it
- **A message**: is used to communicate between processes 
- **A package**: is a fragment of a message that migth travel on wire
- **A protocol**: is a formal description of message formats andthe rules that two processes must follow in order to exchange those messages.
- **A network**: is the infrastructure that links computers, workstations, terminals, servers, etc. It consists  of routers whiich are connected by communication links.
- **A component**: can be a process or any piece of hardware requiered to run a process support communications between processes, store data, etc. // se vera mas adelante
- **A distributed System**: is an application that executes a collection of protocols to coordinate the actions of multiple processes on a network, such that all components cooperate together to perform a single or small set of related tasks.

### Why build a distributed system
- **Fault-Tolerant**: it can recover from component failures without performing incorrect actions
- **High Available**: it can restore operations, permitting it to resume providing services even when som component hace failed
- Recoverable: Failed components can restart themselves and rejoin the system, after the cause of failure has been repaired
- Scalable: it can operate correctly even as some aspect of the system is caled to a larger size. 

### 8 Fallacities of distribuited systems

- Network reliable
- Latency is zero
- Bandwith is infinite
- The network is secure
- Topology doesnt change
- There is one administrator
- Transport cost is zero
- The network is homogeneous

### Client-Server applications

- The server provides some service, such as processing database queries or sending out current stock prices.
- The client uses the service provided by the server, either displaying database query results to the user of making stock purchase recommendations to an investor.

### Cluster computing
- Cluster computing is used  for parallel programming in which a single program is run in parallel on multiple machines.
- Each cluster consists of a collection of compute nodes that are controlled and accessed by means of a single master node.
- The master typically handles the allocation of nodes to a particular parallel progrma, maintains a batch queue of submittef job, and provides an interface for the users of teh system

### Grid computing
- A characteristic feature of traditional cluster computing is its homogeneity.
- In a grid computinf no ssumptions are made concerning similarity of hardware, OS, Network, adminsitrative domains, security polices, etc.

### Cloud Computing 
- **Utility computing:** a customer could upload tasjs to a data center be charged on a per-resource basis.
- **Cloud computing** is characterized by an easily usable and acecessible pool of virtualized resources.
	- **infrastructure-as-aservice (IaaS)** covering hardware and infraestructure layer
	- **Platform-as-a-Service (Paas)** covering the platform layer
	- **Software-as-a-Service (SaaS)** in which the applications are covered

## IPC

**Inter Processes Communication**

Mutex
Semaphore
Critical Section


- SHARED MEMORY
P1 Writes P2 Reads. I can use Semaphore

-NAMED TIPES
PIPE!

- SOCKETS (Read more)
TCP/IP
Ip + port
+ = UDP or TCP


## COM / OLE

OLE ---> Reuse code 
    |--> Complements

Component Object Model  ---> Windows 95

    OLE = Object Linking and Embedding
    DDE = Dynamic Data Exchange
    COM = Component Object Model

OLE: This is a method of linking parts of one document to parts of another. For example, having a powerpoint slide with an Excel chart embedded into it. When the Excel spreadsheet is updated, the chart should update too. When you reopen Powerpoint, magically it has! (This example is a linked object). Embedded objects are the same only the excel spreadsheet doesn't exist in an external file, the data for the spreadsheet is contained within the powerpoint file.

You can embed Excel, Word and Powerpoint into each other with linked objects. Other applications were written specifically to support being embedded into Word, such as Microsoft Equation Editor.

OLE 1 was built on DDE, which used windows messages to notify applications when source data changed, and typically passed data around by using HGLOBAL global memory handles.

OLE 2 was built on COM.

COM is an language neutral, object-oriented component model and ABI based on DCE RPC. As an RPC system it supported remote calls between processes on the same machine, and later, with DCOM, on different machines. Initially COM was used as part of the architecture of MAPI (which uses the COM object model but not the COM registration services) before being formally launched on it's own as a general object model complete with registry and object activation and other services. (Monikers and structured storage for example).

OLE Automation has nothing to do with OLE - it's a branding connection only. OLE Automation is a visual-basic compatible subset of COM which supports basic datatypes only (for example no unsigned integers or structs) but including objects (COM interfaces).

OLE Controls however ARE related to OLE. They are visual components primarily targeted at Visual Basic users from VB 4 onwards, but the visual elements are provided using the embedding facilities of OLE 2. They can also be hosted (in theory, if properly written) by anything capable of hosting an OLE 2 embedded object, and were often used in C++ applications too. They typically use OLE Automation compatible interfaces for programming at runtime.

ActiveX control is a marketing term for COM objects, from the time when Microsoft were attempting to popularise the technology for extending web applications.

## JAVA!

Herencia vs Composicion

Herencia: CUando se queire rutilziar codigo dentro de una jerarquia de objetos, que puedan ser reutilizables despues.
COmposicion: Utilziar codigo.

Java ---> Lenguaje OO ----> Herencia Simple
			|-> Fuertemente Tipado
			|-> Multiplataforma
			|-> Compilado
			|-> Proposito Gerencial

JVM ---> Scala
    |--> Kotlin
    |--> Groovx	


MAVEN!
GRADEL!

App Server
- Servlet Engine  --- tomcat
- Application server ---- JBoss/wildfly

Continous integration Service Jenkins / Circle CI



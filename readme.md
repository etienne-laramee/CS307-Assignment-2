# Diagram Choices for the Smart Home Temperature Control System
For this assignment, I designed three types of **diagrams** to illustrate different views of a **Smart Home Temperature Control System**: *use case*, *sequence*, and *deployment*.
## 1. Use case diagram
### Definition:
A use case diagram illustrate the scope and interaction between actor and components for specific scenarios. Actors are usually human, but can also be a system. This kind of diagram shows what a system does but not how it does it.
### Importance and use
The importance of this kind of diagram is to convey in a simple to understand, high-level view, the interaction between the parts of the system for each represented scenario. It is commonly used early
### Justify design decisions
In this diagram I decided that the heating and cooling units are "smart", meaning they are managed by the control unit and not directly by the thermostats as in traditional "non-smart" systems. In a way, the thermostats are basically comprised of a simple temperature sensor and a user interface enabling the wireless configuration of the related heating/cooling device.
## 2. Sequence diagram
### Definition:
A sequence diagram shows how actors and components interact within a scenario in time. This enables us to have a view that is easy to understand of the order in which actions occur within the system and which components are involved.
### Importance and use
Sequence diagrams are useful to visualize the flow of a system and they are often used in software systems design.
### Justify design decisions
In my sequence diagram I chose to illustrate the "smart appliance" discussed in the use case diagram, notably the interaction with the thermostat being an interface for the control unit versus the traditional serial temperature control.

I also chose to illustrate the temperature sensor update loop between the control unit and the thermostats.

Finally I chose to emphasize the operation of the heating/cooling unit being solely controlled by the control unit in a loop, according to the user defined schedule.
## 3. Deployment diagram
### Definition:
The deployment diagram depicts the relation of the software with the hardware systems and devices and the relationship between each other. Their relationships also indicate the protocols used to communicate.
### Importance and use
The deployment diagrams provide important information about which software is being deployed to which physical system. It enforces in a way the scope of the system being deployed.

A common use for deployment diagrams is for the scaling of parts or a whole application. A web app for example could have a performance bottleneck at the data retrieval point. A deployment diagram will illustrate visually this bottleneck and make it easier for engineers to alter this model and visualize potential solutions.
### Justify design decisions
I chose to depict the heating and cooling devices as a subset of "Compatible Smart Devices" that interact with the control unit, differentiating them form traditional in-line appliances that are controlled directly by the thermostat.

I also represented the input endpoints where the user interacts with the system, being the mobile app, web "self serve" portal and each individual thermostats.

I chose to let the web-facing customer portal have access only to modify the self hosted configurations database residing on the customer's control unit and let that control unit pull its configurations consistently from that database to keep it somewhat independent instead of the portal having a direct influence on the controller, making the design more modular and separating concerns.

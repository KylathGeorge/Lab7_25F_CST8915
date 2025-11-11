# CST8915: Lab 7

## Name: Kylath Mamman George

## Student Number: 041198835

### Youtube Link

[Lab 7 Youtube Link](https://www.youtube.com/watch?v=4129R8SWdnI)

**1. Whether RabbitMQ is a stateless or stateful application.**

- RabbitMQ is a stateless application in this YAML file as it has no persistent storage.

**2. The implications of running RabbitMQ without persistent storage.**

- The data is currently stored inside the containers temporary filesystem, since there is no volume mounted. This data includes queues and messages, users etc. and all this data could be lost at any time.

**3. What happens when the RabbitMQ pod is deleted or restarted?**

- The filesystem will no longer exist or a new one is created so all the data stored previously disappears and is lost.

**4. Potential solutions to this problem (research-based).**

- From my research, if we wanted to solve this ourselves, a persistentVolumeClaim kind can be added to the YAML file and it can be mounted to the RabbitMQ deployment. Otherwise using a fully managed service should solve this issue.

**5. Does using Azure Service Bus solve the issues identified with RabbitMQ Configuration in this Lab?**

- Yes, Azure Service Bus solves these issues as it is a fully managed message broker where the peristent storage, credentials, scaling etc is all fully handled by Azure. Currently we are configuring everything and handling the deployment and managing the broker ourselves.

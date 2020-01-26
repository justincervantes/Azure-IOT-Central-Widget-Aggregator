# Azure-IOT-Central-Widget-Aggregator
Microsoft's​ Azure IoT Central is a fully managed SaaS (software-as-a-service) solution that removes the need for cloud solution expertise and makes it easy to connect, monitor and manage your IoT assets at scale.

Though IOT Central is a great service to quickly get started and visualize data, it does not work to visualize data across multiple IOT devices. A particular situation that I came across was building a fleet management system dashboard; I wanted a widget that would show the total kilometers travelled in a given day by my fleet. Currently, IOT Central has a one-to-one relationship between IOT devices connected to the platform and widgets that it can visualize. 

This node.js application is a service which queries Azure's CosmosDB service (which can be connected to your IOT Central app), aggregates payloads from different devices, and pretends to be a new device, thus enabling a user to have a widget which shows aggregated data.

In order to run this program, you must have Node.js installed on your local machine.
Download information can be found here: https://nodejs.org/en/download/

From the current directory, run the following commands in your preferred CLI:
npm install - this installs all the dependencies required to run this node service
node app.js - runs the program

Disclaimer: The database URI and access key specified in config.js will have changed since the time of document posting. The connection string to a given IoT Central will also have changed. These have been left as a demonstration of what to look for when replacing your own service's connection details. If deploying a similar service, and are looking for templates, I have commented each section where the user ought to replace their connection values.

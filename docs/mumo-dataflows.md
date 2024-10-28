# MuMo Dataflows

Repository for the Museum Monitoring tool project.
In the Museum Monitoring project, incoming sensor data (coming from the Things Network) is mapped into sosa compliant sensor observations.
The observations are published in a LDES that uses smart fragmentations to leverage the usage of [Solid Web Access Control](https://solidproject.org/TR/wac).

Sensor information is also published in a LDES, using a similar fragmentation.
Information about sensors is harvested from a Omeka-s instance.

The pipeline used to create these LDES can be found on [github](https://github.com/ajuvercr/mumo-pipeline), this repository also contains a configuration to start the LDES-Solid-Server to handle publish the created LDESes on the web.


# Dashboard

A dashboard component was built to visualize the stream of observations.
There are 2 version of the dashboard, the old one that didn't take solic into account and on that does.

Link to [github](https://github.com/ajuvercr/mumo-graphs).

## version 1

Version 1 doesn't take solid into account, but only worked with a tiny portion of the data.
It did allow for creating custom graphs that show multiple nodes in the same graph (use editable).

![image](https://github.com/user-attachments/assets/12d5c5bb-14b1-4e1b-86d0-b2b3880d97e0)


## version 2 (work in progress)

Version 2 is more advanced, showing the latests measurements of all nodes that the currently logged in user has access to.
It will also support a page per node that shows the flow of observation for that node.

![image](https://github.com/user-attachments/assets/b420c312-b65e-4815-9637-a8286e613701)
![image](https://github.com/user-attachments/assets/5c08682c-fd75-4bd8-9173-8026c6d3ffd0)


# Authorization

To manage the authrozation of each node, a custom version of [Loama](https://github.com/SolidLabResearch/loama) was deployed locally.
Merging these changes back into the original repository is still todo.

![image](https://github.com/user-attachments/assets/c28f3ac3-d631-47da-a928-56f9615d86ec)

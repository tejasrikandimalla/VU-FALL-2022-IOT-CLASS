Software setup to run on IOT Platform Install:

STEP 1:

1.	Connect Laptop to router and Raspberry pi, make sure Diet pi installed in the raspberry Pi.

STEP 2:

1.	Login to Raspberry pi using Diet pi user credentials in command prompt 
2.	Ssh diepi@[IP_ADDRESS_OF_Raspberry_Pi]

STEP 3:

1.	Select for “Search Software” and using arrows in keyboard to click “ok” and press “enter”.

STEP 4:

1.	Search for “mqtt” and click "ok”, then click the space bar to select the “123 mqtt” option. 
2.	Cross check the * is present next to the software selected.
3.	Search for “node-red” and click "ok”, then click the space bar to select the “122 Node-red:tool” option. 
4.	Search for postgress and select “194 PostgreSQL” by clicking the space bar. Next click ok.
5.	After the software search is completed, for installing software option click “ok”
6.	The installation takes few minutes

![Screenshot 2022-09-18 163910](https://user-images.githubusercontent.com/112652553/191425867-4a52c47a-bd65-493a-affb-caf96b494c22.png)

STEP 5:

POSTGRES Running:

1.	Run “sudo su prostgress” command in the command prompt’s pi ssh session
2.	Create a user using command “createuser pi -P –interactive”
3.	Then enter password for progress account.
4.	Select n for superuser and y for next two questions
5.	Connect to shell of progress using “psql” and create a test database “create database test” commads respectively.
6.	Exit from the psql shell and Postgres user using ctrl+D for two times.
7.	Enter the following commands to create a table and populate it
8.	Enter the command below to get created table as output

![Screenshot 2022-09-18 165159](https://user-images.githubusercontent.com/112652553/191425409-0d552246-ed09-4ff3-8da1-1a41e2fd8f90.png)

NODE-RED:

1.	Connecting the node-red to check it is working with the raspberry pi {IP_ADDRESS}
 
![Screenshot 2022-09-18 165355](https://user-images.githubusercontent.com/112652553/191425792-cc04edee-f68c-411e-9c74-b4e1a6658e4f.png)

2.	Enter “npm install node-red-contrib-re-postgres” to install it 
3.	Enter “dietpi-services restart node-red” to restart node-red
4.	Check the browser for node-red tab and go to manage pallet 
5.	Search for “install node-red-contrib-postgresql”
6.	Left we can search for node tags
7.	Pull a postgres node into a flow from search bar and pull it in interface of graph
8.	Pull trigger, template, postgres, and debug to get them aligned

![Screenshot 2022-09-18 165908](https://user-images.githubusercontent.com/112652553/191425353-0621dfa0-4424-48fe-9cb3-badea0e8ee2a.png)

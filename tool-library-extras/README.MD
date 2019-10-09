front end URL:https://toolbox-client-git-master.teamredpanda.now.sh/

## Setting up the database locally

### Create user
  * In your terminal with postgresql and psql installed, use the following script
    `createuser -Pw --interactive`
    username = ct-admin
    no password
    y for a superuser
  
### Create database
  * In your terminal, type the follwing command:
    `createdb community-toolbox --owner=ct-admin`

### Create the tables
  * In your terminal, change directory to the Tool-Library-Server and create the tables by running the following script: 
    `npm run migrate`

### Seed the database
  * In your terminal, run the following command: 
    `psql -U ct-admin -d community-toolbox -f ./seeds/seed.tools.sql`
    
    #### Front end deployment at https://tool-library-client.jeaninehoffman.now.sh/
    

## Environment Variables
* File .env should be copied into the server's root folder (toolbox-server). This file contains variables related to our databases
* File client-example.env should be copied into the client's folder (toolbox-client) and renamed to _.env_ The environment variable _REACT_APP_MAPS_API_KEY_ allows the app to embed a Google Map.

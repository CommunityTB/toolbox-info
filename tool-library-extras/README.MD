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

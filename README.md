# node-boilerplate

## Running the project

1. Be sure you have **docker/docker-compose** and **yarn** (or **npm**, if you use it) installed.
2. Clone the repository by running

```bash
git clone https://github.com/CITi-UFPE/node-boilerplate.git
```

3. Install all the dependencies by running

```bash
yarn install
# or
npm install
```

4. Create a **.env** file and copy the following content to it:

```dotenv
# ###### SERVER SETTINGS #######
SERVER_PORT=3001

DATABASE_HOST=localhost
DATABASE_USER=root
DATABASE_PASSWORD=YOUR_PASSWORD
DATABASE_PORT=3306
DATABASE_DB=quivi_db
DATABASE_TYPE=mysql

DATABASE_URL=${DATABASE_TYPE}://${DATABASE_USER}:${DATABASE_PASSWORD}@${DATABASE_HOST}:${DATABASE_PORT}/${DATABASE_DB}
```

5. Run the mysql docker container

```bash
docker-compose up
```

6. Run the migrations

```bash
yarn migration
```

7. Run the development server locally

```bash
yarn dev
```

8. Now the server should be running!

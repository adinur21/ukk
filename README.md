# Usage

Please first install node and other packages on your instances.

https://linuxize.com/post/how-to-install-node-js-on-ubuntu-22-04/  --> Install node and npm

Click Use this api and then create new repository

Install `node_modules` on this project

```bash
  npm Install

  # use yarn
  yarn
```

https://expressjs.com/en/starter/installing.html  --> Install express

https://www.npmjs.com/package/nodemon  --> Install nodemon

https://www.thelinuxfaq.com/npm/npm-packages/cors#:~:text=%24%20sudo%20npm%20install%20cors%20%24%20sudo%20npm,command%20as%20below%2C%20%24%20sudo%20npm%20update%20cors  -->> Install cors

https://www.thelinuxfaq.com/npm/npm-packages/body-parser  --> Install body parser


After that, you can setup the database. go to dir model and edit `dbConnection.js`.

```bash
const db = mySql.createPool({
  host: "localhost",
  user: "root",
  password: "",
  database: "cloud_api"
})
```

Run the project

```bash
  npm run start

  # use yarn
  yarn start
```

# API Spec

## Get all guru

Request :

- Method : GET
- Endpoint : `/api/guru/v1`
- Header :
  - Content-Type: application/json
  - Accept: application/json

Response :

```json
{
  "guru": [
    {
      "id_guru": "number",
      "nama_guru": "string",
      "mapel_guru": "string",
      "sekolah_guru": "string"
    }
  ],
  "message": "string"
}
```

## Get guru by id

Request :

- Method : GET
- Endpoint : `/api/guru/v1/{id_guru}`
- Header :
  - Content-Type: application/json
  - Accept: application/json

Response :

```json
{
  "guru": {
    "id_guru": "number",
    "nama_guru": "string",
    "mapel_guru": "string",
    "sekolah_guru": "string"
  },
  "message": "string"
}
```

## Create guru

Request :

- Method : POST
- Endpoint : `/api/guru/v1/create`
- Header :
  - Content-Type: application/json
  - Accept: application/json
- Body :

```json
{
  "nama_guru": "string",
  "mapel_guru": "string",
  "sekolah_guru": "string"
}
```

Response :

```json
{
  "data": {
    "id_guru": "number",
    "nama_guru": "string",
    "mapel_guru": "string",
    "sekolah_guru": "string"
  },
  "message": "string"
}
```

## Update guru

Request :

- Method : PUT
- Endpoint : `/api/guru/v1/{id_guru}/update`
- Header :
  - Content-Type: application/json
  - Accept: application/json
- Body :

```json
{
  "nama_guru": "string",
  "mapel_guru": "string",
  "sekolah_guru": "string"
}
```

Response :

```json
{
  "data": {
    "id_guru": "number",
    "nama_guru": "string",
    "mapel_guru": "string",
    "sekolah_guru": "string"
  },
  "message": "string"
}
```

## Delete guru

Request :

- Method : DELETE
- Endpoint : `/api/guru/v1/{id_guru}`
- Header :
  - Content-Type: application/json
  - Accept: application/json

Response :

```json
{
  "message": "string"
}
```

## Thanks to Authors

- [@setyawannn](https://www.github.com/setyawannn)
- [@kkafi09](https://www.github.com/kkafi09)

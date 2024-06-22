## GoBank - Simple Golang API

**Introduction**

This is a simple API developed in Golang using PostgreSQL as the database. It provides endpoints for creating accounts, logging in, retrieving all accounts, and retrieving specific accounts by ID.

**Prerequisites**

To run this API, you will need the following:

* Golang installed on your system
* PostgreSQL database
* A `.env` file with the following environment variables:
    * `DB_USER`: Your PostgreSQL username
    * `DB_NAME`: Your PostgreSQL database name
    * `DB_PASS`: Your PostgreSQL password
    * `DB_SSL_MODE`: Set to `disable` or `require` depending on your PostgreSQL configuration
    * `JWT_SECRET`: A secret key for generating JSON Web Tokens (JWTs)

**Database Setup**

If you do not have an existing PostgreSQL database, you can use the Docker Compose file provided in the root directory to create one.

```bash
docker-compose up -d
```

**Running the API**

To run the API, execute the following command:

```bash
go build -o bin/gobank && ./bin/gobank
```

**API Endpoints**

| Endpoint | Method | Description |
|---|---|---|
| `/account` | `POST` | Create a new account |
| `/login` | `POST` | Login to an existing account |
| `/account` | `GET` | Retrieve all accounts |
| `/account/{id}` | `GET` | Retrieve an account by ID |
| `/account/{accountNumber}` | `GET` | Retrieve an account by account number |
| `/account/{id}` | `DELETE` | Delete an account by ID |

**Creating an Account**

To create a new account, send a POST request to the `/account` endpoint with the following JSON body:

```json
{
  "firstName": "John",
  "lastName": "Doe",
  "password": "password123"
}
```

**Logging In**

To log in to an existing account, send a POST request to the `/login` endpoint with the following JSON body:

```json
{
  "number": "123",
  "password": "password123"
}
```

**Retrieving All Accounts**

To retrieve all accounts, send a GET request to the `/account` endpoint.

**Retrieving an Account by ID**

To retrieve an account by ID, send a GET request to the `/account/{id}` endpoint, replacing `{id}` with the ID of the account you want to retrieve.

**Deleting an Account by ID**

To delete an account by ID, send a DELETE request to the `/account/{id}` endpoint, replacing `{id}` with the ID of the account you want to retrieve.

**Additional Notes**

* This project is based on the tutorial "Complete JSON API project in Golang (JWT, Postgres, and Docker)" by Anthony GG ([[Tutorial Link]](https://youtube.com/playlist?list=PL0xRBLFXXsP6nudFDqMXzrvQCZrxSOm-2&si=qUAvjtA1pGrqvq0B)).
* The API is currently in development and may undergo changes in the future.
* Please report any bugs or issues you encounter to the project maintainers.

**Contributing**

We welcome contributions to this project. If you are interested in contributing, please open a PR with the changes.

**License**

This project is licensed under the MIT License. For more information, please see the LICENSE file.


PLAY ALL
Complete JSON API project in Golang (JWT, Postgres, and Docker)
Anthony GG
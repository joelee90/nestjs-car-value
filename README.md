## Description

Used Cars Value API

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## API Design

| API                                                  |  Method and Route  |                        Body of Query String                        |                                     Description |
| ---------------------------------------------------- | :----------------: | :----------------------------------------------------------------: | ----------------------------------------------: |
| Sign up with email and password.                     | POST /auth/signup  |                     Body - { email, password}                      |                  Create a new user and sign in. |
|                                                      | POST /auth/signin  |                     Body - { email, password}                      |                    Sign in as an existing user. |
| Worth estimate based on the make/model/year/mileage. |    GET /reports    |       QS - make, model, year, mileage, longtitude, latitude        |             Get an estimate for the cars value. |
| Report what users sold their vehicles for.           |   POST /reports    | Body - { make, model, year, mileage, longtitude, latitude, price } |             Report how much a vehicle sold for. |
| Admins approval for reported sales.                  | PATCH /reports/:id |                        Body - { approved }                         | Approve or reject a report submitted by a user. |

## Module Design

| Module             |    Controllers     |     Services     |         Repositories |
| ------------------ | :----------------: | :--------------: | -------------------: |
| **Users Module**   |                    |
|                    |  Users Controller  |  Users Services  |   Users Repositories |
| **Reports Module** |                    |
|                    | Reports Controller | Reports Services | Reports Repositories |

## License

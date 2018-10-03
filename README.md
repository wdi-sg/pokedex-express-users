# Pokedex Express - Many-to-Many

## Getting Started

1.  Fork and clone this repository to your computer
2.  Run `npm install` to install dependencies
3.  Create a new Postgres database by running `createdb pokemons -U <your_username>`
4.  Run `psql -U <your_username> -d pokemons -a -f tables.sql` to create a `pokemon` table in the database
5.  Look in the starter file called `index.js`, run `nodemon` to start local server on port 3000
6.  Open `localhost:3000` on your browser and see the home page

## Deliverables

The deliverable is an app that has CRUD functionality on pokemons that can be associated with users. Some example code from the previous version of the exercise has been provided for you to build on, although you may extend your own code from the previous exercise if you wish to do so.

* Create the relevant `tables.sql` file to create the appropriate table for your database

* seed your DB with the `pokedex.sql` file

* Create the association where a user can *catch* a pokemon. Users can catch many pokemon, and pokemon can be caught by many users. (this is a many-to-many relationship that must use a join table).
  - start with the simplest implementation of this feature- simply create a form that has a field for each id for each column of the join table
  - then, on the show route of the user (`/users/1`) write a query that will allow you to:
    - show what pokemon a user has captured

#### Further
* For a route showing a single user (`/users/1`). Add a form to this page that uses a `select` (drop down) to select a pokemon that was captured.

#### Further
On the show route of the pokemon, write a query that will allow you to:

- show what users have captured that pokemon
- add a form that will let users select a user that has captured that pokemon

#### Further

* DELETE `/pokemon/:id` should delete the entry of the pokemon with the specified ID, and should redirect to the home page `/`

* Create new routes for editing a user and deleting a user.

#### Further
If the user enters a pokemon to capture that has already been captured by the user, show an error.

#### Further

* Add a types table and a pokemontypes table in your database, and create a seed.sql file inserting relevant data for these 2 tables. Note that a pokemon can have many types, and a type can have many pokemons.

## Useful SQL commands

Note the proceeding commands should be run in a `psql` session on Terminal.

View all the data in a table:
```sql
SELECT * FROM pokemon;
```

Delete your database and start again if you made a mistake:
```sql
DROP DATABASE pokemons;
```

Or if you just need to reset the table:
```sql
DROP TABLE pokemons;
```

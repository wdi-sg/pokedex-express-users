# pokedex user login

Create a user login system for your pokemon.

Add a password column, hash the password and store it in the database. Set a cookie so that you know that the user has logged in.

When the user attempts to log in, hash then check that hash against what you have stored in the db.

#### How to start:
Start by simply adding the new column to the db. Then add the new form input to the registration form. Stop and make sure you can store a plain text password in the db.

Move on to setting the cookie. Set the cookie in the response of the registration. Make a new `GET` route that tests the cookie.

Move on to create a logout route that uses `response.clearCookie`.

Then, create user login. First, create a form that contains all the information we need to log a user in.

Now, we can create a `POST` route that accepts the request made by the form. Query for the user. When you have the user, hash the value that is coming in from the request. Compare this value against what is in the db. If the values match, set a cookie.

#### Further
Add the logic that a user is created and then they can go to any pokemon `/pokemon/2` and capture that pokemon. Restrict the user from capturing pokemon for any other user. *Hint: when the user logs in / registers, you can set another cookie with their user id. Then you can use this user id when they request to capture a pokemon.*

#### Further
If the user goes to their own page ( they are user id 1 ) let them release a pokemon they have captured (delete a row of the join table).
If the user goes to another users page, don't show them the form that lets them delete.

#### Further
Polish up your pokedex using bootstrap. Add in the features we have had in the other apps- sorting, etc.

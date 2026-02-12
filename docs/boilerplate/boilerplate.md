## Boilerplate Notes

## app.py (notes)

# Creating app function
> Load environment variables
> Create flask app specifying static and templates folders. 
> Set flask config variables from the environment variables we loaded (secret key, uploads folder, maximum content length if we are doing file uploading, session cookie settings (http only)
> Ensure that our uploads directory isn't nil by using os makedirs with exist_ok set to true.
> Initialize database (import this function from our database.py)
> Register flask route blueprints 
> Set up flask error handlers (404 (always this), and 413 (file too large) if we are doing file uploads)

# Entry point
> Call the creating app function from app.py entry point and then run the application

## database.py (notes)

# Getting database function
> Connect to SQLite
> Turn on row factory (ease of use and clarity)
> Force foreign key enforcement (to prevent us entering foreign keys that do not exist anywhere as a private key)
> Return the connection to be used elsewhere

# Initializing database function
> Get the database with the previously created function and save it as a variable
> Get the database cursor from our database.
> Create all our default tables, make sure to use IF NOT EXISTS or data will be overwritten on every app startup.
> Commit changes using our database variable
> Close the connection using our database variable



##How to contribute to this project 

1. Fork the project & clone locally.
2. Create an upstream remote and sync your local copy before you branch.
3. Import the local files to a current, stand-alone version of Postman and edit the collection in the application.
4. If adding new requests, only use inherited authentication, as CMS does not need different users and has no 
unauthenticated API.
5. Use only the variables already in the environment. They should cover every variable in the API. 
If more are needed, open an issue on github.
6. Include all arguments for a request you are editing, whether POST/PUT (in Body) or GET (in Params)
    *  only "checkmark" arguments that are required
    * for value use variables (only from those defined in the environment file), 
    ex:`{{variableName}}` where relevant
    * otherwise enter the expected type for value (ex: `String` or `Number`)
    * enter specific value if there is a default setting
    * copy description from the API documentation into field description
7. If needed edit the collection's description 
8. After editing, commit with a good commit message and push to your origin repository.
9. Create a new PR in Github 

For any issues not covered here feel free to create an issue on github.
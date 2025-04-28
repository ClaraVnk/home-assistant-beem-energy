This is based on @nicolinuxfr 's work (available on Gitlab https://gitlab.macg.io/-/snippets/34)

1) Create the beem.yaml file :
- Create a new file named beem.yaml in the main folder of your Home Assistant.
- Modify the line 51 with your email and password from your Beem Energy account.

2) Modify the configuration.yaml file :
- Add the lines to your configuration.yaml file.
- ⚠ Do not create a new line "home assistant" or "packages" if they already exist, just add the beem package.
  
3) Curl your Token :
- Open a terminal and type :
```
 curl https://api-x.beem.energy/beemapp/user/login -X POST -H "Content-Type: application/json" --data-raw '{"email":"YOUR_EMAIL","password":"YOUR_PASSWORD"}'
```

- Copy the token : "accessToken":"YOUR_ACCESS_TOKEN"
- In the file secrets.yaml add the lines for your token

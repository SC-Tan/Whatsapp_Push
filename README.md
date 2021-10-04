# Whatsapp_Push

<br>
This is the only simplest action that I can find in market place which I understand and replicate using the Github<br>

<h1 align="Left">Whatsapp Push Notification�</h1>

This github action which sends a Whatsapp notification when a change is pushed to a repository.

### How does it work?
1. Sign up for an account in twilio [here](https://www.twilio.com/).  
2. Obtain Account Sid and Auth Token from the dashboard.
3. For encryption, create new secrets in your repository named ```account_sid, auth_token, to_whatsapp_no``` and give their values from the dashboard.  
4. Create a ```.github/workflows/Whatsapps.yml```.  
5. Add the following properties to ```Whatsapps.yml``` file   

```name: When any change is made in the master branch, a message is sent to the Whatsapp. (see image on whatsapp below)

on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: whatsapp-notify
   
        env:
          account_sid: ${{ secrets.ACCOUNT_SID }}
          auth_token: ${{ secrets.AUTH_TOKEN }}
          to_whatsapp_no: ${{ secrets.TO_WHATSAPP_NO }}
        uses: SC-Tan/Whatsapp_Push@main
      - name : Run
        run: echo 'Start!'
```

## This is the image of a successful action in Github

<img src="Apps Photo.png" width="200">



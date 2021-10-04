# Twiliotest 

My DevOps project journey!!<br>
With the initial ideas of Github pages to creating CVs to lifestyle blogs to Docker Containers to so on and so forth..<br>
I have finally landed myself on Twilio cos it's so fun to explore!<br>I would have hope to stumble upon this way earlier so I can have more time to experiment it!<br> 
And here we go to some contributing guides to Twilio!!<br>

<h1 align="center">Setting Up Whatsapp Push Notification🚀</h1>
A github action which sends a Whatsapp notification when a change is pushed to a repository.

### Getting Started!
1. Create an account in twilio [here](https://www.twilio.com/).  
2. From your twilio dashboard fetch Account Sid and Auth Token.  
3. To encrypt them, create new secrets in your repository named ```account_sid, auth_token, to_whatsapp_no``` and give it's value.  
4. Create a ```.github/workflows/Whatsapps.yml```.  
5. Add the following properties to ```Whatsapps.yml``` file   

```name: When one of the following events occur in the master branch, a message is sent to the Whatsapp.
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
        uses: Cindywoo11/Twiliotest@main
      - name : Run
        run: echo 'Start!'
```

# Whatsapp Push Notification Output :house_with_garden:
### All Ready To Receive A Whatsapp Notification!
1. Make changes in your Github repository and commit the changes.  
2. From your "Actions" you can see the workflow running and Twilio will send notfication to your Whatsapp when a change is made. 

<img src="Apps Photo.png" width="200">

## 📝 Reference

https://github.com/kaviadigdarshan/whatsapp-actions
***

( TEST TEST )

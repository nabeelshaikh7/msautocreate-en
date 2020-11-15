# Use cloudflare workers to create a Microsoft global sub-number
# demo: https://m.ur.workers.dev/


1 Enter azure AD to create a new app, get tenant id and client id
![image.png](https://i.loli.net/2020/01/26/57GcEDYlQFTOMBL.png)

2.Authorize the app, the permission is Directory.ReadWrite.All of graph
![image.png](https://res.cloudinary.com/image-cdn-78/image/upload/v1605445897/idcreation_vpdqmc.png)

3Create a new client secret
![image.png](https://res.cloudinary.com/image-cdn-78/image/upload/v1605446054/client_secret_khqfox.png)

4 Get subscribed skuid, thanks @tanst for providing the method
> In Microsoft 365 admin center management panel-billing-license
> Then click the "license" you want to see, there is skuid in the address bar了



5 Configure reCAPTCHA, go to https://www.google.com/recaptcha/intro/v3.html to create a new reCAPTCHA v2 checkbox verification, fill in your domain name, and get the site key and secret 
![image.png](https://res.cloudinary.com/image-cdn-78/image/upload/v1605446131/recaptcha_abgwi3.png)



6 Copy the content in index.js to cf workers and fill in the corresponding data


(the original author is [Byg zayabighead](https://github.com/zayabighead/msautocreate). The original repository is : [msautocreate](https://github.com/365a1/msautocreate).)

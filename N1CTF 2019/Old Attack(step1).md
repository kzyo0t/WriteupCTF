The web is down now, so I wil show some my capture from burpsuite
When login to the web, the userpage show a text Hi,username, .... 
![userpage](userpage.png)
You can see auth_name cookie. This is not change after some request. 
Idea: After some account create, a saw the auth_name have changed. At the end I decide create a long name to check if this cookie use which 
encypt ethorigim, so i think they use aes ECB to encrypt auth_name. 
<p align="center">
  <img src="https://en.wikipedia.org/wiki/Block_cipher_mode_of_operation#/media/File:ECB_encryption.svg" height="20%" width="20%">
</p>
this ethogirum decrypt with a block, so if you know the block size you will create a custom cipher text you want as "admin". 
![userpage_admin](userpage_admin.png)

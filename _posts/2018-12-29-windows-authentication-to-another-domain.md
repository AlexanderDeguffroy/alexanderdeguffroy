---
layout: post
title: Windows authentication to another domain
subtitle: How to connect to SQL Servers in another domain using windows authentication.
tags: [Sql],[Connectivity]
---

Sometimes you have the need to connect to a SQL Server (or another resource) in another domain and you have(or want) to use windows authentication. 
This is possible by using the windows credential manager. 
- Open Credential Manager
- Go to Windows Credentials
- Click "Add a Windows credential"
- Fill in the servername (and port-number when connecting to SQL) in the "internet of network adrress"-field. 
- In the username field fill in the windows account you want to use, don't forget to include the domain eg YOURDOMAIN\USERNAME.
- Populute the "Password" field with the correct password.
- Click Ok

The only thing you might still have to do is add the servername (add corresponding IP) to your host file because your DNS-Server probably won't be able to resolve the servername. 





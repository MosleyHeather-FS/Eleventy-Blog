---
title: Password Hashing Article
date: 2022-08-28
tags:
  - React
  - Password Hashing
  - React Router
layout: layouts/post.njk
---

<img src = "https://live.mgm-tp.com/wp-content/uploads/2019/04/Fig4-Changing-Password-Process.png" style = "display: grid; margin-top: 10%; margin-bottom: 5%; width: 50%">

As simple 'Go with the Flow' internet user myself, I never gave much thought to passwords and how they work to keep your accounts and information safe. I always assumed, probably like most, that it protects your information by being uniquely created by you. In a way, this is technically true; however, it isn't the whole truth. There is much more to password protection and internet security than simply having a user create something unique. 

See what really is protecting isn't necessarily those special characters and extra numbers. Especially for those of us that just add on a exclamation point and a number one at the end of our password and call it a day. What really is actually protecting you is called password hashing. Password hashing uses an algorithim of random numbers, letters, and special characters to make your password harder to figure out and hack into. The way this is done is by using different programs like Bcrypt, SHA, Pufferfish2, Script, etc. In this case I'll focus on Bcrypt because it's what I'm used to, and because the others do their password hashing a bit differently.

The way Bcrypt works is that it uses a salt value to add a random value to the password string. This value basically makes a unique password even longer and even more unique. The higher the salt value the higher the amount of characters in the hash gets. If you go too crazy with the amount you might end up causing issues for even your server to figure out and authenticate the password though. So highly recommended not to go too crazy and make the salt amount too high. It's not needed regardless.

Well how does the site figure out the password if it's hashed? Great question! Bcrypt actually has a way to compare the hash and the password using the same algorithm to check and see if the inputed password from the user login matches the password stored in the database. If the two don't match you don't get logged in. If the two do match then it will allow you the login. Because it's the same system creating the hash to begin with, it has a way of securely storing that data to be compared and used for login authorization.

If Bcrypt is so secure why do I keep having to recreate passwords and making them even more unique each time? Yet another great question! While it is really secure, some places may not use it or it may even be those places want another level of extra protection. It can be annoying, but in their minds it's easier that way because they don't want to lose customers or money by being known for not having a secure site. The more unique the password, regardless of the level of hash security, the better in a lot of peoples minds. Basically, look at it as an over protective mother wrapping their kids up in 5 layers of jackets because it's snowing outside. It's basically the company not wanting to be labeled forever as a place that didn't keep your information secure. Especially, if that place is a bank or has access to banking information. Social Security has a website. Imagine what would happen if they messed up and their website was hacked into. While it may be overkill, some places believe the safer the better.
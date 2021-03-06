# pyCombotCAS_API

Simple CAS API for python bots, so you can integrate the [Combot Anti-Spam System](https://combot.org/cas) in
your own python bot, with the original Telegram API.

# What is this?

This is an attempt at writting an API [(what's an API?)](https://en.wikipedia.org/wiki/Application_programming_interface) for compatibility with
python bots. It contains a set of functions to check if a user is CAS Banned or not. You can write a new bot that only checks for
CAS banning with this API.

This is a work in progress, so there might be (definitely are) some bugs out there. You are welcome to open
an issue mentioning this. All I ask is for you to start it with [BUG], just to help me sort most stuff.

# What is this not?

This is not a replacement for Combot. This is not Combot. This is not also the full Combot API. This does not
contain any "interfacing" functions, such as message replies, statistics and all other functions Combot has. I
will say this one more time: This. Is. Not. Combot.

Please read the instructions, it also does not work on it's own. It is an API.

# How can I use it then?

As you use Telegram's API: as an API. You import this module in your script and call functions directly from it.

`import project.modules.functions.cas_api as cas`

If you do it like this, all you need to do to call a function from it is:

`cas.function()`

That's pretty much it. Enjoy.

# Extra info:

I reserve the rights to take down this project, change any of these information/disclaimer files, and to revoke
or change the license under which the project is built, if needed.

# References:

All the methods here created were developed by myself, so the code belongs to me. It is licensed under [DBADPL-B](https://github.com/nunopenim/DBADPL-B), 
which means you are free to use it, even for commercial purposes, but with proper crediting if no changes were made. For the development
process (past, present and future), I used the [Combot Anti-Spam System (CAS) API documentation](https://combot.org/cas/api)
as a reference. The Combot Anti-Spam System and all the data, services and products provided do not belong to me in
any way, shape or form.

SBGAuth
=======

Simple But Good secure for net/http package.

How Does It Works?
------------------

I'm using `compare(bcrypt(Client IP address + Password), bcrypted_recieved)` for auth because you cannot fake IP addresses.

Example
=======

Client
------

**Will not work:** `GET http://golang-http-server-url/something/?auth=ThePassword`
**Result:** `{"message":"Sorry? We didn't catch that.","success":false}` (Can be changed, of course)

**Will Work:** `GET http://golang-http-server-url/something/?auth=$2a$10$E2uO.j9/MeHmgDyZEWurkudEFFVrC/JyaNhU2pnf0NsVvvRe5I70m`
**Result:** `{"Russian_spy_list":[{"name":"Valdimir", "age":32, "location":"WDC"}, {"name":"Igor", "age":76, "location":"NY"}]}` (Russian Spy List not included)

Server
------

SOON

# phpStopForumSpam
A simple StopForumSpam implementation in php

This file works by sending a GET request to:

http://www.stopforumspam.com/api?email=g2fsehis5e@mail.ru&username=MariFoogwoogy&f=json

you get the return a JSON i.e.:

{"success":true,"email":{"lastseen":"2009-06-25 00:24:29","frequency":2,"appears":true},"username":{"frequency":0,"appears":false}}

In order to use:

1. Require this file using i.e.: require_once('StopForumSpam/Model.php');

2. Set spamTolerance by directly accessing the property i.e.: \Models\StopForumSpam\Model::spamTolerance = 10;

3. Verify if a user is classified as spam with the is-functions i.e.: if (\Models\StopForumSpam\Model::isSpamBotByIpOrEmailOrUsername($ip, $email, $alias)) { do something .. } else { do something else .. } 


Author is Christian Johansson <christian@cvj.se>

Visit StopForumSpam at: http://www.stopforumspam.com 

or my blog: http://blog.cvj.se/

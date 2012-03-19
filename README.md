#Twilio-PHP Library Interface#

This module makes use of the 2.x release of the [Libraries API module](http://drupal.org/project/libraries). The Libraries module helps manage external libraries. The Twilio API meets this definition. 

Place the approprate version of the [Twilio API for PHP](https://github.com/twilio/twilio-php) in the libraries directory within the site you are working. That may be 'default' or 'all' like the following: sites/all/libraries or sites/default/libraries. The end result after extracting the library should be sites/.../libraries/twilio-php/Services/Twilio.php.

If you have `git` on your machine, you could install the Twilio library like this:

```shell
cd sites/.../libraries
git clone git://github.com/twilio/twilio-php.git

# future updates could be performed with 
cd sites/.../libraries/twilio-php
git pull
```

To take full advantage of the Twilio API, you should provide your Account SID and your Auth Token, both of which can be found on your [Twilio Dashboard](https://www.twilio.com/user/account). Configuration can be performed either using variables hardcoded into settings.php or the UI. If you want to hardcode them then look at the UI for the variable names. The basics are as follows.

```php
$conf['twiliophp_account_sid'] = '...';
$conf['twiliophp_auth_token'] = '...';
```

The code in this module was modified from a similar library interface, the [AWS SDK for PHP](http://drupal.org/project/awssdk). Thanks to user `boombatower` for the great module.
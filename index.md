# Fuck Spam -- ICU Domains

### What is the purpose of this site?
I got tired of getting a ton of spam email from ICU domains. So I decided to bounce those messages with a message to visit this site instead.

### Are others impacted by these spammers?
Yes! A quick search online for "spam email icu domains" will result in many results of other people running into this problem.

### So what can I do about it?
Block those fucking spammers!

## I got my inspiration from other similiar sites
- https://blocked.icu/
- https://blog.paranoidpenguin.net/2019/08/icu-tld-i-see-you-spammer/

## So.. how do I block these spammers?

I will describe how I blocked them in Postfix (yes.. a copy/paste from the above sites :-)

- In the following file; /etc/postfix/sender_access -- enter the following:
`/\.icu$/ 554 Fuck off ICU spammers`

- In the following file; /etc/postfix/main.cf -- enter the following:
`smtpd_sender_restrictions = pcre:/etc/postfix/sender_access`

- Restart/Reload Postfix

If you get a ton of ICU spam, you can report the domains: https://nic.icu/report-abuse/

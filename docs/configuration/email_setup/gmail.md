![SeAT](https://i.imgur.com/aPPOxSK.png)

# Email Setup - Using GMail

## Introduction
SeAT requires email to be setup to allow for things like notifications to be sent.
This guide will attempt to describe how to go about setting up your email using [GMail] as an SMTP.

## The config
As with anything Laravel, the config for your email setup will live in your installs `.env` file. To use GMail as an SMTP service, set the `MAIL_DRIVER` option in your `.env` configuration file to `smtp`. Next, specify the SMTP details:

```php
// File: .env

MAIL_DRIVER=smtp
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME=username@gmail.com
MAIL_PASSWORD=gmailapppassword
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS=username@gmail.com
```
!!! 'gmailapppassword' is not your gmail account password):
```bash
https://support.google.com/accounts/answer/185833?hl=en
```
Done! To test, you can add some mail notification using the `Integrations` and `Notification groups`.

[GMail]: https://www.gmail.com

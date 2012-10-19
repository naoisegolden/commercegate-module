Commercegate Module for Drupal
=============

This module creates a callback server for the payment service [CommerceGate](http://commercegate.com), a block to display a single link to the CommerceGate payment page and custom actions and triggers.

The module creates a trigger for each of the available transaction types: sale, rebill, upsell, refund and cargeback. Once a payment is received from the CommerceGate servers, the module triggers the correct trigger and returns a string response to de CommerceGate server.

It also creates a custom action that sends an email with the transaction information to a given email address. This actions must be attached to each of the triggers.

Each trigger, action and event generates a log in the System Log.

### Available Settings

* **Account ID:** CommerceGate account ID.
* **Website ID:** Website ID in CommerceGate configuration.
* **Package ID:** Package ID in CommerceGate configuration.
* **Notification email:** Email to which send the notifications.
* **Send user email:** Send logged user's email to Payment Page.
* **Send username:** Send logged user's username to Payment Page.
* **Send user password:** Send logged user's password (hashed) to Payment Page.
* **Send user language setting:** Send logged user's language setting to Payment Page.
* **Check remote IP:** Only accept callbacks from CommerceGate's IPs.

In your CommerceGate account, you must provide the following setting for your site's Gateway Configuration:

Callback URL: `http://yoursite.com/commercegate/callbackserver`

Callback Type: `String`

The rest of options are at your choice, since they can be configured in the module settings.

### Configuration

To configure the module go to: `admin/settings/commercegate` 

To configure triggers go to: `admin/build/trigger/commercegate` 

To see the reports go to: `admin/reports/dblog/commercegate` 

## Endorse me

[![endorse](http://api.coderwall.com/naoise/endorsecount.png)](http://coderwall.com/naoise)
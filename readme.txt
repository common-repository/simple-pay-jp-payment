=== Simple PAY.JP Payment ===
Contributors: koyacode
Tags: payment,shopping,credit card,payment request,e-commerce
Requires at least: 4.9
Tested up to: 6.5
Requires PHP: 5.6
Stable tag: 1.2.0
License: GPL2
License URI: https://www.gnu.org/licenses/gpl-2.0.html

== Description ==
This plugin provides payment form by PAY.JP with simple shortcode.

Note:
The supported currency is only JPY so far.

Example of Shortcode:

	[simple-payjp-payment amount=50 form-id="id-string" name='no' result-ok="https://example.tokyo/?page_id=7" result-ng="https://example.tokyo/?page_id=8" ]

 * amount (mandatory*): price in JPY
 * plan-id (mandatory*): subscription plan ID
 * form-id (mandatory): any ID of the form
 * name: show/hide name field ('yes' => show (default), 'no' => hide)
 * result-ok: page url to redirect after payment succeeded if you want to customize success message
 * result-ng: page url to redirect after payment failed if you want to customize failure message
 * prorate: disabled/enabled prorated for subscription payment ('no' => not prorated (default), 'yes' => prorated)

(*) 'amount' is mandatory for single payment. 'plan-id' is mandatory for subscription payment. 'amount' and 'plan-id' should be exclusive.

You can confirm these information of each payments in descripton property of Charge record on PAY.JP admin panel.

Only one shoutcode can be placed in a page.

== API ==

=== Action hook ===

* simplepayjppayment_result_ok: called after payment succeeded
* simplepayjppayment_result_ng: called after payment failed

= Localization =
* English (default) - always included
* Japanese - always included

== Installation ==
1. Unpack the download package.
2. Upload all files to the /wp-content/plugins/ directory.
3. Activate this plugin in \"Plugin\" menu.

== Technical Details ==

How to use is summalized in the following page:
[WordPressプラグイン Simple PAY.JP Payment](https://it-soudan.com/simple-pay-jp-payment/)

== Changelog ==
= 1.2.0 =
Add action hook 'simplepayjppayment_result_ok' and 'simplepayjppayment_result_ng'

= 1.1.0 =
Add prorated for subscription payment

= 1.0.0 =
Increase amount limit to 3,000,000 yen

= 0.2.0 =
Add subscription payment

= 0.1.7 =
Security update

= 0.1.6 =
Add redirection option after payment to customize success/failure message

= 0.1.5 =
Align settings order to that on PAY.JP API panel

= 0.1.4 =
Change redirect process

= 0.1.3 =
Add name field

= 0.1.2 =
Fix multiple post issue by reload

= 0.1.1 =
Fix readme.txt

= 0.1.0 =
Initial release

### RIP Technologies
RIP is a team of two [Armstrong State University](https://www.armstrong.edu) students: Charles Poole (designer) and Nikenson Midi (developer).

**** RIP Modifications *****

IT IS VERY IMPORTANT THAT MOST OPENCART RECOMMENDATIONS SHOULD BE IGNORED AS THIS SOFTWARE IS DIRECTLY MODIFIED.


RIP developers and designers are undergraduate students from Armstrong State University at the time of the construction of this application. Jan 12, 2016 thru May 6, 2016

The following files were modified in order to accomodate business needs:
- Admin/catalog/checkout/cart => link rerouting 
- Admin/model/customer/customer => edit and add functions were added and the rest of the file edited
- Admin/language/customer/customer
- Admin/controller/customer/customer => entry to capture the uploaded files and the name of the foldername for database purpose. 
- Admin/view/template/customerform.tpl => reflect the effect of the entry above
- Admin/controller/catalog/product => new interface for the product entries
- Admin/view/template/catalog/product_list => transform this file into a recipient for Photo attributes such as deep matte or luster 	
- Admin/model/catalog/product => add new queries to support its controller counterpart
- Admin/controller/catalog/category => New interface for the category section to integrate the packages
- Admin/model/catalog/category 
- Admin/common/menu => changing the ling for the left side column in administration 
- Admin/controller/common/filemanager => multiple file uploaded enabled
- Admin/view/template/common/filemanager => multiple file uploaded enabled
- Admin/model/setting/setting => 2 new functions are introduced: one to set freshbooks and another to get freshbooks
- Admin/view/template/customer/customer_list => The link to the locking functionality i omitted 	
- Admin/controller/customer/customer => added the folder name input, the link to upload the folder the validation checks for folder input and freshbooks api to register cuctomers
- Admin/view/template/common/menu => eliminate all functionalities (links) that are irrelevant to clients
- Admin/view/template/common/header => Take out the links to Opencart documentation and forums in order to encapsulate client from the mechanism of Opencart
- Admin/controller/common/filemanager => Modifies in order to accept bmp files and JPG files 		

- Catalog/account/home 
- Catalog/account/login
- Catalog/view/template/customtheme folder is created.
- Catalog/view/javascript/common.js => cart > add was modified to two parameters
- catalog/view/theme/default/template/checkout/cart => cart modifications 
- Catalog/controller/checkout/cart => cart modifications
- Catalog/system/library/cart => cart modifications
- catalog/language/english/checkout/checkout => Change the language on payment method and other titles.	
- Catalog/controller/checkout/payment_method => this is the controller for the comment section upon checking out
- catalog/controller/account/wishlist => Change $product_info to $product_name and take out the session wishlist.
- catalog/view/theme/default/template/checkout/payment_method => aesthetics icons for button sync
- catalog/view/theme/customtheme/template/common/home	 =>  adding carousel, taking our the column left & right and content bottom
- catalog/model/checkout/order => Create functions to pull freshbooks API data such as request body and invoice numbers
- catalog/controller/information/contact => Add a ressource to access the link for home
- catalog/language/english/payment/cod => change the text title to invoice
- catalog/controller/checkout/payment_address => Place the freshbook API to collect payment address and update customer file on freshbooks
- catalog/view/theme/default/template/account/password => eliminate colum left and rightand content bottom
					
- extension/payment/cod => Cash on delivery is now Freshbooks transactions


DATABASE MODIFICATION:
- table apackage was added => collecting the diffrent packages as they are unique to the business
- table customer was modified
- table product was rearranged completly => So the client can be the one create the product that way not every picture is a product.
- table cart in order to capture picture's route as picture name and the id
- table oc_api is altered and the column name is now varchar 255 character
- table oc_freshbooks_request is created to retain all the request content
- table oc_freshbooks_api is created to maintain and store the client freshbooks API
_ table oc_freshbooks_invoice is created to store freshbook invoice numbers
**** RIP Modifications end. *****


# OpenCart

## Overview

OpenCart is a free open source ecommerce platform for online merchants. OpenCart provides a professional and reliable foundation from which to build a successful online store.

## Reporting a bug

Read the instructions below before you create a bug report.

 1. Search the [OpenCart forum](http://forum.opencart.com/viewforum.php?f=161), ask the community if they have seen the bug or know how to fix it.
 2. Check all open and closed issues on the [GitHub bug tracker](https://github.com/opencart/opencart/issues).
 3. If your bug is related to the OpenCart core code then please create a bug report on GitHub.
 4. READ the [changelog for the master branch](https://github.com/opencart/opencart/blob/master/changelog.md)
 5. Use [Google](http://www.google.com) to search for your issue.
 6. Make sure that your bug/issue is not related to your hosting environment.

If you are not sure about your issue, it is always best to ask the community on our [bug forum thread](http://forum.opencart.com/viewforum.php?f=161&sid=f5208eb3888b13a5065be051362daa0d)

**Important!**
- If your bug report is not related to the core code (such as a 3rd party module or your server configuration) then the issue will be closed without a reason. You must contact the extension developer, use the forum or find a commercial partner to resolve a 3rd party code issue.
- If you would like to report a serious security bug please PM an OpenCart moderator/administrator on the forum. Please do not report concept/ideas/unproven security flaws - all security reports are taken seriously but you must include the EXACT details steps to reproduce it. Please DO NOT post security flaws in a public location.

## Making a suggestion

Please do not create a bug report if you think something needs improving / adding (such as features or change to code standards etc).

We welcome public suggestions on our [User Voice site](http://opencart.uservoice.com).

## How to contribute

Fork the repository, edit and [submit a pull request](https://github.com/opencart/opencart/wiki/Creating-a-pull-request).

Please be very clear on your commit messages and pull request, empty pull request messages may be rejected without reason.

Your code standards should match the [OpenCart coding standards](https://github.com/opencart/opencart/wiki/Coding-standards). We use an automated code scanner to check for most basic mistakes - if the test fails your pull request will be rejected.

## Versioning

The version is broken down into 4 points e.g 1.2.3.4 We use MAJOR.MINOR.FEATURE.PATCH to describe the version numbers.

A MAJOR is very rare, it would only be considered if the source was effectively re-written or a clean break was desired for other reasons. This increment would likely break most 3rd party modules.

A MINOR is when there are significant changes that affect core structures. This increment would likely break some 3rd party modules.

A FEATURE version is when new extensions or features are added (such as a payment gateway, shipping module etc). Updating a feature version is at a low risk of breaking 3rd party modules.

A PATCH version is when a fix is added, it should be considered safe to update patch versions e.g 1.2.3.4 to 1.2.3.5

## Releases

OpenCart will announce to developers 1 week prior to public release of FEATURE versions, this is to allow for testing of their own modules for compatibility. For bigger releases (ones that contain many core changes, features and fixes) an extended period will be considered following an announced release candidate (RC). Patch versions (which are considered safe to update with) may have a significantly reduced developer release period.

The master branch will always contain an "_rc" postfix of the next intended version. The next "_rc" version may change at any time.

Developer release source code will not change once tagged.

If a bug is found in an announced developer release that is significant (such as a major feature is broken) then the release will be pulled. A patch version will be issued to replace it, depending on the severity of the patch an extended testing period may be announced. If the developer release version was never made public then the preceding patch version tag will be removed.

To receive developer notifications about release information, sign up to the newsletter on the [OpenCart website](http://www.opencart.com) - located in the footer. Then choose the developer news option.

## How to install

Please read the installation instructions included in the repository or download file.

## License

[GNU General Public License version 3 (GPLv3)](https://github.com/opencart/opencart/blob/master/license.txt)

## Links

- [OpenCart homepage](http://www.opencart.com/)
- [OpenCart forums](http://forum.opencart.com/)
- [OpenCart blog](http://www.opencart.com/index.php?route=feature/blog)
- [How to documents](http://docs.opencart.com/)
- [Newsletter](http://newsletter.opencart.com/h/r/B660EBBE4980C85C)
- [User Voice suggestions](http://opencart.uservoice.com)

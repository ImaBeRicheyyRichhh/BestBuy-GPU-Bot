# BestBuy GottaCatchEmAll Bot — Open Source Trading Card Buy Bot

## Description

BestBuy GottaCatchEmAll Bot is an Add to cart and Auto Checkout Bot. This auto buying bot can search an item repeatedly on the item page using one keyword. Once the desired item is available it can add to cart and checkout very fast. It can run for multiple items simultaneously.

## Why???

Cuz we gotta catch em all!!!

### Dependencies

1. Install [Tampermonkey Extension](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo) for Chrome or [Userscripts](https://apps.apple.com/us/app/userscripts/id1463298887) for IOS
2. BestBuy Account (Please be signed in) 
3. Please allow [Pop-Ups](https://www.isc.upenn.edu/how-to/configuring-your-web-browser-allow-pop-windows) for ```https://www.bestbuy.com/``` in your browser


### Installing

* Go to https://greasyfork.org/en/scripts/540069-bestbuy-gottacatchemall-bot and click the green "Install this script" button
* Follow the on screen instructions to install
* [Optional step) Update REQUIRED FLAGS in the code for your information such as the item keyword, your last 4 phone digits, etc. Then save the script.
* Go to https://www.bestbuy.com and click the tampermonkey extension, make sure script "BestBuy-GottaCatchEmAll-Bot" is enabled
* Login to BestBuy user account, have an address saved from a previous purchase or cart checkout step
* Go to https://www.bestbuy.com/site/ultra-pro-poke-ball-premium-9-pocket-pro-binder-for-pokemon/6570314.p?skuId=6570314 and bot will add to cart and checkout! Magic!


### Further Details

* Item Keyword corresponds to a keyword in your product name ( case sensitive | no spaces allowed )
	*_you can retrive ITEM_KEYWORD from the Black Title on a specific Products Page_*
```
const ITEM_KEYWORD= "Ultra";
```
* Credit Card CVV  (Not Required. BOT just wont do final checkout)
```
const CREDITCARD_CVV = "***";
```
* Test Mode "YES" will not purchase item. But do all the steps except pressing the last button. ```TESTMODE = "No" ``` will purchase the item.
```
const TESTMODE = "Yes"
``` 
* Enter last 4 digits of phone # for SMS verification (optional)
```
const SMS_DIGITS = "****"
``` 
* Preferred Shipping "Yes" will select the Shipping Radio Button if available
```
const PREFERRED_SHIPPING = "No"
``` 

## Workflow

This tool is designed to multitask. That means, it can run in many tabs simultaneously, if there is a ```ITEM_KEYWORD``` overlap.
If there is no ```ITEM_KEYWORD``` overlap. You will need to create a new copy of script for each ```ITEM_KEYWORD```.

Please make sure your CART is empty.

After updating variables and enabling the script in Tampermonkey, go to the your favourite GPU page in BestBuy.
If the Title of GPU has ```ITEM_KEYWORD```, it will add the item to cart and checkout. If item is out of stock it will keep on refreshing every 5 seconds.

Please use ```TESTMODE = "Yes"``` to test with an item already in stock.


## License

This project is licensed under the MIT License - see the LICENSE.md file for details

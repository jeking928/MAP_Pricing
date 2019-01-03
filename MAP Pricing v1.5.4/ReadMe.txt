MAP Pricing v1.5.4

This is a revamped version of MAP Pricing v1.0 by Richard Kersey (www.slickricky.com).  MAP Pricing = Manufacturer's Advertised Price.  It is used when you want to sell something for a price that is lower than what you are able to advertise on your website.  The actual price will only display in the cart.

This module adds a question to the admin section when you're adding or editing a product, that asks if this product should have MAP pricing enabled. If MAP pricing is enabled for that product, it replaces the price throughout your website with editable text that says: "Priced so low, we're not able to advertise it. Add to cart for price."

You may optionally also specify a "minimum displayed price" in the admin, which will cause the storefront to say "$xxx.xx but for a lower price, add to cart" (text is editable)

ONLY WORKS WITH PRODUCT-GENERAL product type.  For other product-types, you must manually merge coding changes into corresponding admin files, using the supplied admin files as a model.

#################################################################################
Installation:

1) FTP both the admin and includes folder to your Zen Cart directory.  If you have renamed your admin folder, then of course substitute the name of your admin folder instead of "admin".  You will be prompted to overwrite some files, click yes to each.
(You might want to merge any customizations you've made to those files before overwriting them! WinMerge is free.)
(Rename the YOURTEMPLATEFOLDERNAME folder to whatever folder your active template is called, and put the stylesheet into that folder's corresponding css folder.)

2) NOTE: This plugin doesn't require any SQL Patch for installation. 
BUT you will see blank pages on your storefront until you login to your Admin and click to edit any product (this will trigger the database changes automatically).

3) You should be good to go.  If you have any errors or problems, you can post in the Zen Cart forum or email me (thebricktongroup@gmail.com).

4) To change the text "Priced so low, we're not able to advertise it. Add to cart for price." edit your /includes/languages/english/extra_datafiles/map_pricing.php 

5) If you wish to use the styling options, apply your updates to /includes/templates/your_template_folder/css/stylesheet_map_pricing.css



##########################

Removal:
a) If you need to remove this addon, you will need to delete all the files you added as part of this addon. Of course, since this addon required replacing some original core files, you will need to put back the original files after removing the files customized in this addon.
b) You will need to run a small SQL patch to delete the database data added/maintained by this addon:
		ALTER TABLE products DROP map_enabled;
		ALTER TABLE products DROP map_price;
(If you run this via phpMyAdmin, you may need to add the appropriate table-name prefix before the word "products", if your site is using a prefix.)

##########################


REVISION HISTORY:
v0.1 - 2006 released by Richard Kersey slickricky.com
v1.0 - 2006 updated by bgroup99 thebricktongroup@gmail.com
v1.1 - 2006 updated by DrByte to simplify the code and make integration easier for storeowners
v1.2 - 2007 (was initially called "2.0" but was later changed to 1.2) updated by slickricky.com to add the ability to state what the MAP-price "is" instead of just "so low we can't say".
v1.5 - 2012 updated by DrByte -- to make it work with Zen Cart v1.5.0 specifically.  This version will NOT work with prior versions of Zen Cart before v1.5.0.
v1.5.1 - Sept 2012 - updated by DrByte for ZC v1.5.1 specifically. NOTE: requires manual adaptation if needed for other than product-general product type.
v1.5.3 - 2014 updated by DrByte to make it work with ZC v1.5.0-thru-v1.5.3
V1.5.4 - 6/13/2017 updates by jeking to be compatible with ZC 1.5.5e


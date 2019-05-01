# SSLCommerz-Payment-Gateway
SSL Commerz Payment Gateway API Integration for Laravel

## Description
In this example you will find below script and a mysql table creation file.
  1. routes\web.php : Create route for the functions
  
  *: Rename Controller files as your needs. (Here It's given for TEST & LIVE)
  
  2. app\Http\Controllers\PublicSslCommerzPaymentController.php: All the functions to do the transaction. Read the comments carefully.
  3. app\Http\Controllers\SSLCommerz.php: Helping class, here you will input store information
  4. app\Http\Middleware\VerifyCsrfToken.php : Input Route names to accept call from out side your site
  5. Sample_order_table.sql: This is a sample table to store order or transaction information.
  

## Run the project
	1. First create your Sanbox(Test Environment) store account from below url. After registration you will get two mail. One for Store_id and Store_password.Another one for Report panel access.	
	   https://developer.sslcommerz.com/registration/
	   Note: For live store id or account you have to communicate with us. Our mail address: operation@sslcommerz.com
	2. Then give the store_id and store_password in SSLCommerz.php page. 
	3. Here you have to run the PublicSslCommerzPaymentController.php controller by calling pay(Like: http://yourdomain.com/pay or http://yourdomain.com/public/pay)
	   Here you have to receive all the order data to initate the payment.
           Lets your oder trnsaction informations are saving in a table called "orders"
           In orders table order uniq identity is "order_id","order_status" field contain status of the transaction, "grand_total" 
	   is the order amount to be paid and "currency" is for storing Site Currency which will be checked with paid currency.
	4. You have to set your IPN page from the provided report panel. After login, go to My Stores then IPN Settings. IPN url will be http://yourdomain.com/ipn or http://yourdomain.com/public/ipn.

## Help URL
	1. https://developer.sslcommerz.com/docs.html :URL to start integrate SSLCOMMERZ as a Developer
	2. https://developer.sslcommerz.com/registration/: URL to Create Account in Sandbox


## Source URL
https://github.com/sslcommerz/Integration_in_Laravel-5.6-with-IPN


## Few Instructions for LIVE
*: Change SSLCZ_STORE_ID, SSLCZ_STORE_PASSWD with your store id and password given by SSLCOMMERZ define("SSLCZ_STORE_ID", "XXXXX");define("SSLCZ_STORE_PASSWD", "XXXXX");

*: If you are using SANDBOX storied and password then define("SSLCZ_IS_SANDBOX", true); keep SSLCZ_IS_SANDBOX, true. If you are using Live store id and password then turn SSLCZ_IS_SANDBOX, false.

*: If you are using Localhost then define("SSLCZ_IS_LOCAL_HOST", true); keep SSLCZ_IS_LOCAL_HOST, true. If you are using Live server then turn SSLCZ_IS_LOCAL_HOST, false.

# Alhamdulillah ~ All Praise is Due to ALLAH Alone ...

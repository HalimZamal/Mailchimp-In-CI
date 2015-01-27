# Integrate mailchimp and Codeigniter (CI)
I will explain how to integrate MailChimp with CodeIgniter framework
## Requirements

 * PHP 5.2+
 * Mailchimp
 
## Link

 * Download CodeIgniter Framework https://ellislab.com/codeigniter/user-guide/installation/downloads.html
 * Register Mailchimp http://mailchimp.com/

## Instalation

 * Download and Extract FIle
 * Place mcapi.php in application/libraries
 

## How to Use

 * Please register and get API Key
 * Create list or group in mailchimp
 * Get list id
 * Insert code below in controllers
  
 User for select one data
```php
	$config = array(
		'apikey' => ''      // Insert your api key
		'secure' => FALSE   // Optional (defaults to FALSE)
	);
	$this->load->library('MCAPI', $config, 'mail_chimp');
	
	if($this->mail_chimp->listSubscribe($list_id, $email)) {
		// $email is now subscribed to list with id: $list_id
	}
	
```

# Simple Email Crawler
A PHP Email Crawler. Crawl a single website or multiple websites for email address(s) using simple_html_dom
You can test this crawler here:

https://marcosraudkett.com/mvrclabs/email-crawler/tests/


### Installation
```php
<?php
  /* use autoloader */
  require_once "/path/to/includes/init.php";
?>
```

### Manual Installation
```php
<?php
  /* include email_crawler */
  require_once "/path/to/classes/email_crawler.class.php";
?>
```

### Usage
```php
<?php
  /* Your url that you wish to crawl */
  $url = 'https://marcosraudkett.com';
  $crawl = email_crawler::crawl_site($url);
  
  /* foreach email */
  foreach($crawl['results'] as $result) 
  {
    echo $result['element']; /* prints out the element this email address was found */
    echo $result['email']; /* prints out each email address on that page */
  }
?>
```

## Contributing
Feel free to help this project or if you've found a bug then feel free to visit [the issues page](https://github.com/juliuste/tallink/issues).

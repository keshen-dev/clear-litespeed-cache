# clear-litespeed-cache
A simple PHP script to clear LiteSpeed cache in WordPress by visiting a specific URL.
This repository contains a simple PHP script designed to clear the LiteSpeed cache for a WordPress website. When placed in the root directory of a WordPress installation, the script can be triggered by visiting a specific URL (e.g., http://your-domain.com/clear.php). This provides a quick and convenient way to clear your site's LiteSpeed cache.

Please note, this method does not implement any form of authentication, meaning anyone who knows the URL can clear the cache. If you plan to use this script in a production environment, please consider adding appropriate security measures to prevent unauthorized cache clearing. As always, we recommend backing up your site before making any changes.

Feel free to use and modify the script as per your needs. Contributions to improve the script are always welcome.

```
<?php
// Load WordPress core
require_once( 'wp-load.php' );

// Define function to clear cache
function clear_litespeed_cache() {
    if (function_exists('do_action')) {
        do_action('litespeed_purge_all');
    }
}

// Call the function
clear_litespeed_cache();

echo "Cache cleared successfully.";
?>
```

# How to use productswithqr module.

Git clone module under "web/modules/custom"
refer command "git clone https://github.com/pankajraundal/productswithqr.git"
Enable module using command 
refer command "drush en productswithqr"

## Install modules dependency
    - Add below snippet under root composer.json refer https://sicse.dev/blog/use-composerjson-file-custom-module-install-dependent-vendor-packages
    
    {
        "type": "path",
        "url": "web/modules/custom/*"
    }
    - run composer require command to add module as dependency in composer.json
    - refer command "composer require drupal/productswithqr:@dev"
    - Clear cache, you should now good to go.

## What it does by its own
    - It will creat content type products
    - It will create custom block for qr code.
    - Qr code Custom block will get auto placed on each products detail page. 
    
## What manual stuff need to do:
    - Module has package to generate qr code, for which composer json has been already added.
    - This composer json contains package for qr code with version.
    - Once module install composer install should needs to run from root.
    - This will add package into the vendor directory.

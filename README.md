# RIGHT PLACE
## Configuration

In the tag 'require' into composer.json archive add:

    "raphaeldeziderio/apirightplace": "dev-main"
        
Also in the composer.json archive, add in final archive:

    "repositories": [
            {
                "type": "vcs",
                "url": "https://github.com/Raphael-Augusto-Deziderio/ApiRightPlace.git"
            }
        ]

## Installation
You can add this library as a local, per-project dependency to your project using [Composer](https://getcomposer.org/):

    composer require raphaeldeziderio/apirightplace

## Usage examples
```php
use RaphaelDeziderio\ApiRightPlace\App\Http\Controllers\Api\ApiHotelSearch;

//GETTING THE CONTROLLER FROM RIGHT PLACE API
$api = app(ApiHotelSearch::class);

//SETTING THE LATITUDE AND LOGITUDE
$latitude = -19.7455269;
$longitude = -47.9575337;

/*
    OPTIONAL PARAMETERS: ORDER BY ['proximity' (DEFAULT) or 'pricepernight']
*/

//CALCULATING DE DISTANCE
$distance = $api->getNearbyHotelsApi($latitude, $longitude);

//RETURN THE RIGHT PLACE       
return $distance;

```


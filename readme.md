

## How I did this example

* In an existing Laravel project, i executed

```
 composer require farhanwazir/laravelgooglemaps
```

* Add this service provider in app.php

https://github.com/hector2/laravel-gmaps-example/blob/master/config/app.php#L169

* Add this alias in app.php

https://github.com/hector2/laravel-gmaps-example/blob/master/config/app.php#L230

* Execute this command to publish config
```
    php artisan vendor:publish --provider="FarhanWazir\GoogleMaps\GMapsServiceProvider"
```

* Create new project in Google Console

https://console.developers.google.com/projectcreate

* In this project, you need to enable Google Maps Javascript API and Geocoding API.

https://console.developers.google.com/apis

* You also need to create an API key for the Google Maps API (Recommended you choose option "Help me choose".

https://console.developers.google.com/apis/credentials

* Once you have an API key, copy and paste it in 

https://github.com/hector2/laravel-gmaps-example/blob/master/config/googlemaps.php#L14

(replace HERE_API_KEY with your API key)

Once you do this, the project is configured and you can use Google Maps API. This repo contains a simple example with a routing config, a controller and a view.

# Routing:

https://github.com/hector2/laravel-gmaps-example/blob/master/routes/web.php#L14

- Two routes, / and /map.

# Controller

https://github.com/hector2/laravel-gmaps-example/blob/master/app/Http/Controllers/MapController.php

It configures a map and a draggable marker. When you drag the marker, it updates its label (using Geocoding API, that's why you need to enable it).

# View

https://github.com/hector2/laravel-gmaps-example/blob/master/resources/views/map.blade.php

Simple view.


# How to try this example

Simply execute php artisan serve, and you should see the map in localhost:8000/map






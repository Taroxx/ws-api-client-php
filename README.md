# ws-api-client-php

The Wheel Fitment API allows for programmatic access to the database of www.wheel-size.com and its services. Use this API to retrieve information about vehicle fitment database for rims and tires, including OE and option fitments, and plus/minus sizing fitment information. A variety of country and language specific options are available. The coverage of fitment data for vehicles manufactured since 2000 is nearly 100%.  The information about fitment data is updated on a daily basis.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: v1
- Package version: 1.0.0
- Build package: io.swagger.codegen.languages.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/driveate/ws-api-client-php.git"
    }
  ],
  "require": {
    "driveate/ws-api-client-php": "*@dev"
  }
}
```

Then run `composer install`

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: user_key
$config = WsApiClient\Configuration::getDefaultConfiguration()->setApiKey('user_key', 'YOUR_API_KEY');

$apiInstance = new WsApiClient\Api\MakesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$countries = "us,gb,jp"; // string | Show information for local manufacturers from specified countries only. Use `GET /countries/` method to get the full list of countries. (e.g. `us,gb,jp`)

try {
    $result = $apiInstance->makesList($countries);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MakesApi->makesList: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://api.wheel-size.com/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BoltPatternsApi* | [**boltPatternsList**](docs/Api/BoltPatternsApi.md#boltpatternslist) | **GET** /bolt-patterns/ | Get list of bolt patterns
*BoltPatternsApi* | [**boltPatternsRead**](docs/Api/BoltPatternsApi.md#boltpatternsread) | **GET** /bolt-patterns/{bolt_pattern}/ | Model modifications by bolt pattern
*CountriesApi* | [**countriesList**](docs/Api/CountriesApi.md#countrieslist) | **GET** /countries/ | Returns a list of countries
*GenerationsApi* | [**generationsList**](docs/Api/GenerationsApi.md#generationslist) | **GET** /generations/ | Generations for the given model
*MakesApi* | [**makesList**](docs/Api/MakesApi.md#makeslist) | **GET** /makes/ | Returns a list of manufacturers
*MarketsApi* | [**marketsList**](docs/Api/MarketsApi.md#marketslist) | **GET** /markets/ | Returns a list of markets/regions
*ModelsApi* | [**modelsList**](docs/Api/ModelsApi.md#modelslist) | **GET** /models/ | Returns a list of models by manufacturer
*ModelsApi* | [**modelsRead**](docs/Api/ModelsApi.md#modelsread) | **GET** /models/{make}/{slug}/ | Get more info about model
*ModelsApi* | [**modelsReadYear**](docs/Api/ModelsApi.md#modelsreadyear) | **GET** /models/{make}/{slug}/{year}/ | Get more info about model/year
*SearchApi* | [**searchByHfTireList**](docs/Api/SearchApi.md#searchbyhftirelist) | **GET** /search/by_hf_tire/ | Find models matching given high flotation tire
*SearchApi* | [**searchByModelList**](docs/Api/SearchApi.md#searchbymodellist) | **GET** /search/by_model/ | Find OE and option fitments by model/year/trim
*SearchApi* | [**searchByRimList**](docs/Api/SearchApi.md#searchbyrimlist) | **GET** /search/by_rim/ | Find models matching given rim parameters
*SearchApi* | [**searchByTireList**](docs/Api/SearchApi.md#searchbytirelist) | **GET** /search/by_tire/ | Find models matching given tire parameters
*TiresApi* | [**tiresList**](docs/Api/TiresApi.md#tireslist) | **GET** /tires/ | Returns a list of tires
*TiresApi* | [**tiresRead**](docs/Api/TiresApi.md#tiresread) | **GET** /tires/{tire}/ | Model modifications matching given tire
*TrimsApi* | [**trimsList**](docs/Api/TrimsApi.md#trimslist) | **GET** /trims/ | Model modifications
*VehiclesApi* | [**vehiclesList**](docs/Api/VehiclesApi.md#vehicleslist) | **GET** /vehicles/ | Find OE and option fitments by model/year/trim
*YearsApi* | [**yearsList**](docs/Api/YearsApi.md#yearslist) | **GET** /years/ | Returns list of years for the given manufacturer/model


## Documentation For Models

 - [Aggregation](docs/Model/Aggregation.md)
 - [Body](docs/Model/Body.md)
 - [BoltPattern](docs/Model/BoltPattern.md)
 - [Country](docs/Model/Country.md)
 - [Generation](docs/Model/Generation.md)
 - [MakeModel](docs/Model/MakeModel.md)
 - [MakeWithModels](docs/Model/MakeWithModels.md)
 - [Market](docs/Model/Market.md)
 - [Model](docs/Model/Model.md)
 - [ModelWithTires](docs/Model/ModelWithTires.md)
 - [ModelWithTrims](docs/Model/ModelWithTrims.md)
 - [Power](docs/Model/Power.md)
 - [Pressure](docs/Model/Pressure.md)
 - [RimAgregation](docs/Model/RimAgregation.md)
 - [SizeAggregation](docs/Model/SizeAggregation.md)
 - [Tire](docs/Model/Tire.md)
 - [TiresAggregation](docs/Model/TiresAggregation.md)
 - [Trim](docs/Model/Trim.md)
 - [TrimWithMarketAndYears](docs/Model/TrimWithMarketAndYears.md)
 - [Vehicle](docs/Model/Vehicle.md)
 - [Wheel](docs/Model/Wheel.md)
 - [WheelPair](docs/Model/WheelPair.md)
 - [Year](docs/Model/Year.md)


## Documentation For Authorization


## user_key

- **Type**: API key
- **API key parameter name**: user_key
- **Location**: URL query string


## Author

info@wheel-size.com



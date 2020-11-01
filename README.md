# amznSellingPartnerApiPhpSdkAuthorization
The Selling Partner API for Authorization helps developers manage authorizations and check the specific permissions associated with a given authorization.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: v1
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen
For more information, please visit [https://sellercentral.amazon.com/gp/mws/contactus.html](https://sellercentral.amazon.com/gp/mws/contactus.html)

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
      "url": "https://github.com/raymundfischer/amznsellingpartnerapiphpsdkauthorization.git"
    }
  ],
  "require": {
    "raymundfischer/amznsellingpartnerapiphpsdkauthorization": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/amznSellingPartnerApiPhpSdkAuthorization/vendor/autoload.php');
```

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

$apiInstance = new amznSellingPartnerApiPhpSdk\Authorization\Api\AuthorizationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$selling_partner_id = "selling_partner_id_example"; // string | The seller ID of the seller for whom you are requesting Selling Partner API authorization. This must be the seller ID of the seller who authorized your application on the Marketplace Appstore.
$developer_id = "developer_id_example"; // string | Your developer ID. This must be one of the developer ID values that you provided when you registered your application in Developer Central.
$mws_auth_token = "mws_auth_token_example"; // string | The MWS Auth Token that was generated when the seller authorized your application on the Marketplace Appstore.

try {
    $result = $apiInstance->getAuthorizationCode($selling_partner_id, $developer_id, $mws_auth_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthorizationApi->getAuthorizationCode: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to *https://sellingpartnerapi-na.amazon.com/*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthorizationApi* | [**getAuthorizationCode**](docs/Api/AuthorizationApi.md#getauthorizationcode) | **GET** /authorization/v1/authorizationCode | Returns the Login with Amazon (LWA) authorization code for an existing Amazon MWS authorization.

## Documentation For Models

 - [AuthorizationCode](docs/Model/AuthorizationCode.md)
 - [Error](docs/Model/Error.md)
 - [ErrorList](docs/Model/ErrorList.md)
 - [GetAuthorizationCodeResponse](docs/Model/GetAuthorizationCodeResponse.md)

## Documentation For Authorization

 All endpoints do not require authorization.


## Author



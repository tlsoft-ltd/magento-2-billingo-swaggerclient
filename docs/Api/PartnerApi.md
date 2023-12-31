# Swagger\Client\PartnerApi

All URIs are relative to *https://api.billingo.hu/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createPartner**](PartnerApi.md#createpartner) | **POST** /partners | Create a partner
[**listPartner**](PartnerApi.md#listpartner) | **GET** /partners | List all partners

# **createPartner**
> \Swagger\Client\Model\Partner createPartner($body)

Create a partner

Create a new partner. Returns a partner object if the create is succeded.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\PartnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\Partner(); // \Swagger\Client\Model\Partner | Partner object that you would like to store.

try {
    $result = $apiInstance->createPartner($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartnerApi->createPartner: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\Partner**](../Model/Partner.md)| Partner object that you would like to store. |

### Return type

[**\Swagger\Client\Model\Partner**](../Model/Partner.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listPartner**
> \Swagger\Client\Model\PartnerList listPartner($page, $per_page, $query)

List all partners

Returns a list of your partners. The partners are returned sorted by creation date, with the most recent partners appearing first.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: api_key
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\PartnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int | 
$per_page = 25; // int | 
$query = "query_example"; // string | 

try {
    $result = $apiInstance->listPartner($page, $per_page, $query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartnerApi->listPartner: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional]
 **per_page** | **int**|  | [optional] [default to 25]
 **query** | **string**|  | [optional]

### Return type

[**\Swagger\Client\Model\PartnerList**](../Model/PartnerList.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


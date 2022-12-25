# OpenAPI\Client\ItemsApi

All URIs are relative to http://127.0.0.1:8000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createShoppingList()**](ItemsApi.md#createShoppingList) | **POST** /items | Create a new todo shopping list item |
| [**retrieveSingleShoppingList()**](ItemsApi.md#retrieveSingleShoppingList) | **GET** /items/{id} | Retrieve a single todo shopping list item by ID |
| [**retriveTodoList()**](ItemsApi.md#retriveTodoList) | **GET** /items | Retrieve a list of all todo shopping list items |
| [**updateTodoShoppingList()**](ItemsApi.md#updateTodoShoppingList) | **PUT** /items/{id} | Update a todo shopping list item |


## `createShoppingList()`

```php
createShoppingList($create_shopping_list_request): \OpenAPI\Client\Model\SuccessMessage
```

Create a new todo shopping list item

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ItemsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$create_shopping_list_request = new \OpenAPI\Client\Model\CreateShoppingListRequest(); // \OpenAPI\Client\Model\CreateShoppingListRequest

try {
    $result = $apiInstance->createShoppingList($create_shopping_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemsApi->createShoppingList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_shopping_list_request** | [**\OpenAPI\Client\Model\CreateShoppingListRequest**](../Model/CreateShoppingListRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SuccessMessage**](../Model/SuccessMessage.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `retrieveSingleShoppingList()`

```php
retrieveSingleShoppingList($id): \OpenAPI\Client\Model\Items
```

Retrieve a single todo shopping list item by ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ItemsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->retrieveSingleShoppingList($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemsApi->retrieveSingleShoppingList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Items**](../Model/Items.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `retriveTodoList()`

```php
retriveTodoList(): \OpenAPI\Client\Model\Items[]
```

Retrieve a list of all todo shopping list items

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ItemsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->retriveTodoList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemsApi->retriveTodoList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\Items[]**](../Model/Items.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTodoShoppingList()`

```php
updateTodoShoppingList($id, $update_shopping_list_request): \OpenAPI\Client\Model\Items
```

Update a todo shopping list item

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ItemsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string
$update_shopping_list_request = new \OpenAPI\Client\Model\UpdateShoppingListRequest(); // \OpenAPI\Client\Model\UpdateShoppingListRequest

try {
    $result = $apiInstance->updateTodoShoppingList($id, $update_shopping_list_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemsApi->updateTodoShoppingList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **update_shopping_list_request** | [**\OpenAPI\Client\Model\UpdateShoppingListRequest**](../Model/UpdateShoppingListRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Items**](../Model/Items.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

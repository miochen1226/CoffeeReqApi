# DefaultAPI

All URIs are relative to *http://localhost:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ordersGet**](DefaultAPI.md#ordersget) | **GET** /orders | Get all coffee orders
[**ordersPost**](DefaultAPI.md#orderspost) | **POST** /orders | Create a new coffee order


# **ordersGet**
```swift
    open class func ordersGet(completion: @escaping (_ data: RestResponseListOrdersDTO?, _ error: Error?) -> Void)
```

Get all coffee orders

Retrieves a list of all coffee orders

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


// Get all coffee orders
DefaultAPI.ordersGet() { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**RestResponseListOrdersDTO**](RestResponseListOrdersDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ordersPost**
```swift
    open class func ordersPost(orderDTO: OrderDTO, completion: @escaping (_ data: ResponseDTO?, _ error: Error?) -> Void)
```

Create a new coffee order

Creates a new coffee order with the provided details

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let orderDTO = OrderDTO(ticketUUID: 123, customerName: "customerName_example", productName: "productName_example", count: 123, pickupTime: Date(), temperature: TemperatureOption(), isUserCup: true) // OrderDTO | 

// Create a new coffee order
DefaultAPI.ordersPost(orderDTO: orderDTO) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderDTO** | [**OrderDTO**](OrderDTO.md) |  | 

### Return type

[**ResponseDTO**](ResponseDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


# PassApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createOrUpdatePass**](PassApi.md#createOrUpdatePass) | **POST** /pass | This method creates or (if the pass id already exists) updates a pass, so you don&#39;t have to track ids and creation status of your passes.
[**deletePass**](PassApi.md#deletePass) | **DELETE** /pass | Delete pass by pass id.
[**getPass**](PassApi.md#getPass) | **GET** /pass | Get pass information by pass id.
[**passList**](PassApi.md#passList) | **GET** /pass/list | Retrieve the list of active pass ids for a given pass type.
[**passSync**](PassApi.md#passSync) | **POST** /pass/sync | Send updates to all active passes for a given pass type.


<a name="createOrUpdatePass"></a>
# **createOrUpdatePass**
> createOrUpdatePass(passTypeId, passId)

This method creates or (if the pass id already exists) updates a pass, so you don&#39;t have to track ids and creation status of your passes.

This method creates or (if the pass id already exists) updates a pass, so you don&#39;t have to track ids and creation status of your passes.

### Example
```kotlin
// Import classes:
//import io.swagger.client.infrastructure.*
//import io.swagger.client.models.*

val apiInstance = PassApi()
val passTypeId : kotlin.Any =  // kotlin.Any | your pass type id, for example P963493 (Urban Fitness)
val passId : kotlin.Any =  // kotlin.Any | id of the pass (provided by you when creating the pass or automatically set by passmeister)
try {
    apiInstance.createOrUpdatePass(passTypeId, passId)
} catch (e: ClientException) {
    println("4xx response calling PassApi#createOrUpdatePass")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PassApi#createOrUpdatePass")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **passTypeId** | [**kotlin.Any**](.md)| your pass type id, for example P963493 (Urban Fitness) |
 **passId** | [**kotlin.Any**](.md)| id of the pass (provided by you when creating the pass or automatically set by passmeister) | [optional]

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a name="deletePass"></a>
# **deletePass**
> deletePass(passTypeId, passId)

Delete pass by pass id.

Delete pass by pass id.

### Example
```kotlin
// Import classes:
//import io.swagger.client.infrastructure.*
//import io.swagger.client.models.*

val apiInstance = PassApi()
val passTypeId : kotlin.Any =  // kotlin.Any | your pass type id, for example P963493 (Urban Fitness)
val passId : kotlin.Any =  // kotlin.Any | id of the pass
try {
    apiInstance.deletePass(passTypeId, passId)
} catch (e: ClientException) {
    println("4xx response calling PassApi#deletePass")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PassApi#deletePass")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **passTypeId** | [**kotlin.Any**](.md)| your pass type id, for example P963493 (Urban Fitness) |
 **passId** | [**kotlin.Any**](.md)| id of the pass |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a name="getPass"></a>
# **getPass**
> getPass(passTypeId, passId)

Get pass information by pass id.

Get pass information by pass id.

### Example
```kotlin
// Import classes:
//import io.swagger.client.infrastructure.*
//import io.swagger.client.models.*

val apiInstance = PassApi()
val passTypeId : kotlin.Any =  // kotlin.Any | your pass type id, for example P963493 (Urban Fitness)
val passId : kotlin.Any =  // kotlin.Any | id of the pass
try {
    apiInstance.getPass(passTypeId, passId)
} catch (e: ClientException) {
    println("4xx response calling PassApi#getPass")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PassApi#getPass")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **passTypeId** | [**kotlin.Any**](.md)| your pass type id, for example P963493 (Urban Fitness) |
 **passId** | [**kotlin.Any**](.md)| id of the pass |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a name="passList"></a>
# **passList**
> passList(passTypeId, page, limit)

Retrieve the list of active pass ids for a given pass type.

Retrieve the list of active pass ids for a given pass type.

### Example
```kotlin
// Import classes:
//import io.swagger.client.infrastructure.*
//import io.swagger.client.models.*

val apiInstance = PassApi()
val passTypeId : kotlin.Any =  // kotlin.Any | your pass type id, for example P963493 (Urban Fitness)
val page : kotlin.Any =  // kotlin.Any | 
val limit : kotlin.Any =  // kotlin.Any | 
try {
    apiInstance.passList(passTypeId, page, limit)
} catch (e: ClientException) {
    println("4xx response calling PassApi#passList")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PassApi#passList")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **passTypeId** | [**kotlin.Any**](.md)| your pass type id, for example P963493 (Urban Fitness) |
 **page** | [**kotlin.Any**](.md)|  | [optional]
 **limit** | [**kotlin.Any**](.md)|  | [optional]

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a name="passSync"></a>
# **passSync**
> passSync(passTypeId)

Send updates to all active passes for a given pass type.

For example: you changed the pass type layout and now you want to update all installed passes. (The API call only confirms the scheduling of the updates, actual updating of passes on your customers devices can take a while.)

### Example
```kotlin
// Import classes:
//import io.swagger.client.infrastructure.*
//import io.swagger.client.models.*

val apiInstance = PassApi()
val passTypeId : kotlin.Any =  // kotlin.Any | your pass type id, for example P963493 (Urban Fitness)
try {
    apiInstance.passSync(passTypeId)
} catch (e: ClientException) {
    println("4xx response calling PassApi#passSync")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PassApi#passSync")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **passTypeId** | [**kotlin.Any**](.md)| your pass type id, for example P963493 (Urban Fitness) |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


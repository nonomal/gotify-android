# ApplicationApi

All URIs are relative to *http://localhost/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createApp**](ApplicationApi.md#createApp) | **POST** application | Create an application.
[**deleteApp**](ApplicationApi.md#deleteApp) | **DELETE** application/{id} | Delete an application.
[**getApps**](ApplicationApi.md#getApps) | **GET** application | Return all applications.
[**removeAppImage**](ApplicationApi.md#removeAppImage) | **DELETE** application/{id}/image | Deletes an image of an application.
[**updateApplication**](ApplicationApi.md#updateApplication) | **PUT** application/{id} | Update an application.
[**uploadAppImage**](ApplicationApi.md#uploadAppImage) | **POST** application/{id}/image | Upload an image for an application.

<a name="createApp"></a>
# **createApp**
> Application createApp(body)

Create an application.

### Example
```java
// Import classes:
//import com.github.gotify.client.ApiClient;
//import com.github.gotify.client.ApiException;
//import com.github.gotify.client.Configuration;
//import com.github.gotify.client.auth.*;
//import com.github.gotify.client.api.ApplicationApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();
// Configure HTTP basic authorization: basicAuth
HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
basicAuth.setUsername("YOUR USERNAME");
basicAuth.setPassword("YOUR PASSWORD");

// Configure API key authorization: clientTokenAuthorizationHeader
ApiKeyAuth clientTokenAuthorizationHeader = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenAuthorizationHeader");
clientTokenAuthorizationHeader.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenAuthorizationHeader.setApiKeyPrefix("Token");

// Configure API key authorization: clientTokenHeader
ApiKeyAuth clientTokenHeader = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenHeader");
clientTokenHeader.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenHeader.setApiKeyPrefix("Token");

// Configure API key authorization: clientTokenQuery
ApiKeyAuth clientTokenQuery = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenQuery");
clientTokenQuery.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenQuery.setApiKeyPrefix("Token");

ApplicationApi apiInstance = new ApplicationApi();
ApplicationParams body = new ApplicationParams(); // ApplicationParams | the application to add
try {
    Application result = apiInstance.createApp(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ApplicationApi#createApp");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ApplicationParams**](ApplicationParams.md)| the application to add |

### Return type

[**Application**](Application.md)

### Authorization

[basicAuth](../README.md#basicAuth)[clientTokenAuthorizationHeader](../README.md#clientTokenAuthorizationHeader)[clientTokenHeader](../README.md#clientTokenHeader)[clientTokenQuery](../README.md#clientTokenQuery)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="deleteApp"></a>
# **deleteApp**
> Void deleteApp(id)

Delete an application.

### Example
```java
// Import classes:
//import com.github.gotify.client.ApiClient;
//import com.github.gotify.client.ApiException;
//import com.github.gotify.client.Configuration;
//import com.github.gotify.client.auth.*;
//import com.github.gotify.client.api.ApplicationApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();
// Configure HTTP basic authorization: basicAuth
HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
basicAuth.setUsername("YOUR USERNAME");
basicAuth.setPassword("YOUR PASSWORD");

// Configure API key authorization: clientTokenAuthorizationHeader
ApiKeyAuth clientTokenAuthorizationHeader = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenAuthorizationHeader");
clientTokenAuthorizationHeader.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenAuthorizationHeader.setApiKeyPrefix("Token");

// Configure API key authorization: clientTokenHeader
ApiKeyAuth clientTokenHeader = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenHeader");
clientTokenHeader.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenHeader.setApiKeyPrefix("Token");

// Configure API key authorization: clientTokenQuery
ApiKeyAuth clientTokenQuery = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenQuery");
clientTokenQuery.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenQuery.setApiKeyPrefix("Token");

ApplicationApi apiInstance = new ApplicationApi();
Long id = 789L; // Long | the application id
try {
    Void result = apiInstance.deleteApp(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ApplicationApi#deleteApp");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Long**| the application id |

### Return type

[**Void**](.md)

### Authorization

[basicAuth](../README.md#basicAuth)[clientTokenAuthorizationHeader](../README.md#clientTokenAuthorizationHeader)[clientTokenHeader](../README.md#clientTokenHeader)[clientTokenQuery](../README.md#clientTokenQuery)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getApps"></a>
# **getApps**
> List&lt;Application&gt; getApps()

Return all applications.

### Example
```java
// Import classes:
//import com.github.gotify.client.ApiClient;
//import com.github.gotify.client.ApiException;
//import com.github.gotify.client.Configuration;
//import com.github.gotify.client.auth.*;
//import com.github.gotify.client.api.ApplicationApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();
// Configure HTTP basic authorization: basicAuth
HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
basicAuth.setUsername("YOUR USERNAME");
basicAuth.setPassword("YOUR PASSWORD");

// Configure API key authorization: clientTokenAuthorizationHeader
ApiKeyAuth clientTokenAuthorizationHeader = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenAuthorizationHeader");
clientTokenAuthorizationHeader.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenAuthorizationHeader.setApiKeyPrefix("Token");

// Configure API key authorization: clientTokenHeader
ApiKeyAuth clientTokenHeader = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenHeader");
clientTokenHeader.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenHeader.setApiKeyPrefix("Token");

// Configure API key authorization: clientTokenQuery
ApiKeyAuth clientTokenQuery = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenQuery");
clientTokenQuery.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenQuery.setApiKeyPrefix("Token");

ApplicationApi apiInstance = new ApplicationApi();
try {
    List<Application> result = apiInstance.getApps();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ApplicationApi#getApps");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**List&lt;Application&gt;**](Application.md)

### Authorization

[basicAuth](../README.md#basicAuth)[clientTokenAuthorizationHeader](../README.md#clientTokenAuthorizationHeader)[clientTokenHeader](../README.md#clientTokenHeader)[clientTokenQuery](../README.md#clientTokenQuery)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="removeAppImage"></a>
# **removeAppImage**
> Void removeAppImage(id)

Deletes an image of an application.

### Example
```java
// Import classes:
//import com.github.gotify.client.ApiClient;
//import com.github.gotify.client.ApiException;
//import com.github.gotify.client.Configuration;
//import com.github.gotify.client.auth.*;
//import com.github.gotify.client.api.ApplicationApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();
// Configure HTTP basic authorization: basicAuth
HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
basicAuth.setUsername("YOUR USERNAME");
basicAuth.setPassword("YOUR PASSWORD");

// Configure API key authorization: clientTokenAuthorizationHeader
ApiKeyAuth clientTokenAuthorizationHeader = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenAuthorizationHeader");
clientTokenAuthorizationHeader.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenAuthorizationHeader.setApiKeyPrefix("Token");

// Configure API key authorization: clientTokenHeader
ApiKeyAuth clientTokenHeader = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenHeader");
clientTokenHeader.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenHeader.setApiKeyPrefix("Token");

// Configure API key authorization: clientTokenQuery
ApiKeyAuth clientTokenQuery = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenQuery");
clientTokenQuery.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenQuery.setApiKeyPrefix("Token");

ApplicationApi apiInstance = new ApplicationApi();
Long id = 789L; // Long | the application id
try {
    Void result = apiInstance.removeAppImage(id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ApplicationApi#removeAppImage");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Long**| the application id |

### Return type

[**Void**](.md)

### Authorization

[basicAuth](../README.md#basicAuth)[clientTokenAuthorizationHeader](../README.md#clientTokenAuthorizationHeader)[clientTokenHeader](../README.md#clientTokenHeader)[clientTokenQuery](../README.md#clientTokenQuery)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="updateApplication"></a>
# **updateApplication**
> Application updateApplication(body, id)

Update an application.

### Example
```java
// Import classes:
//import com.github.gotify.client.ApiClient;
//import com.github.gotify.client.ApiException;
//import com.github.gotify.client.Configuration;
//import com.github.gotify.client.auth.*;
//import com.github.gotify.client.api.ApplicationApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();
// Configure HTTP basic authorization: basicAuth
HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
basicAuth.setUsername("YOUR USERNAME");
basicAuth.setPassword("YOUR PASSWORD");

// Configure API key authorization: clientTokenAuthorizationHeader
ApiKeyAuth clientTokenAuthorizationHeader = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenAuthorizationHeader");
clientTokenAuthorizationHeader.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenAuthorizationHeader.setApiKeyPrefix("Token");

// Configure API key authorization: clientTokenHeader
ApiKeyAuth clientTokenHeader = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenHeader");
clientTokenHeader.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenHeader.setApiKeyPrefix("Token");

// Configure API key authorization: clientTokenQuery
ApiKeyAuth clientTokenQuery = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenQuery");
clientTokenQuery.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenQuery.setApiKeyPrefix("Token");

ApplicationApi apiInstance = new ApplicationApi();
ApplicationParams body = new ApplicationParams(); // ApplicationParams | the application to update
Long id = 789L; // Long | the application id
try {
    Application result = apiInstance.updateApplication(body, id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ApplicationApi#updateApplication");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ApplicationParams**](ApplicationParams.md)| the application to update |
 **id** | **Long**| the application id |

### Return type

[**Application**](Application.md)

### Authorization

[basicAuth](../README.md#basicAuth)[clientTokenAuthorizationHeader](../README.md#clientTokenAuthorizationHeader)[clientTokenHeader](../README.md#clientTokenHeader)[clientTokenQuery](../README.md#clientTokenQuery)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="uploadAppImage"></a>
# **uploadAppImage**
> Application uploadAppImage(file, id)

Upload an image for an application.

### Example
```java
// Import classes:
//import com.github.gotify.client.ApiClient;
//import com.github.gotify.client.ApiException;
//import com.github.gotify.client.Configuration;
//import com.github.gotify.client.auth.*;
//import com.github.gotify.client.api.ApplicationApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();
// Configure HTTP basic authorization: basicAuth
HttpBasicAuth basicAuth = (HttpBasicAuth) defaultClient.getAuthentication("basicAuth");
basicAuth.setUsername("YOUR USERNAME");
basicAuth.setPassword("YOUR PASSWORD");

// Configure API key authorization: clientTokenAuthorizationHeader
ApiKeyAuth clientTokenAuthorizationHeader = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenAuthorizationHeader");
clientTokenAuthorizationHeader.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenAuthorizationHeader.setApiKeyPrefix("Token");

// Configure API key authorization: clientTokenHeader
ApiKeyAuth clientTokenHeader = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenHeader");
clientTokenHeader.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenHeader.setApiKeyPrefix("Token");

// Configure API key authorization: clientTokenQuery
ApiKeyAuth clientTokenQuery = (ApiKeyAuth) defaultClient.getAuthentication("clientTokenQuery");
clientTokenQuery.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//clientTokenQuery.setApiKeyPrefix("Token");

ApplicationApi apiInstance = new ApplicationApi();
File file = new File("file_example"); // File | 
Long id = 789L; // Long | the application id
try {
    Application result = apiInstance.uploadAppImage(file, id);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ApplicationApi#uploadAppImage");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **File**|  |
 **id** | **Long**| the application id |

### Return type

[**Application**](Application.md)

### Authorization

[basicAuth](../README.md#basicAuth)[clientTokenAuthorizationHeader](../README.md#clientTokenAuthorizationHeader)[clientTokenHeader](../README.md#clientTokenHeader)[clientTokenQuery](../README.md#clientTokenQuery)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


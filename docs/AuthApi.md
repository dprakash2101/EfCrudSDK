# efcrud.AuthApi

All URIs are relative to *https://localhost:7217*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_auth_login_post**](AuthApi.md#api_auth_login_post) | **POST** /api/Auth/login | 
[**api_auth_register_post**](AuthApi.md#api_auth_register_post) | **POST** /api/Auth/register | 


# **api_auth_login_post**
> User api_auth_login_post(userdto=userdto)



### Example

```python
import time
import os
import efcrud
from efcrud.models.user import User
from efcrud.models.userdto import Userdto
from efcrud.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://localhost:7217
# See configuration.py for a list of all supported configuration parameters.
configuration = efcrud.Configuration(
    host = "https://localhost:7217"
)


# Enter a context with an instance of the API client
with efcrud.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = efcrud.AuthApi(api_client)
    userdto = efcrud.Userdto() # Userdto |  (optional)

    try:
        api_response = api_instance.api_auth_login_post(userdto=userdto)
        print("The response of AuthApi->api_auth_login_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->api_auth_login_post: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **userdto** | [**Userdto**](Userdto.md)|  | [optional] 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_auth_register_post**
> User api_auth_register_post(role=role, userdto=userdto)



### Example

```python
import time
import os
import efcrud
from efcrud.models.user import User
from efcrud.models.userdto import Userdto
from efcrud.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://localhost:7217
# See configuration.py for a list of all supported configuration parameters.
configuration = efcrud.Configuration(
    host = "https://localhost:7217"
)


# Enter a context with an instance of the API client
with efcrud.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = efcrud.AuthApi(api_client)
    role = 'role_example' # str |  (optional)
    userdto = efcrud.Userdto() # Userdto |  (optional)

    try:
        api_response = api_instance.api_auth_register_post(role=role, userdto=userdto)
        print("The response of AuthApi->api_auth_register_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->api_auth_register_post: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **role** | **str**|  | [optional] 
 **userdto** | [**Userdto**](Userdto.md)|  | [optional] 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


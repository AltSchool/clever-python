# swagger_client.LMSConnectApi

All URIs are relative to *https://api.clever.com/v3.1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_assignment_for_section**](LMSConnectApi.md#create_assignment_for_section) | **POST** /sections/{section_id}/assignments | 
[**delete_assignment_for_section**](LMSConnectApi.md#delete_assignment_for_section) | **DELETE** /sections/{section_id}/assignments/{assignment_id} | 
[**get_assignment_for_section**](LMSConnectApi.md#get_assignment_for_section) | **GET** /sections/{section_id}/assignments/{assignment_id} | 
[**get_submission_for_assignment**](LMSConnectApi.md#get_submission_for_assignment) | **GET** /sections/{section_id}/assignments/{assignment_id}/submissions/{user_id} | 
[**get_submissions_for_assignment**](LMSConnectApi.md#get_submissions_for_assignment) | **GET** /sections/{section_id}/assignments/{assignment_id}/submissions | 
[**update_assignment_for_section**](LMSConnectApi.md#update_assignment_for_section) | **PATCH** /sections/{section_id}/assignments/{assignment_id} | 
[**update_submission_for_assignment**](LMSConnectApi.md#update_submission_for_assignment) | **PATCH** /sections/{section_id}/assignments/{assignment_id}/submissions/{user_id} | 


# **create_assignment_for_section**
> AssignmentResponse create_assignment_for_section(section_id, assignment_request_body)



Creates a new assignment in the specified section

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: oauth
configuration = swagger_client.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = swagger_client.LMSConnectApi(swagger_client.ApiClient(configuration))
section_id = 'section_id_example' # str | 
assignment_request_body = swagger_client.AssignmentRequest() # AssignmentRequest | 

try:
    api_response = api_instance.create_assignment_for_section(section_id, assignment_request_body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LMSConnectApi->create_assignment_for_section: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **section_id** | **str**|  | 
 **assignment_request_body** | [**AssignmentRequest**](AssignmentRequest.md)|  | 

### Return type

[**AssignmentResponse**](AssignmentResponse.md)

### Authorization

[oauth](../README.md#oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_assignment_for_section**
> delete_assignment_for_section(section_id, assignment_id)



Deletes an existing assignment in the specified section

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: oauth
configuration = swagger_client.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = swagger_client.LMSConnectApi(swagger_client.ApiClient(configuration))
section_id = 'section_id_example' # str | 
assignment_id = 'assignment_id_example' # str | 

try:
    api_instance.delete_assignment_for_section(section_id, assignment_id)
except ApiException as e:
    print("Exception when calling LMSConnectApi->delete_assignment_for_section: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **section_id** | **str**|  | 
 **assignment_id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[oauth](../README.md#oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_assignment_for_section**
> AssignmentResponse get_assignment_for_section(section_id, assignment_id)



Returns a specific assignment for a section

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: oauth
configuration = swagger_client.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = swagger_client.LMSConnectApi(swagger_client.ApiClient(configuration))
section_id = 'section_id_example' # str | 
assignment_id = 'assignment_id_example' # str | 

try:
    api_response = api_instance.get_assignment_for_section(section_id, assignment_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LMSConnectApi->get_assignment_for_section: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **section_id** | **str**|  | 
 **assignment_id** | **str**|  | 

### Return type

[**AssignmentResponse**](AssignmentResponse.md)

### Authorization

[oauth](../README.md#oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_submission_for_assignment**
> SubmissionResponse get_submission_for_assignment(section_id, assignment_id, user_id)



Returns a specific user's submission for an assignment.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: oauth
configuration = swagger_client.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = swagger_client.LMSConnectApi(swagger_client.ApiClient(configuration))
section_id = 'section_id_example' # str | 
assignment_id = 'assignment_id_example' # str | 
user_id = 'user_id_example' # str | 

try:
    api_response = api_instance.get_submission_for_assignment(section_id, assignment_id, user_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LMSConnectApi->get_submission_for_assignment: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **section_id** | **str**|  | 
 **assignment_id** | **str**|  | 
 **user_id** | **str**|  | 

### Return type

[**SubmissionResponse**](SubmissionResponse.md)

### Authorization

[oauth](../README.md#oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_submissions_for_assignment**
> SubmissionsResponse get_submissions_for_assignment(section_id, assignment_id, cursor=cursor, limit=limit)



Returns the submissions for an assignment.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: oauth
configuration = swagger_client.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = swagger_client.LMSConnectApi(swagger_client.ApiClient(configuration))
section_id = 'section_id_example' # str | 
assignment_id = 'assignment_id_example' # str | 
cursor = 'cursor_example' # str |  (optional)
limit = 56 # int |  (optional)

try:
    api_response = api_instance.get_submissions_for_assignment(section_id, assignment_id, cursor=cursor, limit=limit)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LMSConnectApi->get_submissions_for_assignment: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **section_id** | **str**|  | 
 **assignment_id** | **str**|  | 
 **cursor** | **str**|  | [optional] 
 **limit** | **int**|  | [optional] 

### Return type

[**SubmissionsResponse**](SubmissionsResponse.md)

### Authorization

[oauth](../README.md#oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_assignment_for_section**
> AssignmentResponse update_assignment_for_section(section_id, assignment_id, assignment_request_body)



Updates an existing assignment in the specified section

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: oauth
configuration = swagger_client.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = swagger_client.LMSConnectApi(swagger_client.ApiClient(configuration))
section_id = 'section_id_example' # str | 
assignment_id = 'assignment_id_example' # str | 
assignment_request_body = swagger_client.AssignmentRequest() # AssignmentRequest | 

try:
    api_response = api_instance.update_assignment_for_section(section_id, assignment_id, assignment_request_body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LMSConnectApi->update_assignment_for_section: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **section_id** | **str**|  | 
 **assignment_id** | **str**|  | 
 **assignment_request_body** | [**AssignmentRequest**](AssignmentRequest.md)|  | 

### Return type

[**AssignmentResponse**](AssignmentResponse.md)

### Authorization

[oauth](../README.md#oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_submission_for_assignment**
> SubmissionResponse update_submission_for_assignment(section_id, assignment_id, user_id, submission_request_body)



Updates an existing submission in the specified assignment for a user.

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: oauth
configuration = swagger_client.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = swagger_client.LMSConnectApi(swagger_client.ApiClient(configuration))
section_id = 'section_id_example' # str | 
assignment_id = 'assignment_id_example' # str | 
user_id = 'user_id_example' # str | 
submission_request_body = swagger_client.SubmissionRequest() # SubmissionRequest | 

try:
    api_response = api_instance.update_submission_for_assignment(section_id, assignment_id, user_id, submission_request_body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LMSConnectApi->update_submission_for_assignment: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **section_id** | **str**|  | 
 **assignment_id** | **str**|  | 
 **user_id** | **str**|  | 
 **submission_request_body** | [**SubmissionRequest**](SubmissionRequest.md)|  | 

### Return type

[**SubmissionResponse**](SubmissionResponse.md)

### Authorization

[oauth](../README.md#oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


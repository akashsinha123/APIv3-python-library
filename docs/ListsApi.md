# sib_api_v3_sdk.ListsApi

All URIs are relative to *https://api.sendinblue.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_contact_to_list**](ListsApi.md#add_contact_to_list) | **POST** /contacts/lists/{listId}/contacts/add | Add existing contacts to a list
[**create_list**](ListsApi.md#create_list) | **POST** /contacts/lists | Create a list
[**delete_list**](ListsApi.md#delete_list) | **DELETE** /contacts/lists/{listId} | Delete a list
[**get_contacts_from_list**](ListsApi.md#get_contacts_from_list) | **GET** /contacts/lists/{listId}/contacts | Get the contacts in a list
[**get_folder_lists**](ListsApi.md#get_folder_lists) | **GET** /contacts/folders/{folderId}/lists | Get the lists in a folder
[**get_list**](ListsApi.md#get_list) | **GET** /contacts/lists/{listId} | Get the details of a list
[**get_lists**](ListsApi.md#get_lists) | **GET** /contacts/lists | Get all the lists
[**remove_contact_to_list**](ListsApi.md#remove_contact_to_list) | **POST** /contacts/lists/{listId}/contacts/remove | Remove existing contacts from a list
[**update_list**](ListsApi.md#update_list) | **PUT** /contacts/lists/{listId} | Update a list


# **add_contact_to_list**
> PostContactInfo add_contact_to_list(list_id, contact_emails)

Add existing contacts to a list

### Example 
```python
from __future__ import print_function
import time
import sib_api_v3_sdk
from sib_api_v3_sdk.rest import ApiException
from pprint import pprint

# Configure API key authorization: api-key
sib_api_v3_sdk.configuration.api_key['api-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# sib_api_v3_sdk.configuration.api_key_prefix['api-key'] = 'Bearer'

# create an instance of the API class
api_instance = sib_api_v3_sdk.ListsApi()
list_id = 'list_id_example' # str | Id of the list
contact_emails = sib_api_v3_sdk.AddRemoveContactToList() # AddRemoveContactToList | Emails addresses of the contacts

try: 
    # Add existing contacts to a list
    api_response = api_instance.add_contact_to_list(list_id, contact_emails)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ListsApi->add_contact_to_list: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **list_id** | **str**| Id of the list | 
 **contact_emails** | [**AddRemoveContactToList**](AddRemoveContactToList.md)| Emails addresses of the contacts | 

### Return type

[**PostContactInfo**](PostContactInfo.md)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_list**
> CreateModel create_list(create_list)

Create a list

### Example 
```python
from __future__ import print_function
import time
import sib_api_v3_sdk
from sib_api_v3_sdk.rest import ApiException
from pprint import pprint

# Configure API key authorization: api-key
sib_api_v3_sdk.configuration.api_key['api-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# sib_api_v3_sdk.configuration.api_key_prefix['api-key'] = 'Bearer'

# create an instance of the API class
api_instance = sib_api_v3_sdk.ListsApi()
create_list = sib_api_v3_sdk.CreateList() # CreateList | Values to create a list

try: 
    # Create a list
    api_response = api_instance.create_list(create_list)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ListsApi->create_list: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_list** | [**CreateList**](CreateList.md)| Values to create a list | 

### Return type

[**CreateModel**](CreateModel.md)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_list**
> delete_list(list_id)

Delete a list

### Example 
```python
from __future__ import print_function
import time
import sib_api_v3_sdk
from sib_api_v3_sdk.rest import ApiException
from pprint import pprint

# Configure API key authorization: api-key
sib_api_v3_sdk.configuration.api_key['api-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# sib_api_v3_sdk.configuration.api_key_prefix['api-key'] = 'Bearer'

# create an instance of the API class
api_instance = sib_api_v3_sdk.ListsApi()
list_id = 'list_id_example' # str | Id of the list

try: 
    # Delete a list
    api_instance.delete_list(list_id)
except ApiException as e:
    print("Exception when calling ListsApi->delete_list: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **list_id** | **str**| Id of the list | 

### Return type

void (empty response body)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_contacts_from_list**
> GetContacts get_contacts_from_list(list_id, modified_since=modified_since, limit=limit, offset=offset)

Get the contacts in a list

### Example 
```python
from __future__ import print_function
import time
import sib_api_v3_sdk
from sib_api_v3_sdk.rest import ApiException
from pprint import pprint

# Configure API key authorization: api-key
sib_api_v3_sdk.configuration.api_key['api-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# sib_api_v3_sdk.configuration.api_key_prefix['api-key'] = 'Bearer'

# create an instance of the API class
api_instance = sib_api_v3_sdk.ListsApi()
list_id = 'list_id_example' # str | Id of the list
modified_since = 'modified_since_example' # str | Filter the contacts modified after a given date (YYYY-MM-DD HH:mm:ss) (optional)
limit = 50 # int | Number of documents per page (optional) (default to 50)
offset = 0 # int | Index of the first document of the page (optional) (default to 0)

try: 
    # Get the contacts in a list
    api_response = api_instance.get_contacts_from_list(list_id, modified_since=modified_since, limit=limit, offset=offset)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ListsApi->get_contacts_from_list: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **list_id** | **str**| Id of the list | 
 **modified_since** | **str**| Filter the contacts modified after a given date (YYYY-MM-DD HH:mm:ss) | [optional] 
 **limit** | **int**| Number of documents per page | [optional] [default to 50]
 **offset** | **int**| Index of the first document of the page | [optional] [default to 0]

### Return type

[**GetContacts**](GetContacts.md)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_folder_lists**
> GetFolderLists get_folder_lists(folder_id, limit=limit, offset=offset)

Get the lists in a folder

### Example 
```python
from __future__ import print_function
import time
import sib_api_v3_sdk
from sib_api_v3_sdk.rest import ApiException
from pprint import pprint

# Configure API key authorization: api-key
sib_api_v3_sdk.configuration.api_key['api-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# sib_api_v3_sdk.configuration.api_key_prefix['api-key'] = 'Bearer'

# create an instance of the API class
api_instance = sib_api_v3_sdk.ListsApi()
folder_id = 'folder_id_example' # str | Id of the folder
limit = 10 # int | Number of documents per page (optional) (default to 10)
offset = 0 # int | Index of the first document of the page (optional) (default to 0)

try: 
    # Get the lists in a folder
    api_response = api_instance.get_folder_lists(folder_id, limit=limit, offset=offset)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ListsApi->get_folder_lists: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **folder_id** | **str**| Id of the folder | 
 **limit** | **int**| Number of documents per page | [optional] [default to 10]
 **offset** | **int**| Index of the first document of the page | [optional] [default to 0]

### Return type

[**GetFolderLists**](GetFolderLists.md)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_list**
> GetExtendedList get_list(list_id)

Get the details of a list

### Example 
```python
from __future__ import print_function
import time
import sib_api_v3_sdk
from sib_api_v3_sdk.rest import ApiException
from pprint import pprint

# Configure API key authorization: api-key
sib_api_v3_sdk.configuration.api_key['api-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# sib_api_v3_sdk.configuration.api_key_prefix['api-key'] = 'Bearer'

# create an instance of the API class
api_instance = sib_api_v3_sdk.ListsApi()
list_id = 'list_id_example' # str | Id of the list

try: 
    # Get the details of a list
    api_response = api_instance.get_list(list_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ListsApi->get_list: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **list_id** | **str**| Id of the list | 

### Return type

[**GetExtendedList**](GetExtendedList.md)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_lists**
> GetLists get_lists(limit=limit, offset=offset)

Get all the lists

### Example 
```python
from __future__ import print_function
import time
import sib_api_v3_sdk
from sib_api_v3_sdk.rest import ApiException
from pprint import pprint

# Configure API key authorization: api-key
sib_api_v3_sdk.configuration.api_key['api-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# sib_api_v3_sdk.configuration.api_key_prefix['api-key'] = 'Bearer'

# create an instance of the API class
api_instance = sib_api_v3_sdk.ListsApi()
limit = 10 # int | Number of documents per page (optional) (default to 10)
offset = 0 # int | Index of the first document of the page (optional) (default to 0)

try: 
    # Get all the lists
    api_response = api_instance.get_lists(limit=limit, offset=offset)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ListsApi->get_lists: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Number of documents per page | [optional] [default to 10]
 **offset** | **int**| Index of the first document of the page | [optional] [default to 0]

### Return type

[**GetLists**](GetLists.md)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_contact_to_list**
> PostContactInfo remove_contact_to_list(list_id, contact_emails)

Remove existing contacts from a list

### Example 
```python
from __future__ import print_function
import time
import sib_api_v3_sdk
from sib_api_v3_sdk.rest import ApiException
from pprint import pprint

# Configure API key authorization: api-key
sib_api_v3_sdk.configuration.api_key['api-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# sib_api_v3_sdk.configuration.api_key_prefix['api-key'] = 'Bearer'

# create an instance of the API class
api_instance = sib_api_v3_sdk.ListsApi()
list_id = 'list_id_example' # str | Id of the list
contact_emails = sib_api_v3_sdk.AddRemoveContactToList() # AddRemoveContactToList | Emails adresses of the contact

try: 
    # Remove existing contacts from a list
    api_response = api_instance.remove_contact_to_list(list_id, contact_emails)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ListsApi->remove_contact_to_list: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **list_id** | **str**| Id of the list | 
 **contact_emails** | [**AddRemoveContactToList**](AddRemoveContactToList.md)| Emails adresses of the contact | 

### Return type

[**PostContactInfo**](PostContactInfo.md)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_list**
> update_list(list_id, update_list)

Update a list

### Example 
```python
from __future__ import print_function
import time
import sib_api_v3_sdk
from sib_api_v3_sdk.rest import ApiException
from pprint import pprint

# Configure API key authorization: api-key
sib_api_v3_sdk.configuration.api_key['api-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# sib_api_v3_sdk.configuration.api_key_prefix['api-key'] = 'Bearer'

# create an instance of the API class
api_instance = sib_api_v3_sdk.ListsApi()
list_id = 'list_id_example' # str | Id of the list
update_list = sib_api_v3_sdk.UpdateList() # UpdateList | Values to update a list

try: 
    # Update a list
    api_instance.update_list(list_id, update_list)
except ApiException as e:
    print("Exception when calling ListsApi->update_list: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **list_id** | **str**| Id of the list | 
 **update_list** | [**UpdateList**](UpdateList.md)| Values to update a list | 

### Return type

void (empty response body)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

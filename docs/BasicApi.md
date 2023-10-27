# {{classname}}

All URIs are relative to *https://tdx.transportdata.tw/api/basic*

Method | HTTP request | Description
------------- | ------------- | -------------
[**BasicGetCity**](BasicApi.md#BasicGetCity) | **Get** /v2/Basic/City | 取得[縣市]之City列表
[**BasicGetCityTown**](BasicApi.md#BasicGetCityTown) | **Get** /v2/Basic/City/{City}/Town | 取得指定[縣市(City)]之鄉鎮市區列表
[**BasicGetCityVillage**](BasicApi.md#BasicGetCityVillage) | **Get** /v2/Basic/City/{City}/Village | 取得指定[縣市(City)]之村里列表
[**BasicGetCounty**](BasicApi.md#BasicGetCounty) | **Get** /v2/Basic/County | 取得[縣市]之County列表
[**BasicGetCountyTown**](BasicApi.md#BasicGetCountyTown) | **Get** /v2/Basic/County/{County}/Town | 取得指定[縣市(County)]之鄉鎮市區列表
[**BasicGetCountyVillage**](BasicApi.md#BasicGetCountyVillage) | **Get** /v2/Basic/County/{County}/Village | 取得指定[縣市(County)]之村里列表

# **BasicGetCity**
> ArrayOfCity BasicGetCity(ctx, format, optional)
取得[縣市]之City列表

取得[縣市]之City列表

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **format** | **string**| 指定來源格式 | 
 **optional** | ***BasicApiBasicGetCityOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a BasicApiBasicGetCityOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **select_** | **optional.String**| 挑選 | 
 **filter** | **optional.String**| 過濾 | 
 **orderby** | **optional.String**| 排序 | 
 **top** | **optional.Int32**| 取前幾筆 | 
 **skip** | **optional.Int32**| 跳過前幾筆 | 

### Return type

[**ArrayOfCity**](ArrayOfCity.md)

### Authorization

[TDX](../README.md#TDX)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **BasicGetCityTown**
> ArrayOfTown BasicGetCityTown(ctx, city, format, optional)
取得指定[縣市(City)]之鄉鎮市區列表

取得指定[縣市(City)]之鄉鎮市區列表<br />  TownCode以內政部戶政司制定代碼之前7碼作為鄉鎮市區之唯一代碼。第8碼原則為0，完整8碼請至內政部戶政司網站( https://www.ris.gov.tw/app/portal/164 )戶役政資料代碼內容查詢。

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **city** | **string**| 縣市(英文)&lt;br&gt;Taipei &#x3D; 臺北市, &lt;br&gt;Taichung &#x3D; 臺中市, &lt;br&gt;Keelung &#x3D; 基隆市, &lt;br&gt;Tainan &#x3D; 臺南市, &lt;br&gt;Kaohsiung &#x3D; 高雄市, &lt;br&gt;NewTaipei &#x3D; 新北市, &lt;br&gt;YilanCounty &#x3D; 宜蘭縣, &lt;br&gt;Taoyuan &#x3D; 桃園市, &lt;br&gt;Chiayi &#x3D; 嘉義市, &lt;br&gt;HsinchuCounty &#x3D; 新竹縣, &lt;br&gt;MiaoliCounty &#x3D; 苗栗縣, &lt;br&gt;NantouCounty &#x3D; 南投縣, &lt;br&gt;ChanghuaCounty &#x3D; 彰化縣, &lt;br&gt;Hsinchu &#x3D; 新竹市, &lt;br&gt;YunlinCounty &#x3D; 雲林縣, &lt;br&gt;ChiayiCounty &#x3D; 嘉義縣, &lt;br&gt;PingtungCounty &#x3D; 屏東縣, &lt;br&gt;HualienCounty &#x3D; 花蓮縣, &lt;br&gt;TaitungCounty &#x3D; 臺東縣, &lt;br&gt;KinmenCounty &#x3D; 金門縣, &lt;br&gt;PenghuCounty &#x3D; 澎湖縣, &lt;br&gt;LienchiangCounty &#x3D; 連江縣 | 
  **format** | **string**| 指定來源格式 | 
 **optional** | ***BasicApiBasicGetCityTownOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a BasicApiBasicGetCityTownOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **select_** | **optional.String**| 挑選 | 
 **filter** | **optional.String**| 過濾 | 
 **orderby** | **optional.String**| 排序 | 
 **top** | **optional.Int32**| 取前幾筆 | 
 **skip** | **optional.Int32**| 跳過前幾筆 | 

### Return type

[**ArrayOfTown**](ArrayOfTown.md)

### Authorization

[TDX](../README.md#TDX)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **BasicGetCityVillage**
> ArrayOfVillage BasicGetCityVillage(ctx, city, format, optional)
取得指定[縣市(City)]之村里列表

取得指定[縣市(City)]之村里列表

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **city** | **string**| 縣市(英文)&lt;br&gt;Taipei &#x3D; 臺北市, &lt;br&gt;Taichung &#x3D; 臺中市, &lt;br&gt;Keelung &#x3D; 基隆市, &lt;br&gt;Tainan &#x3D; 臺南市, &lt;br&gt;Kaohsiung &#x3D; 高雄市, &lt;br&gt;NewTaipei &#x3D; 新北市, &lt;br&gt;YilanCounty &#x3D; 宜蘭縣, &lt;br&gt;Taoyuan &#x3D; 桃園市, &lt;br&gt;Chiayi &#x3D; 嘉義市, &lt;br&gt;HsinchuCounty &#x3D; 新竹縣, &lt;br&gt;MiaoliCounty &#x3D; 苗栗縣, &lt;br&gt;NantouCounty &#x3D; 南投縣, &lt;br&gt;ChanghuaCounty &#x3D; 彰化縣, &lt;br&gt;Hsinchu &#x3D; 新竹市, &lt;br&gt;YunlinCounty &#x3D; 雲林縣, &lt;br&gt;ChiayiCounty &#x3D; 嘉義縣, &lt;br&gt;PingtungCounty &#x3D; 屏東縣, &lt;br&gt;HualienCounty &#x3D; 花蓮縣, &lt;br&gt;TaitungCounty &#x3D; 臺東縣, &lt;br&gt;KinmenCounty &#x3D; 金門縣, &lt;br&gt;PenghuCounty &#x3D; 澎湖縣, &lt;br&gt;LienchiangCounty &#x3D; 連江縣 | 
  **format** | **string**| 指定來源格式 | 
 **optional** | ***BasicApiBasicGetCityVillageOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a BasicApiBasicGetCityVillageOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **select_** | **optional.String**| 挑選 | 
 **filter** | **optional.String**| 過濾 | 
 **orderby** | **optional.String**| 排序 | 
 **top** | **optional.Int32**| 取前幾筆 | 
 **skip** | **optional.Int32**| 跳過前幾筆 | 

### Return type

[**ArrayOfVillage**](ArrayOfVillage.md)

### Authorization

[TDX](../README.md#TDX)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **BasicGetCounty**
> ArrayOfCounty BasicGetCounty(ctx, format, optional)
取得[縣市]之County列表

取得[縣市]之County列表

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **format** | **string**| 指定來源格式 | 
 **optional** | ***BasicApiBasicGetCountyOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a BasicApiBasicGetCountyOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **select_** | **optional.String**| 挑選 | 
 **filter** | **optional.String**| 過濾 | 
 **orderby** | **optional.String**| 排序 | 
 **top** | **optional.Int32**| 取前幾筆 | 
 **skip** | **optional.Int32**| 跳過前幾筆 | 

### Return type

[**ArrayOfCounty**](ArrayOfCounty.md)

### Authorization

[TDX](../README.md#TDX)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **BasicGetCountyTown**
> ArrayOfCountyTown BasicGetCountyTown(ctx, county, format, optional)
取得指定[縣市(County)]之鄉鎮市區列表

取得指定[縣市(County)]之鄉鎮市區列表<br />  TownCode以內政部戶政司制定代碼之前7碼作為鄉鎮市區之唯一代碼。第8碼原則為0，完整8碼請至內政部戶政司網站( https://www.ris.gov.tw/app/portal/164 )戶役政資料代碼內容查詢。

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **county** | **string**| 縣市(英文)&lt;br&gt;Taipei &#x3D; 臺北市, &lt;br&gt;Taichung &#x3D; 臺中市, &lt;br&gt;Keelung &#x3D; 基隆市, &lt;br&gt;Tainan &#x3D; 臺南市, &lt;br&gt;Kaohsiung &#x3D; 高雄市, &lt;br&gt;NewTaipei &#x3D; 新北市, &lt;br&gt;YilanCounty &#x3D; 宜蘭縣, &lt;br&gt;Taoyuan &#x3D; 桃園市, &lt;br&gt;Chiayi &#x3D; 嘉義市, &lt;br&gt;HsinchuCounty &#x3D; 新竹縣, &lt;br&gt;MiaoliCounty &#x3D; 苗栗縣, &lt;br&gt;NantouCounty &#x3D; 南投縣, &lt;br&gt;ChanghuaCounty &#x3D; 彰化縣, &lt;br&gt;Hsinchu &#x3D; 新竹市, &lt;br&gt;YunlinCounty &#x3D; 雲林縣, &lt;br&gt;ChiayiCounty &#x3D; 嘉義縣, &lt;br&gt;PingtungCounty &#x3D; 屏東縣, &lt;br&gt;HualienCounty &#x3D; 花蓮縣, &lt;br&gt;TaitungCounty &#x3D; 臺東縣, &lt;br&gt;KinmenCounty &#x3D; 金門縣, &lt;br&gt;PenghuCounty &#x3D; 澎湖縣, &lt;br&gt;LienchiangCounty &#x3D; 連江縣 | 
  **format** | **string**| 指定來源格式 | 
 **optional** | ***BasicApiBasicGetCountyTownOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a BasicApiBasicGetCountyTownOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **select_** | **optional.String**| 挑選 | 
 **filter** | **optional.String**| 過濾 | 
 **orderby** | **optional.String**| 排序 | 
 **top** | **optional.Int32**| 取前幾筆 | 
 **skip** | **optional.Int32**| 跳過前幾筆 | 

### Return type

[**ArrayOfCountyTown**](ArrayOfCountyTown.md)

### Authorization

[TDX](../README.md#TDX)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **BasicGetCountyVillage**
> ArrayOfCountyVillage BasicGetCountyVillage(ctx, county, format, optional)
取得指定[縣市(County)]之村里列表

取得指定[縣市(County)]之村里列表

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **county** | **string**| 縣市(英文)&lt;br&gt;Taipei &#x3D; 臺北市, &lt;br&gt;Taichung &#x3D; 臺中市, &lt;br&gt;Keelung &#x3D; 基隆市, &lt;br&gt;Tainan &#x3D; 臺南市, &lt;br&gt;Kaohsiung &#x3D; 高雄市, &lt;br&gt;NewTaipei &#x3D; 新北市, &lt;br&gt;YilanCounty &#x3D; 宜蘭縣, &lt;br&gt;Taoyuan &#x3D; 桃園市, &lt;br&gt;Chiayi &#x3D; 嘉義市, &lt;br&gt;HsinchuCounty &#x3D; 新竹縣, &lt;br&gt;MiaoliCounty &#x3D; 苗栗縣, &lt;br&gt;NantouCounty &#x3D; 南投縣, &lt;br&gt;ChanghuaCounty &#x3D; 彰化縣, &lt;br&gt;Hsinchu &#x3D; 新竹市, &lt;br&gt;YunlinCounty &#x3D; 雲林縣, &lt;br&gt;ChiayiCounty &#x3D; 嘉義縣, &lt;br&gt;PingtungCounty &#x3D; 屏東縣, &lt;br&gt;HualienCounty &#x3D; 花蓮縣, &lt;br&gt;TaitungCounty &#x3D; 臺東縣, &lt;br&gt;KinmenCounty &#x3D; 金門縣, &lt;br&gt;PenghuCounty &#x3D; 澎湖縣, &lt;br&gt;LienchiangCounty &#x3D; 連江縣 | 
  **format** | **string**| 指定來源格式 | 
 **optional** | ***BasicApiBasicGetCountyVillageOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a BasicApiBasicGetCountyVillageOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **select_** | **optional.String**| 挑選 | 
 **filter** | **optional.String**| 過濾 | 
 **orderby** | **optional.String**| 排序 | 
 **top** | **optional.Int32**| 取前幾筆 | 
 **skip** | **optional.Int32**| 跳過前幾筆 | 

### Return type

[**ArrayOfCountyVillage**](ArrayOfCountyVillage.md)

### Authorization

[TDX](../README.md#TDX)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


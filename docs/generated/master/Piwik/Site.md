<small>Piwik</small>

Site
====

Provides access to individual site data (such as name, URL, etc.).

Description
-----------

### Examples

**Basic usage**

    $site = new Site($idSite);
    $name = $site-&gt;getName();

**Without allocation**

    $name = Site::getNameFor($idSite);


Properties
----------

This class defines the following properties:

- [`$infoSites`](#$infoSites)

### `$infoSites` <a name="infoSites"></a>

#### Signature

- It is a **public static** property.
- It is a(n) `array` value.

Methods
-------

The class defines the following methods:

- [`__construct()`](#__construct) &mdash; Constructor.
- [`setSites()`](#setSites) &mdash; Sets the cached site data with an array that associates site IDs with individual site data.
- [`setSitesFromArray()`](#setSitesFromArray) &mdash; Sets the cached Site data with a non-associated array of site data.
- [`__toString()`](#__toString) &mdash; Returns a string representation of the site this instance references.
- [`getName()`](#getName) &mdash; Returns the name of the site.
- [`getMainUrl()`](#getMainUrl) &mdash; Returns the main url of the site.
- [`getId()`](#getId) &mdash; Returns the id of the site.
- [`getCreationDate()`](#getCreationDate) &mdash; Returns the creation date of the site.
- [`getTimezone()`](#getTimezone) &mdash; Returns the timezone of the size.
- [`getCurrency()`](#getCurrency) &mdash; Returns the currency of the site.
- [`getExcludedIps()`](#getExcludedIps) &mdash; Returns the excluded ips of the site.
- [`getExcludedQueryParameters()`](#getExcludedQueryParameters) &mdash; Returns the excluded query parameters of the site.
- [`isEcommerceEnabled()`](#isEcommerceEnabled) &mdash; Returns whether ecommerce is enabled for the site.
- [`getSearchKeywordParameters()`](#getSearchKeywordParameters) &mdash; Returns the site search keyword query parameters for the site.
- [`getSearchCategoryParameters()`](#getSearchCategoryParameters) &mdash; Returns the site search category query parameters for the site.
- [`isSiteSearchEnabled()`](#isSiteSearchEnabled) &mdash; Returns whether Site Search Tracking is enabled for the site.
- [`getIdSitesFromIdSitesString()`](#getIdSitesFromIdSitesString) &mdash; Checks the given string for valid site ids and returns them as an array.
- [`clearCache()`](#clearCache) &mdash; Clears the site data cache.
- [`getNameFor()`](#getNameFor) &mdash; Returns the name of the site with the specified ID.
- [`getTimezoneFor()`](#getTimezoneFor) &mdash; Returns the timezone of the site with the specified ID.
- [`getCreationDateFor()`](#getCreationDateFor) &mdash; Returns the creation date of the site with the specified ID.
- [`getMainUrlFor()`](#getMainUrlFor) &mdash; Returns the url for the site with the specified ID.
- [`isEcommerceEnabledFor()`](#isEcommerceEnabledFor) &mdash; Returns whether the site with the specified ID is ecommerce enabled
- [`isSiteSearchEnabledFor()`](#isSiteSearchEnabledFor) &mdash; Returns whether the site with the specified ID is Site Search enabled
- [`getCurrencyFor()`](#getCurrencyFor) &mdash; Returns the currency of the site with the specified ID.
- [`getExcludedIpsFor()`](#getExcludedIpsFor) &mdash; Returns the excluded IP addresses of the site with the specified ID.
- [`getExcludedQueryParametersFor()`](#getExcludedQueryParametersFor) &mdash; Returns the excluded query parameters for the site with the specified ID.

### `__construct()` <a name="__construct"></a>

Constructor.

#### Signature

- It is a **public** method.
- It accepts the following parameter(s):
    - `$idsite`
- It does not return anything.

### `setSites()` <a name="setSites"></a>

Sets the cached site data with an array that associates site IDs with individual site data.

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$sites`
- It does not return anything.

### `setSitesFromArray()` <a name="setSitesFromArray"></a>

Sets the cached Site data with a non-associated array of site data.

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$sites`
- It does not return anything.

### `__toString()` <a name="__toString"></a>

Returns a string representation of the site this instance references.

#### Description

Useful for debugging.

#### Signature

- It is a **public** method.
- It returns a(n) `string` value.

### `getName()` <a name="getName"></a>

Returns the name of the site.

#### Signature

- It is a **public** method.
- It returns a(n) `string` value.
- It throws one of the following exceptions:
    - [`Exception`](http://php.net/class.Exception) &mdash; if data for the site cannot be found.

### `getMainUrl()` <a name="getMainUrl"></a>

Returns the main url of the site.

#### Signature

- It is a **public** method.
- It returns a(n) `string` value.
- It throws one of the following exceptions:
    - [`Exception`](http://php.net/class.Exception) &mdash; if data for the site cannot be found.

### `getId()` <a name="getId"></a>

Returns the id of the site.

#### Signature

- It is a **public** method.
- It returns a(n) `int` value.
- It throws one of the following exceptions:
    - [`Exception`](http://php.net/class.Exception) &mdash; if data for the site cannot be found.

### `getCreationDate()` <a name="getCreationDate"></a>

Returns the creation date of the site.

#### Signature

- It is a **public** method.
- It returns a(n) [`Date`](../Piwik/Date.md) value.
- It throws one of the following exceptions:
    - [`Exception`](http://php.net/class.Exception) &mdash; if data for the site cannot be found.

### `getTimezone()` <a name="getTimezone"></a>

Returns the timezone of the size.

#### Signature

- It is a **public** method.
- It returns a(n) `string` value.
- It throws one of the following exceptions:
    - [`Exception`](http://php.net/class.Exception) &mdash; if data for the site cannot be found.

### `getCurrency()` <a name="getCurrency"></a>

Returns the currency of the site.

#### Signature

- It is a **public** method.
- It returns a(n) `string` value.
- It throws one of the following exceptions:
    - [`Exception`](http://php.net/class.Exception) &mdash; if data for the site cannot be found.

### `getExcludedIps()` <a name="getExcludedIps"></a>

Returns the excluded ips of the site.

#### Signature

- It is a **public** method.
- It returns a(n) `string` value.
- It throws one of the following exceptions:
    - [`Exception`](http://php.net/class.Exception) &mdash; if data for the site cannot be found.

### `getExcludedQueryParameters()` <a name="getExcludedQueryParameters"></a>

Returns the excluded query parameters of the site.

#### Signature

- It is a **public** method.
- It returns a(n) `string` value.
- It throws one of the following exceptions:
    - [`Exception`](http://php.net/class.Exception) &mdash; if data for the site cannot be found.

### `isEcommerceEnabled()` <a name="isEcommerceEnabled"></a>

Returns whether ecommerce is enabled for the site.

#### Signature

- It is a **public** method.
- It returns a(n) `bool` value.
- It throws one of the following exceptions:
    - [`Exception`](http://php.net/class.Exception) &mdash; if data for the site cannot be found.

### `getSearchKeywordParameters()` <a name="getSearchKeywordParameters"></a>

Returns the site search keyword query parameters for the site.

#### Signature

- It is a **public** method.
- It returns a(n) `string` value.
- It throws one of the following exceptions:
    - [`Exception`](http://php.net/class.Exception) &mdash; if data for the site cannot be found.

### `getSearchCategoryParameters()` <a name="getSearchCategoryParameters"></a>

Returns the site search category query parameters for the site.

#### Signature

- It is a **public** method.
- It returns a(n) `string` value.
- It throws one of the following exceptions:
    - [`Exception`](http://php.net/class.Exception) &mdash; if data for the site cannot be found.

### `isSiteSearchEnabled()` <a name="isSiteSearchEnabled"></a>

Returns whether Site Search Tracking is enabled for the site.

#### Signature

- It is a **public** method.
- It returns a(n) `bool` value.
- It throws one of the following exceptions:
    - [`Exception`](http://php.net/class.Exception) &mdash; if data for the site cannot be found.

### `getIdSitesFromIdSitesString()` <a name="getIdSitesFromIdSitesString"></a>

Checks the given string for valid site ids and returns them as an array.

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$ids`
    - `$_restrictSitesToLogin`
- _Returns:_ An array of valid, unique integers.
    - `array`

### `clearCache()` <a name="clearCache"></a>

Clears the site data cache.

#### Description

See also [setSites](#setSites) and [setSitesFromArray](#setSitesFromArray).

#### Signature

- It is a **public static** method.
- It does not return anything.

### `getNameFor()` <a name="getNameFor"></a>

Returns the name of the site with the specified ID.

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$idsite`
- It returns a(n) `string` value.

### `getTimezoneFor()` <a name="getTimezoneFor"></a>

Returns the timezone of the site with the specified ID.

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$idsite`
- It returns a(n) `string` value.

### `getCreationDateFor()` <a name="getCreationDateFor"></a>

Returns the creation date of the site with the specified ID.

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$idsite`
- It returns a(n) `string` value.

### `getMainUrlFor()` <a name="getMainUrlFor"></a>

Returns the url for the site with the specified ID.

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$idsite`
- It returns a(n) `string` value.

### `isEcommerceEnabledFor()` <a name="isEcommerceEnabledFor"></a>

Returns whether the site with the specified ID is ecommerce enabled

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$idsite`
- It returns a(n) `string` value.

### `isSiteSearchEnabledFor()` <a name="isSiteSearchEnabledFor"></a>

Returns whether the site with the specified ID is Site Search enabled

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$idsite`
- It returns a(n) `string` value.

### `getCurrencyFor()` <a name="getCurrencyFor"></a>

Returns the currency of the site with the specified ID.

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$idsite`
- It returns a(n) `string` value.

### `getExcludedIpsFor()` <a name="getExcludedIpsFor"></a>

Returns the excluded IP addresses of the site with the specified ID.

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$idsite`
- It returns a(n) `string` value.

### `getExcludedQueryParametersFor()` <a name="getExcludedQueryParametersFor"></a>

Returns the excluded query parameters for the site with the specified ID.

#### Signature

- It is a **public static** method.
- It accepts the following parameter(s):
    - `$idsite`
- It returns a(n) `string` value.

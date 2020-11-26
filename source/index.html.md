---
title: Bang The Table v2.0.0
language_tabs:
  - ruby: Ruby
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="bang-the-table">Bang The Table v2.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Bang The Table

Base URLs:

* <a href="https://dev.ehq.test/api/v2">https://dev.ehq.test/api/v2</a>

* <a href="https://dev.ehq.test/api/v2">https://dev.ehq.test/api/v2</a>

* <a href="https://dev.ehq.test/api/v2">https://dev.ehq.test/api/v2</a>

Email: <a href="mailto:support@bangthetable.com">Bang The Table</a> Web: <a href="https://www.bangthetable.com">Bang The Table</a>

# Authentication

* API Key (ApiKeyAuth)
    - Parameter Name: **X-API-Token**, in: header.

<h1 id="bang-the-table-sites">Sites</h1>

Sites Management

## update-current-site

<a id="opIdupdate-current-site"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/site',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /site`

*Update Current Site*

Update Current Site

> Body parameter

```json
{
  "name": "Mark Jaundoo",
  "blocked": false,
  "block_username": "Mark Jaundoo",
  "block_password": 123123,
  "moderated": true,
  "email_sender_name": "Mark Jaundoo",
  "email_address": "mark@example.com",
  "licence_type": "plus",
  "timezone": "Sydney",
  "display_site_banner": false,
  "display_project_banner": false,
  "logo_url": "string",
  "banner_url": "string",
  "favicon_url": "string",
  "background_image_url": "string"
}
```

<h3 id="update-current-site-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|A JSON object with site information|
|» name|body|[Site/properties/name](#schemasite/properties/name)|false|Name of the person to send review request|
|» blocked|body|[Site/properties/blocked](#schemasite/properties/blocked)|false|Set true for block this site|
|» block_username|body|[Site/properties/block_username](#schemasite/properties/block_username)|false|none|
|» block_password|body|[Site/properties/block_password](#schemasite/properties/block_password)|false|none|
|» moderated|body|[Site/properties/moderated](#schemasite/properties/moderated)|false|none|
|» email_sender_name|body|[Site/properties/email_sender_name](#schemasite/properties/email_sender_name)|false|none|
|» email_address|body|[Site/properties/email_address](#schemasite/properties/email_address)|false|none|
|» licence_type|body|[Site/properties/licence_type](#schemasite/properties/licence_type)|false|none|
|» timezone|body|[Site/properties/timezone](#schemasite/properties/timezone)|false|none|
|» display_site_banner|body|[Site/properties/display_site_banner](#schemasite/properties/display_site_banner)|false|none|
|» display_project_banner|body|[Site/properties/display_project_banner](#schemasite/properties/display_project_banner)|false|none|
|» logo_url|body|[Site/properties/logo_url](#schemasite/properties/logo_url)|false|none|
|» banner_url|body|[Site/properties/banner_url](#schemasite/properties/banner_url)|false|none|
|» favicon_url|body|[Site/properties/favicon_url](#schemasite/properties/favicon_url)|false|none|
|» background_image_url|body|[Site/properties/background_image_url](#schemasite/properties/background_image_url)|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Site",
    "attributes": {
      "id": 1,
      "name": "Mark Jaundoo",
      "blocked": false,
      "block_username": "Mark Jaundoo",
      "block_password": 123123,
      "moderated": true,
      "client_id": 1,
      "email_sender_name": "Mark Jaundoo",
      "email_address": "mark@example.com",
      "demo": false,
      "logo_url": "string",
      "locale": "en",
      "licence_type": "plus",
      "theme_name": "bondi",
      "timezone": "Sydney",
      "banner_url": "string",
      "favicon_url": "string",
      "background_image_url": "string",
      "display_site_banner": false,
      "display_project_banner": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-current-site-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Current Site|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-current-site-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-current-site

<a id="opIdget-current-site"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/site',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /site`

*Get current site*

Get current site

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Site",
    "attributes": {
      "id": 1,
      "name": "Mark Jaundoo",
      "blocked": false,
      "block_username": "Mark Jaundoo",
      "block_password": 123123,
      "moderated": true,
      "client_id": 1,
      "email_sender_name": "Mark Jaundoo",
      "email_address": "mark@example.com",
      "demo": false,
      "logo_url": "string",
      "locale": "en",
      "licence_type": "plus",
      "theme_name": "bondi",
      "timezone": "Sydney",
      "banner_url": "string",
      "favicon_url": "string",
      "background_image_url": "string",
      "display_site_banner": false,
      "display_project_banner": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-current-site-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Site|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-current-site-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-current-site-launch

<a id="opIdupdate-current-site-launch"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/site/launch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /site/launch`

*Update Current Site Launch*

Update Current Site Launch

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Site",
    "attributes": {
      "id": 1,
      "name": "Mark Jaundoo",
      "blocked": false,
      "block_username": "Mark Jaundoo",
      "block_password": 123123,
      "moderated": true,
      "client_id": 1,
      "email_sender_name": "Mark Jaundoo",
      "email_address": "mark@example.com",
      "demo": false,
      "logo_url": "string",
      "locale": "en",
      "licence_type": "plus",
      "theme_name": "bondi",
      "timezone": "Sydney",
      "banner_url": "string",
      "favicon_url": "string",
      "background_image_url": "string",
      "display_site_banner": false,
      "display_project_banner": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-current-site-launch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Current Site|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-current-site-launch-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-site

<a id="opIdupdate-site"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/sites/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /sites/{id}`

*Update Site*

Update Site

> Body parameter

```json
{
  "name": "Mark Jaundoo",
  "blocked": false,
  "block_username": "Mark Jaundoo",
  "block_password": 123123,
  "moderated": true,
  "client_id": 1,
  "email_sender_name": "Mark Jaundoo",
  "email_address": "mark@example.com",
  "demo": false,
  "logo_url": "string",
  "locale": "en",
  "licence_type": "plus",
  "theme_name": "bondi",
  "timezone": "Sydney",
  "banner_url": "string",
  "favicon_url": "string",
  "background_image_url": "string"
}
```

<h3 id="update-site-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with site information|
|» name|body|[Site/properties/name](#schemasite/properties/name)|false|Name of the person to send review request|
|» blocked|body|[Site/properties/blocked](#schemasite/properties/blocked)|false|Set true for block this site|
|» block_username|body|[Site/properties/block_username](#schemasite/properties/block_username)|false|none|
|» block_password|body|[Site/properties/block_password](#schemasite/properties/block_password)|false|none|
|» moderated|body|[Site/properties/moderated](#schemasite/properties/moderated)|false|none|
|» client_id|body|[Site/properties/client_id](#schemasite/properties/client_id)|false|none|
|» email_sender_name|body|[Site/properties/email_sender_name](#schemasite/properties/email_sender_name)|false|none|
|» email_address|body|[Site/properties/email_address](#schemasite/properties/email_address)|false|none|
|» demo|body|[Site/properties/demo](#schemasite/properties/demo)|false|none|
|» logo_url|body|[Site/properties/logo_url](#schemasite/properties/logo_url)|false|none|
|» locale|body|[Site/properties/locale](#schemasite/properties/locale)|false|none|
|» licence_type|body|[Site/properties/licence_type](#schemasite/properties/licence_type)|false|none|
|» theme_name|body|[Site/properties/theme_name](#schemasite/properties/theme_name)|false|none|
|» timezone|body|[Site/properties/timezone](#schemasite/properties/timezone)|false|none|
|» banner_url|body|[Site/properties/banner_url](#schemasite/properties/banner_url)|false|none|
|» favicon_url|body|[Site/properties/favicon_url](#schemasite/properties/favicon_url)|false|none|
|» background_image_url|body|[Site/properties/background_image_url](#schemasite/properties/background_image_url)|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Site",
    "attributes": {
      "id": 1,
      "name": "Mark Jaundoo",
      "blocked": false,
      "block_username": "Mark Jaundoo",
      "block_password": 123123,
      "moderated": true,
      "client_id": 1,
      "email_sender_name": "Mark Jaundoo",
      "email_address": "mark@example.com",
      "demo": false,
      "logo_url": "string",
      "locale": "en",
      "licence_type": "plus",
      "theme_name": "bondi",
      "timezone": "Sydney",
      "banner_url": "string",
      "favicon_url": "string",
      "background_image_url": "string",
      "display_site_banner": false,
      "display_project_banner": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-site-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Site|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-site-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-users">Users</h1>

Users Management

## get-users

<a id="opIdget-users"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/users',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /users`

*Get list of Users*

Get list of Users

<h3 id="get-users-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer|false|none|
|per_page|query|integer|false|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "User",
      "attributes": {
        "id": 1,
        "login": "user5040",
        "email": "user6145@example.com",
        "created_at": "2020-11-13T10:00:00.000Z",
        "last_seen_at": "2020-11-13T10:00:00.000Z",
        "role_name": "participant",
        "blocked": false,
        "unconfirmed": false,
        "role_before_blocking": "role_name",
        "accessible_projects_count": false,
        "accessible_hubs_count": false,
        "accessible_projects_ids": [
          1,
          2
        ],
        "image_url": "string",
        "confirmed": false,
        "subscribed": true,
        "type": "string",
        "unconfirmed_email": "string",
        "login_count": 2
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-users-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Users|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|

<h3 id="get-users-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-user

<a id="opIdupdate-user"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/users/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /users/{id}`

*Update User*

Update User

> Body parameter

```json
{
  "image_url": "string"
}
```

<h3 id="update-user-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with user information|
|» image_url|body|[User/properties/image_url](#schemauser/properties/image_url)|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "User",
    "attributes": {
      "id": 1,
      "login": "user5040",
      "email": "user6145@example.com",
      "created_at": "2020-11-13T10:00:00.000Z",
      "last_seen_at": "2020-11-13T10:00:00.000Z",
      "role_name": "participant",
      "blocked": false,
      "unconfirmed": false,
      "role_before_blocking": "role_name",
      "accessible_projects_count": false,
      "accessible_hubs_count": false,
      "accessible_projects_ids": [
        1,
        2
      ],
      "image_url": "string",
      "confirmed": false,
      "subscribed": true,
      "type": "string",
      "unconfirmed_email": "string",
      "login_count": 2
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-user-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated User|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-user-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## user-change-password

<a id="opIduser-change-password"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/users/change_password',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /users/change_password`

*Change user Password*

Change user Password

> Body parameter

```json
{
  "old_password": "xyz1234",
  "new_password": "abc1234",
  "new_password_confirmation": "abc1234"
}
```

<h3 id="user-change-password-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|A JSON object with user password information|
|» old_password|body|string|false|Old password user|
|» new_password|body|string|false|New password user|
|» new_password_confirmation|body|string|false|New password confirmation user|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "User",
    "attributes": {
      "id": 1,
      "login": "user5040",
      "email": "user6145@example.com",
      "created_at": "2020-11-13T10:00:00.000Z",
      "last_seen_at": "2020-11-13T10:00:00.000Z",
      "role_name": "participant",
      "blocked": false,
      "unconfirmed": false,
      "role_before_blocking": "role_name",
      "accessible_projects_count": false,
      "accessible_hubs_count": false,
      "accessible_projects_ids": [
        1,
        2
      ],
      "image_url": "string",
      "confirmed": false,
      "subscribed": true,
      "type": "string",
      "unconfirmed_email": "string",
      "login_count": 2
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="user-change-password-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated User|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="user-change-password-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## user-reset-password

<a id="opIduser-reset-password"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/users/reset_password',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /users/reset_password`

*Reset user Password*

Reset user Password

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "User",
    "attributes": {
      "id": 1,
      "login": "user5040",
      "email": "user6145@example.com",
      "created_at": "2020-11-13T10:00:00.000Z",
      "last_seen_at": "2020-11-13T10:00:00.000Z",
      "role_name": "participant",
      "blocked": false,
      "unconfirmed": false,
      "role_before_blocking": "role_name",
      "accessible_projects_count": false,
      "accessible_hubs_count": false,
      "accessible_projects_ids": [
        1,
        2
      ],
      "image_url": "string",
      "confirmed": false,
      "subscribed": true,
      "type": "string",
      "unconfirmed_email": "string",
      "login_count": 2
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="user-reset-password-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated User|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="user-reset-password-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-current-user

<a id="opIdget-current-user"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/users/current',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /users/current`

*Get current user*

Get current user

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "User",
    "attributes": {
      "id": 1,
      "login": "user5040",
      "email": "user6145@example.com",
      "created_at": "2020-11-13T10:00:00.000Z",
      "last_seen_at": "2020-11-13T10:00:00.000Z",
      "role_name": "participant",
      "blocked": false,
      "unconfirmed": false,
      "role_before_blocking": "role_name",
      "accessible_projects_count": false,
      "accessible_hubs_count": false,
      "accessible_projects_ids": [
        1,
        2
      ],
      "image_url": "string",
      "confirmed": false,
      "subscribed": true,
      "type": "string",
      "unconfirmed_email": "string",
      "login_count": 2
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-current-user-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-current-user-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## user-logout

<a id="opIduser-logout"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/users/logout',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /users/logout`

*User Logout*

User Logout

> Example responses

> 400 Response

```
"string"
```

<h3 id="user-logout-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|User logout successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## user-verify

<a id="opIduser-verify"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'text/plain',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/users/verify',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /users/verify`

*User Verify*

User Verify

> Body parameter

```json
{
  "email_or_login": "abc@example.com",
  "password": "abc1234"
}
```

<h3 id="user-verify-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|A JSON object with user verify information|
|» email_or_login|body|string|false|Email or Login of the user|
|» password|body|string|false|Password of the user|

> Example responses

> 200 Response

```
"LOGIN_SUCCESS"
```

<h3 id="user-verify-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User Verify|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## user-confirm

<a id="opIduser-confirm"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/users/{user_id}/confirm',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /users/{user_id}/confirm`

*User Confirm*

User Confirm

> Body parameter

```json
{
  "otp": 123456
}
```

<h3 id="user-confirm-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|user_id|path|integer|true|User ID|
|body|body|object|true|A JSON object with user confirm information|
|» otp|body|string|false|OTP for user confirm account|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="user-confirm-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Activate user with a valid otp|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="user-confirm-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## user-resend_email

<a id="opIduser-resend_email"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/users/{user_id}/resend_email',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /users/{user_id}/resend_email`

*User Resend Email*

User Resend Email

<h3 id="user-resend_email-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|user_id|path|integer|true|User ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="user-resend_email-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Send User Confirmation Instruction Successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="user-resend_email-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## user-resend_confirmation_email

<a id="opIduser-resend_confirmation_email"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/users/resend_confirmation_email',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /users/resend_confirmation_email`

*User Resend Confirmation Email*

User Resend Confirmation Email

> Body parameter

```json
{
  "email": "abc@example.com"
}
```

<h3 id="user-resend_confirmation_email-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|A JSON object with user confirmation or reset password information|
|» email|body|string|false|Email of the user|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="user-resend_confirmation_email-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Send User ReConfirmation Instruction Successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="user-resend_confirmation_email-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## user-forgot_password_email

<a id="opIduser-forgot_password_email"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/users/forgot_password_email',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /users/forgot_password_email`

*Send User Rest Password Instruction Successfully*

User Forgot Password Email

> Body parameter

```json
{
  "email": "abc@example.com"
}
```

<h3 id="user-forgot_password_email-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|A JSON object with user confirmation or reset password information|
|» email|body|string|false|Email of the user|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "User",
    "attributes": {
      "id": 1,
      "login": "user5040",
      "email": "user6145@example.com",
      "created_at": "2020-11-13T10:00:00.000Z",
      "last_seen_at": "2020-11-13T10:00:00.000Z",
      "role_name": "participant",
      "blocked": false,
      "unconfirmed": false,
      "role_before_blocking": "role_name",
      "accessible_projects_count": false,
      "accessible_hubs_count": false,
      "accessible_projects_ids": [
        1,
        2
      ],
      "image_url": "string",
      "confirmed": false,
      "subscribed": true,
      "type": "string",
      "unconfirmed_email": "string",
      "login_count": 2
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="user-forgot_password_email-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="user-forgot_password_email-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-clients">Clients</h1>

Clients Management

## get-clients

<a id="opIdget-clients"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/clients',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /clients`

*Get list of Clients*

Get list of Clients

<h3 id="get-clients-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|q|query|string|false|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Client",
      "attributes": {
        "id": 2,
        "name": "Test client"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-clients-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Clients|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|

<h3 id="get-clients-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-client

<a id="opIdcreate-client"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/clients',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /clients`

*Create Client*

Create Client

> Body parameter

```json
{
  "name": "Test client"
}
```

<h3 id="create-client-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|A JSON object with client information|
|» name|body|[Client/properties/name](#schemaclient/properties/name)|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Client",
    "attributes": {
      "id": 2,
      "name": "Test client"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-client-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Client|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-client-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-client

<a id="opIdget-client"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/clients/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /clients/{id}`

*Get Client*

Get Client

<h3 id="get-client-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Client",
    "attributes": {
      "id": 2,
      "name": "Test client"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-client-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Client|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-client-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-dashboards">Dashboards</h1>

Dashboards Management

## get-dashboards

<a id="opIdget-dashboards"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/dashboards',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /dashboards`

*Get list of Dashboards*

Get list of Dashboards

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Dashboard",
      "attributes": {
        "id": 1,
        "title": "Nice Dashboard",
        "embed_link": "<iframe>ABCDE</iframe>",
        "description": "Very Nice Dashboard, Please Use",
        "sequence": 1
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-dashboards-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Dashboards|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|

<h3 id="get-dashboards-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-dashboard

<a id="opIdcreate-dashboard"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/dashboards',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /dashboards`

*Create Dashboard*

Create Dashboard

> Body parameter

```json
{
  "title": "Nice Dashboard",
  "embed_link": "<iframe>ABCDE</iframe>",
  "description": "Very Nice Dashboard, Please Use",
  "sequence": 1
}
```

<h3 id="create-dashboard-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|A JSON object with dashboard information|
|» title|body|[Dashboard/properties/title](#schemadashboard/properties/title)|false|none|
|» embed_link|body|[Dashboard/properties/embed_link](#schemadashboard/properties/embed_link)|false|none|
|» description|body|[Dashboard/properties/description](#schemadashboard/properties/description)|false|none|
|» sequence|body|[Dashboard/properties/sequence](#schemadashboard/properties/sequence)|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Dashboard",
    "attributes": {
      "id": 1,
      "title": "Nice Dashboard",
      "embed_link": "<iframe>ABCDE</iframe>",
      "description": "Very Nice Dashboard, Please Use",
      "sequence": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-dashboard-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Dashboard|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-dashboard-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-dashboard

<a id="opIdget-dashboard"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/dashboards/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /dashboards/{id}`

*Get Dashboard*

Get Dashboard

<h3 id="get-dashboard-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Dashboard",
    "attributes": {
      "id": 1,
      "title": "Nice Dashboard",
      "embed_link": "<iframe>ABCDE</iframe>",
      "description": "Very Nice Dashboard, Please Use",
      "sequence": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-dashboard-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Dashboard|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-dashboard-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-dashboard

<a id="opIdupdate-dashboard"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/dashboards/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /dashboards/{id}`

*Update Dashboard*

Update Dashboard

> Body parameter

```json
{
  "title": "Nice Dashboard",
  "embed_link": "<iframe>ABCDE</iframe>",
  "description": "Very Nice Dashboard, Please Use",
  "sequence": 1
}
```

<h3 id="update-dashboard-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with dashboard information|
|» title|body|[Dashboard/properties/title](#schemadashboard/properties/title)|false|none|
|» embed_link|body|[Dashboard/properties/embed_link](#schemadashboard/properties/embed_link)|false|none|
|» description|body|[Dashboard/properties/description](#schemadashboard/properties/description)|false|none|
|» sequence|body|[Dashboard/properties/sequence](#schemadashboard/properties/sequence)|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Dashboard",
    "attributes": {
      "id": 1,
      "title": "Nice Dashboard",
      "embed_link": "<iframe>ABCDE</iframe>",
      "description": "Very Nice Dashboard, Please Use",
      "sequence": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-dashboard-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Dashboard|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-dashboard-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-dashboard

<a id="opIddelete-dashboard"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/dashboards/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /dashboards/{id}`

*Delete Dashboard*

Delete Dashboard

<h3 id="delete-dashboard-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-dashboard-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-dashboard-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-guest-books">Guest Books</h1>

Guest Books Management

## create-project-guest_book

<a id="opIdcreate-project-guest_book"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/projects/{project_id}/guest_book',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /projects/{project_id}/guest_book`

*Create Project Guest Book*

Create Project Guest Book

> Body parameter

```json
{
  "name": "Guest book",
  "permalink": "guest-book",
  "intro_msg": "string",
  "thank_you_message": "string",
  "moderated": false,
  "premoderated": true,
  "allow_unverified_participation": false,
  "state": "draft",
  "description_display_mode": "truncated",
  "image_url": "string",
  "send_acknowledgement_to_admins": false,
  "send_acknowledgement": false,
  "archival_reason_message": "archival message",
  "notifications_emails": "devteam@bangthetable.com",
  "comment_text_limit": 250,
  "limit_comment": false
}
```

<h3 id="create-project-guest_book-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|body|body|object|true|A JSON object with project guest book information|
|» name|body|[GuestBook/properties/name](#schemaguestbook/properties/name)|false|none|
|» permalink|body|[GuestBook/properties/permalink](#schemaguestbook/properties/permalink)|false|none|
|» intro_msg|body|[GuestBook/properties/intro_msg](#schemaguestbook/properties/intro_msg)|false|none|
|» thank_you_message|body|[GuestBook/properties/thank_you_message](#schemaguestbook/properties/thank_you_message)|false|none|
|» moderated|body|[GuestBook/properties/moderated](#schemaguestbook/properties/moderated)|false|none|
|» premoderated|body|[GuestBook/properties/premoderated](#schemaguestbook/properties/premoderated)|false|none|
|» allow_unverified_participation|body|[GuestBook/properties/allow_unverified_participation](#schemaguestbook/properties/allow_unverified_participation)|false|none|
|» state|body|[GuestBook/properties/state](#schemaguestbook/properties/state)|false|none|
|» description_display_mode|body|[GuestBook/properties/description_display_mode](#schemaguestbook/properties/description_display_mode)|false|none|
|» image_url|body|[GuestBook/properties/image_url](#schemaguestbook/properties/image_url)|false|none|
|» send_acknowledgement_to_admins|body|[GuestBook/properties/send_acknowledgement_to_admins](#schemaguestbook/properties/send_acknowledgement_to_admins)|false|none|
|» send_acknowledgement|body|[GuestBook/properties/send_acknowledgement](#schemaguestbook/properties/send_acknowledgement)|false|none|
|» archival_reason_message|body|[GuestBook/properties/archival_reason_message](#schemaguestbook/properties/archival_reason_message)|false|none|
|» notifications_emails|body|[GuestBook/properties/notifications_emails](#schemaguestbook/properties/notifications_emails)|false|none|
|» comment_text_limit|body|[GuestBook/properties/comment_text_limit](#schemaguestbook/properties/comment_text_limit)|false|none|
|» limit_comment|body|[GuestBook/properties/limit_comment](#schemaguestbook/properties/limit_comment)|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Gues tBook",
    "attributes": {
      "id": 1,
      "name": "Guest book",
      "permalink": "guest-book",
      "intro_msg": "string",
      "thank_you_message": "string",
      "moderated": false,
      "premoderated": true,
      "allow_unverified_participation": false,
      "state": "draft",
      "description_display_mode": "truncated",
      "image_url": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "archival_reason_message": "archival message",
      "notifications_emails": "devteam@bangthetable.com",
      "comment_text_limit": 250,
      "limit_comment": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-project-guest_book-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Created Project GuestBook|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-project-guest_book-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-guest_book

<a id="opIdget-project-guest_book"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/guest_book',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/guest_book`

*Get Project Guest Book*

Get Project Guest Book

<h3 id="get-project-guest_book-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Gues tBook",
    "attributes": {
      "id": 1,
      "name": "Guest book",
      "permalink": "guest-book",
      "intro_msg": "string",
      "thank_you_message": "string",
      "moderated": false,
      "premoderated": true,
      "allow_unverified_participation": false,
      "state": "draft",
      "description_display_mode": "truncated",
      "image_url": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "archival_reason_message": "archival message",
      "notifications_emails": "devteam@bangthetable.com",
      "comment_text_limit": 250,
      "limit_comment": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-guest_book-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Guest Book|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-guest_book-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-project-guest_book

<a id="opIdupdate-project-guest_book"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/projects/{project_id}/guest_book',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /projects/{project_id}/guest_book`

*Update Project Guest Book*

Update Project Guest Book

> Body parameter

```json
{
  "name": "Guest book",
  "permalink": "guest-book",
  "intro_msg": "string",
  "thank_you_message": "string",
  "moderated": false,
  "premoderated": true,
  "allow_unverified_participation": false,
  "description_display_mode": "truncated",
  "image_url": "string",
  "send_acknowledgement_to_admins": false,
  "send_acknowledgement": false,
  "archival_reason_message": "archival message",
  "notifications_emails": "devteam@bangthetable.com",
  "comment_text_limit": 250,
  "limit_comment": false
}
```

<h3 id="update-project-guest_book-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|body|body|object|true|A JSON object with project guest book information|
|» name|body|[GuestBook/properties/name](#schemaguestbook/properties/name)|false|none|
|» permalink|body|[GuestBook/properties/permalink](#schemaguestbook/properties/permalink)|false|none|
|» intro_msg|body|[GuestBook/properties/intro_msg](#schemaguestbook/properties/intro_msg)|false|none|
|» thank_you_message|body|[GuestBook/properties/thank_you_message](#schemaguestbook/properties/thank_you_message)|false|none|
|» moderated|body|[GuestBook/properties/moderated](#schemaguestbook/properties/moderated)|false|none|
|» premoderated|body|[GuestBook/properties/premoderated](#schemaguestbook/properties/premoderated)|false|none|
|» allow_unverified_participation|body|[GuestBook/properties/allow_unverified_participation](#schemaguestbook/properties/allow_unverified_participation)|false|none|
|» description_display_mode|body|[GuestBook/properties/description_display_mode](#schemaguestbook/properties/description_display_mode)|false|none|
|» image_url|body|[GuestBook/properties/image_url](#schemaguestbook/properties/image_url)|false|none|
|» send_acknowledgement_to_admins|body|[GuestBook/properties/send_acknowledgement_to_admins](#schemaguestbook/properties/send_acknowledgement_to_admins)|false|none|
|» send_acknowledgement|body|[GuestBook/properties/send_acknowledgement](#schemaguestbook/properties/send_acknowledgement)|false|none|
|» archival_reason_message|body|[GuestBook/properties/archival_reason_message](#schemaguestbook/properties/archival_reason_message)|false|none|
|» notifications_emails|body|[GuestBook/properties/notifications_emails](#schemaguestbook/properties/notifications_emails)|false|none|
|» comment_text_limit|body|[GuestBook/properties/comment_text_limit](#schemaguestbook/properties/comment_text_limit)|false|none|
|» limit_comment|body|[GuestBook/properties/limit_comment](#schemaguestbook/properties/limit_comment)|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Gues tBook",
    "attributes": {
      "id": 1,
      "name": "Guest book",
      "permalink": "guest-book",
      "intro_msg": "string",
      "thank_you_message": "string",
      "moderated": false,
      "premoderated": true,
      "allow_unverified_participation": false,
      "state": "draft",
      "description_display_mode": "truncated",
      "image_url": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "archival_reason_message": "archival message",
      "notifications_emails": "devteam@bangthetable.com",
      "comment_text_limit": 250,
      "limit_comment": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-project-guest_book-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Project Guest Book|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-project-guest_book-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-project-guest_book

<a id="opIddelete-project-guest_book"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/projects/{project_id}/guest_book',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /projects/{project_id}/guest_book`

*Delete Project Guest Book*

Delete Project Guest Book

<h3 id="delete-project-guest_book-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-project-guest_book-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-project-guest_book-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## publish-project-guest_book

<a id="opIdpublish-project-guest_book"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/guest_book/publish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/guest_book/publish`

*Publish Project Guest Book*

Publish Project Guest Book

<h3 id="publish-project-guest_book-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Gues tBook",
    "attributes": {
      "id": 1,
      "name": "Guest book",
      "permalink": "guest-book",
      "intro_msg": "string",
      "thank_you_message": "string",
      "moderated": false,
      "premoderated": true,
      "allow_unverified_participation": false,
      "state": "draft",
      "description_display_mode": "truncated",
      "image_url": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "archival_reason_message": "archival message",
      "notifications_emails": "devteam@bangthetable.com",
      "comment_text_limit": 250,
      "limit_comment": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="publish-project-guest_book-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Publish Project Guest Book|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="publish-project-guest_book-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unpublish-project-guest_book

<a id="opIdunpublish-project-guest_book"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/guest_book/unpublish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/guest_book/unpublish`

*Unpublish Project Guest Book*

Unpublish Project Guest Book

<h3 id="unpublish-project-guest_book-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Gues tBook",
    "attributes": {
      "id": 1,
      "name": "Guest book",
      "permalink": "guest-book",
      "intro_msg": "string",
      "thank_you_message": "string",
      "moderated": false,
      "premoderated": true,
      "allow_unverified_participation": false,
      "state": "draft",
      "description_display_mode": "truncated",
      "image_url": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "archival_reason_message": "archival message",
      "notifications_emails": "devteam@bangthetable.com",
      "comment_text_limit": 250,
      "limit_comment": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unpublish-project-guest_book-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unpublish Project Guest Book|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unpublish-project-guest_book-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## archive-project-guest_book

<a id="opIdarchive-project-guest_book"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/guest_book/archive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/guest_book/archive`

*Archive Project Guest Book*

Archive Project Guest Book

> Body parameter

```json
{
  "hide": true
}
```

<h3 id="archive-project-guest_book-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|body|body|object|true|A JSON object with archive information|
|» hide|body|boolean|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Gues tBook",
    "attributes": {
      "id": 1,
      "name": "Guest book",
      "permalink": "guest-book",
      "intro_msg": "string",
      "thank_you_message": "string",
      "moderated": false,
      "premoderated": true,
      "allow_unverified_participation": false,
      "state": "draft",
      "description_display_mode": "truncated",
      "image_url": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "archival_reason_message": "archival message",
      "notifications_emails": "devteam@bangthetable.com",
      "comment_text_limit": 250,
      "limit_comment": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="archive-project-guest_book-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Archive Project Guest Book|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="archive-project-guest_book-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unarchive-project-guest_book

<a id="opIdunarchive-project-guest_book"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/guest_book/unarchive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/guest_book/unarchive`

*Unarchive Project Guest Book*

Unarchive Project Guest Book

<h3 id="unarchive-project-guest_book-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Gues tBook",
    "attributes": {
      "id": 1,
      "name": "Guest book",
      "permalink": "guest-book",
      "intro_msg": "string",
      "thank_you_message": "string",
      "moderated": false,
      "premoderated": true,
      "allow_unverified_participation": false,
      "state": "draft",
      "description_display_mode": "truncated",
      "image_url": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "archival_reason_message": "archival message",
      "notifications_emails": "devteam@bangthetable.com",
      "comment_text_limit": 250,
      "limit_comment": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unarchive-project-guest_book-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unarchive Project Guest Book|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unarchive-project-guest_book-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## hide-project-guest_book

<a id="opIdhide-project-guest_book"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/guest_book/hide',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/guest_book/hide`

*Hide Project Guest Book*

Hide Project Guest Book

<h3 id="hide-project-guest_book-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Gues tBook",
    "attributes": {
      "id": 1,
      "name": "Guest book",
      "permalink": "guest-book",
      "intro_msg": "string",
      "thank_you_message": "string",
      "moderated": false,
      "premoderated": true,
      "allow_unverified_participation": false,
      "state": "draft",
      "description_display_mode": "truncated",
      "image_url": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "archival_reason_message": "archival message",
      "notifications_emails": "devteam@bangthetable.com",
      "comment_text_limit": 250,
      "limit_comment": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="hide-project-guest_book-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hide Project Guest Book|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="hide-project-guest_book-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## visible-project-guest_book

<a id="opIdvisible-project-guest_book"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/guest_book/visible',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/guest_book/visible`

*Visible Project Guest Book*

Visible Project Guest Book

<h3 id="visible-project-guest_book-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Gues tBook",
    "attributes": {
      "id": 1,
      "name": "Guest book",
      "permalink": "guest-book",
      "intro_msg": "string",
      "thank_you_message": "string",
      "moderated": false,
      "premoderated": true,
      "allow_unverified_participation": false,
      "state": "draft",
      "description_display_mode": "truncated",
      "image_url": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "archival_reason_message": "archival message",
      "notifications_emails": "devteam@bangthetable.com",
      "comment_text_limit": 250,
      "limit_comment": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="visible-project-guest_book-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Visible Project Guest Book|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="visible-project-guest_book-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-guest_book-generate_permalink

<a id="opIdget-guest_book-generate_permalink"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/guest_book/generate_permalink',
  params: {
  'name' => 'string'
}, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/guest_book/generate_permalink`

*Get Guest Book Generate Permalink*

Get Guest Book Generate Permalink

<h3 id="get-guest_book-generate_permalink-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|name|query|string|true|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "type": "Permalink",
    "attributes": {
      "permalink": "sample"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-guest_book-generate_permalink-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Guest Book Generate Permalink|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="get-guest_book-generate_permalink-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» data|object|false|none|none|
|»» type|string|false|none|none|
|»» attributes|object|false|none|none|
|»»» permalink|string|false|none|none|

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-hubs">Hubs</h1>

Hubs Management

## get-hubs

<a id="opIdget-hubs"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/hubs',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /hubs`

*Get list of Hubs*

Get list of Hubs

<h3 id="get-hubs-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer|false|none|
|per_page|query|integer|false|none|
|filters|query|object|false|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Hub",
      "attributes": {
        "id": 1,
        "description": "new_description",
        "name": "longtext",
        "meta_description": "new_meta_description",
        "meta_keywords": "new_meta_keywords",
        "permalink": "string",
        "description_display_mode": "truncated",
        "image_url": "http://test.com/image.png",
        "image_caption": "string",
        "image_description": "string",
        "is_new_hub": false,
        "visibility_mode": "Protected",
        "text_wrap_mode": "string",
        "user_ids": [
          0
        ],
        "platform_analytics_tag_list": [
          "string"
        ]
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-hubs-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Hubs|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="get-hubs-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-hub

<a id="opIdcreate-hub"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/hubs',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /hubs`

*Create Hub*

Create Hub

> Body parameter

```json
{
  "name": "longtext",
  "description": "new_description",
  "meta_description": "new_meta_description",
  "meta_keywords": "new_meta_keywords",
  "permalink": "string",
  "description_display_mode": "truncated",
  "image_url": "http://test.com/image.png",
  "image_caption": "string",
  "image_description": "string",
  "is_new_hub": false,
  "visibility_mode": "Protected",
  "text_wrap_mode": "string",
  "user_ids": [
    0
  ],
  "platform_analytics_tag_list": [
    "string"
  ]
}
```

<h3 id="create-hub-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|A JSON object with hub information|
|» name|body|[Hub/properties/name](#schemahub/properties/name)|false|none|
|» description|body|[Hub/properties/description](#schemahub/properties/description)|false|none|
|» meta_description|body|[Hub/properties/meta_description](#schemahub/properties/meta_description)|false|none|
|» meta_keywords|body|[Hub/properties/meta_keywords](#schemahub/properties/meta_keywords)|false|none|
|» permalink|body|[Hub/properties/permalink](#schemahub/properties/permalink)|false|none|
|» description_display_mode|body|[Hub/properties/description_display_mode](#schemahub/properties/description_display_mode)|false|none|
|» image_url|body|[Hub/properties/image_url](#schemahub/properties/image_url)|false|none|
|» image_caption|body|[Hub/properties/image_caption](#schemahub/properties/image_caption)|false|none|
|» image_description|body|[Hub/properties/image_description](#schemahub/properties/image_description)|false|none|
|» is_new_hub|body|[Hub/properties/is_new_hub](#schemahub/properties/is_new_hub)|false|none|
|» visibility_mode|body|[Hub/properties/visibility_mode](#schemahub/properties/visibility_mode)|false|none|
|» text_wrap_mode|body|[Hub/properties/text_wrap_mode](#schemahub/properties/text_wrap_mode)|false|none|
|» user_ids|body|[integer]|false|none|
|» platform_analytics_tag_list|body|[string]|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Hub",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "longtext",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "permalink": "string",
      "description_display_mode": "truncated",
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "is_new_hub": false,
      "visibility_mode": "Protected",
      "text_wrap_mode": "string",
      "user_ids": [
        0
      ],
      "platform_analytics_tag_list": [
        "string"
      ]
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-hub-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Hub|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-hub-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-hub

<a id="opIdget-hub"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/hubs/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /hubs/{id}`

*Get Hub*

Get Hub

<h3 id="get-hub-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Hub",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "longtext",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "permalink": "string",
      "description_display_mode": "truncated",
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "is_new_hub": false,
      "visibility_mode": "Protected",
      "text_wrap_mode": "string",
      "user_ids": [
        0
      ],
      "platform_analytics_tag_list": [
        "string"
      ]
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-hub-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hub|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-hub-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-hub

<a id="opIdupdate-hub"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/hubs/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /hubs/{id}`

*Update Hub*

Update Hub

> Body parameter

```json
{
  "id": 1,
  "name": "longtext",
  "description": "new_description",
  "meta_description": "new_meta_description",
  "meta_keywords": "new_meta_keywords",
  "permalink": "string",
  "description_display_mode": "truncated",
  "image_url": "http://test.com/image.png",
  "image_caption": "string",
  "image_description": "string",
  "text_wrap_mode": "string",
  "platform_analytics_tag_list": [
    "string"
  ]
}
```

<h3 id="update-hub-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with hub information|
|» id|body|[Hub/properties/id](#schemahub/properties/id)|false|Id of the hub|
|» name|body|[Hub/properties/name](#schemahub/properties/name)|false|none|
|» description|body|[Hub/properties/description](#schemahub/properties/description)|false|none|
|» meta_description|body|[Hub/properties/meta_description](#schemahub/properties/meta_description)|false|none|
|» meta_keywords|body|[Hub/properties/meta_keywords](#schemahub/properties/meta_keywords)|false|none|
|» permalink|body|[Hub/properties/permalink](#schemahub/properties/permalink)|false|none|
|» description_display_mode|body|[Hub/properties/description_display_mode](#schemahub/properties/description_display_mode)|false|none|
|» image_url|body|[Hub/properties/image_url](#schemahub/properties/image_url)|false|none|
|» image_caption|body|[Hub/properties/image_caption](#schemahub/properties/image_caption)|false|none|
|» image_description|body|[Hub/properties/image_description](#schemahub/properties/image_description)|false|none|
|» text_wrap_mode|body|[Hub/properties/text_wrap_mode](#schemahub/properties/text_wrap_mode)|false|none|
|» platform_analytics_tag_list|body|[string]|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Hub",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "longtext",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "permalink": "string",
      "description_display_mode": "truncated",
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "is_new_hub": false,
      "visibility_mode": "Protected",
      "text_wrap_mode": "string",
      "user_ids": [
        0
      ],
      "platform_analytics_tag_list": [
        "string"
      ]
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-hub-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Hub|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-hub-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-hub

<a id="opIddelete-hub"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/hubs/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /hubs/{id}`

*Delete Hub*

Delete Hub

<h3 id="delete-hub-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-hub-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-hub-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-hub-visibility

<a id="opIdupdate-hub-visibility"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/hubs/{hub_id}/visibility',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /hubs/{hub_id}/visibility`

*Update Hub Visibility*

Update Hub Visibility

> Body parameter

```json
{
  "segment_ids": [
    0
  ]
}
```

<h3 id="update-hub-visibility-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|hub_id|path|integer|true|Hub ID|
|body|body|object|true|A JSON object with hub visibility information|
|» segment_ids|body|[integer]|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Hub",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "longtext",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "permalink": "string",
      "description_display_mode": "truncated",
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "is_new_hub": false,
      "visibility_mode": "Protected",
      "text_wrap_mode": "string",
      "user_ids": [
        0
      ],
      "platform_analytics_tag_list": [
        "string"
      ]
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-hub-visibility-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Hub Visibility|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-hub-visibility-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-hub-tags

<a id="opIdget-hub-tags"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/hubs/{hub_id}/tags',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /hubs/{hub_id}/tags`

*Get list of Hub Tags*

Get list of Hub Tags

<h3 id="get-hub-tags-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|hub_id|path|integer|true|Hub ID|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Tag",
      "attributes": {
        "id": 1,
        "name": "New"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-hub-tags-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Hub Tags|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|

<h3 id="get-hub-tags-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-hub-tag

<a id="opIdcreate-hub-tag"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/hubs/{hub_id}/tags',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /hubs/{hub_id}/tags`

*Create Hub Tag*

Create Hub Tag

> Body parameter

```json
{
  "name": "New"
}
```

<h3 id="create-hub-tag-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|hub_id|path|integer|true|Hub ID|
|body|body|object|true|A JSON object with tag information|
|» name|body|[Tag/properties/name](#schematag/properties/name)|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Tag",
    "attributes": {
      "id": 1,
      "name": "New"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-hub-tag-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Hub Tag|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-hub-tag-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-hub-delete

<a id="opIddelete-hub-delete"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/hubs/{hub_id}/tags/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /hubs/{hub_id}/tags/{id}`

*Delete Hub Delete*

Delete Hub Delete

<h3 id="delete-hub-delete-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|hub_id|path|integer|true|Hub ID|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-hub-delete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-hub-delete-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-hub-generate_permalink

<a id="opIdget-hub-generate_permalink"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/hubs/generate_permalink',
  params: {
  'name' => 'string'
}, headers: headers

p JSON.parse(result)

```

`GET /hubs/generate_permalink`

*Get Hub Generate Permalink*

Get Hub Generate Permalink

<h3 id="get-hub-generate_permalink-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|name|query|string|true|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "type": "Permalink",
    "attributes": {
      "permalink": "sample"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-hub-generate_permalink-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hub Generate Permalink|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="get-hub-generate_permalink-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» data|object|false|none|none|
|»» type|string|false|none|none|
|»» attributes|object|false|none|none|
|»»» permalink|string|false|none|none|

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-hub_page_revisions

<a id="opIdget-hub_page_revisions"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/hubs/{hub_id}/hub_page_revisions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /hubs/{hub_id}/hub_page_revisions`

*Get list of Hub Page Revisions*

Get list of Hub Page Revisions

<h3 id="get-hub_page_revisions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|hub_id|path|integer|true|Hub ID|
|page|query|integer|false|none|
|per_page|query|integer|false|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "HubPageRevision",
      "attributes": {
        "id": 1,
        "hub_id": 1,
        "published": false,
        "sections": {
          "sample_meta": {
            "brand-color": "string"
          }
        },
        "created_at": "2020-11-13T10:00:00.000Z",
        "updated_at": "2020-11-13T10:00:00.000Z"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-hub_page_revisions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Hub Page Revisions|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-hub_page_revisions-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-hub_page_revision

<a id="opIdcreate-hub_page_revision"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/hubs/{hub_id}/hub_page_revisions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /hubs/{hub_id}/hub_page_revisions`

*Create Hub Page Revision*

Create Hub Page Revision

> Body parameter

```json
{
  "published": false,
  "sections": {
    "sample_meta": {
      "brand-color": "string"
    }
  }
}
```

<h3 id="create-hub_page_revision-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|hub_id|path|integer|true|Hub ID|
|body|body|object|true|A JSON object with hub page revision information|
|» published|body|[HubPageRevision/properties/published](#schemahubpagerevision/properties/published)|false|none|
|» sections|body|[HubPageRevision/properties/sections](#schemahubpagerevision/properties/sections)|false|none|
|»» sample_meta|body|object|false|none|
|»»» brand-color|body|string|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "HubPageRevision",
    "attributes": {
      "id": 1,
      "hub_id": 1,
      "published": false,
      "sections": {
        "sample_meta": {
          "brand-color": "string"
        }
      },
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-hub_page_revision-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Hub Page Revision|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-hub_page_revision-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-hub_page_revision

<a id="opIdget-hub_page_revision"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/hubs/{hub_id}/hub_page_revisions/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /hubs/{hub_id}/hub_page_revisions/{id}`

*Get Hub Page Revision*

Get Hub Page Revision

<h3 id="get-hub_page_revision-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|hub_id|path|integer|true|Hub ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "HubPageRevision",
    "attributes": {
      "id": 1,
      "hub_id": 1,
      "published": false,
      "sections": {
        "sample_meta": {
          "brand-color": "string"
        }
      },
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-hub_page_revision-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hub Page Revision|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-hub_page_revision-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-hub_page_revision

<a id="opIdupdate-hub_page_revision"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/hubs/{hub_id}/hub_page_revisions/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /hubs/{hub_id}/hub_page_revisions/{id}`

*Update Hub Page Revision*

Update Hub Page Revision

> Body parameter

```json
{
  "sections": {
    "sample_meta": {
      "brand-color": "string"
    }
  }
}
```

<h3 id="update-hub_page_revision-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|hub_id|path|integer|true|Hub ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with hub page revision information|
|» sections|body|[HubPageRevision/properties/sections](#schemahubpagerevision/properties/sections)|false|none|
|»» sample_meta|body|object|false|none|
|»»» brand-color|body|string|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "HubPageRevision",
    "attributes": {
      "id": 1,
      "hub_id": 1,
      "published": false,
      "sections": {
        "sample_meta": {
          "brand-color": "string"
        }
      },
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-hub_page_revision-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Hub Page Revision|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-hub_page_revision-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-hub-admins

<a id="opIdget-hub-admins"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/{hub_id}/admins',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /{hub_id}/admins`

*Get list of Hub Admins*

Get list of Hub Admins

<h3 id="get-hub-admins-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|hub_id|path|integer|true|Hub ID|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "User",
      "attributes": {
        "id": 1,
        "login": "user5040",
        "email": "user6145@example.com",
        "created_at": "2020-11-13T10:00:00.000Z",
        "last_seen_at": "2020-11-13T10:00:00.000Z",
        "role_name": "participant",
        "blocked": false,
        "unconfirmed": false,
        "role_before_blocking": "role_name",
        "accessible_projects_count": false,
        "accessible_hubs_count": false,
        "accessible_projects_ids": [
          1,
          2
        ],
        "image_url": "string",
        "confirmed": false,
        "subscribed": true,
        "type": "string",
        "unconfirmed_email": "string",
        "login_count": 2
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-hub-admins-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Hub Admins|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-hub-admins-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-hub-admin

<a id="opIdcreate-hub-admin"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/{hub_id}/admins',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /{hub_id}/admins`

*Create Hub Admin*

Create Hub Admin

> Body parameter

```json
{
  "user_id": 1
}
```

<h3 id="create-hub-admin-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|hub_id|path|integer|true|Hub ID|
|body|body|object|true|A JSON object with admin information|
|» user_id|body|integer|false|Id of the user|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "User",
    "attributes": {
      "id": 1,
      "login": "user5040",
      "email": "user6145@example.com",
      "created_at": "2020-11-13T10:00:00.000Z",
      "last_seen_at": "2020-11-13T10:00:00.000Z",
      "role_name": "participant",
      "blocked": false,
      "unconfirmed": false,
      "role_before_blocking": "role_name",
      "accessible_projects_count": false,
      "accessible_hubs_count": false,
      "accessible_projects_ids": [
        1,
        2
      ],
      "image_url": "string",
      "confirmed": false,
      "subscribed": true,
      "type": "string",
      "unconfirmed_email": "string",
      "login_count": 2
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-hub-admin-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Hub Admin|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-hub-admin-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## admin-hub-delete

<a id="opIdadmin-hub-delete"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/{hub_id}/admins/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /{hub_id}/admins/{id}`

*Delete Hub Admin*

Delete Hub Admin

<h3 id="admin-hub-delete-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|hub_id|path|integer|true|Hub ID|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="admin-hub-delete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="admin-hub-delete-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-home-page-revisions">Home Page Revisions</h1>

Home Page Revisions Management

## get-home_page_revisions

<a id="opIdget-home_page_revisions"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/home_page_revisions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /home_page_revisions`

*Get list of Home Page Revisions*

Get list of Home Page Revisions

<h3 id="get-home_page_revisions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer|false|none|
|per_page|query|integer|false|none|
|filters|query|object|false|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Home Page Revision",
      "attributes": {
        "id": 1,
        "site_id": 1,
        "published": false,
        "sections": {
          "sample": "string"
        },
        "created_at": "2020-11-13T10:00:00.000Z",
        "updated_at": "2020-11-13T10:00:00.000Z"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-home_page_revisions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Home Page Revisions|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|

<h3 id="get-home_page_revisions-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-home_page_revision

<a id="opIdcreate-home_page_revision"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/home_page_revisions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /home_page_revisions`

*Create Home Page Revision*

Create Home Page Revision

> Body parameter

```json
{
  "published": false,
  "sections": {
    "sample": "string"
  }
}
```

<h3 id="create-home_page_revision-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|A JSON object with home page revision information|
|» published|body|[HomePageRevision/properties/published](#schemahomepagerevision/properties/published)|false|none|
|» sections|body|[HomePageRevision/properties/sections](#schemahomepagerevision/properties/sections)|false|none|
|»» sample|body|string|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Home Page Revision",
    "attributes": {
      "id": 1,
      "site_id": 1,
      "published": false,
      "sections": {
        "sample": "string"
      },
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-home_page_revision-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Home Page Revision|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-home_page_revision-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-home_page_revision

<a id="opIdget-home_page_revision"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/home_page_revisions/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /home_page_revisions/{id}`

*Get Home Page Revision*

Get Home Page Revision

<h3 id="get-home_page_revision-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Home Page Revision",
    "attributes": {
      "id": 1,
      "site_id": 1,
      "published": false,
      "sections": {
        "sample": "string"
      },
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-home_page_revision-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Home Page Revision|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|

<h3 id="get-home_page_revision-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-home_page_revision

<a id="opIdupdate-home_page_revision"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/home_page_revisions/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /home_page_revisions/{id}`

*Update Home Page Revision*

Update Home Page Revision

> Body parameter

```json
{
  "sections": {
    "sample": "string"
  }
}
```

<h3 id="update-home_page_revision-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with home page revision information|
|» sections|body|[HomePageRevision/properties/sections](#schemahomepagerevision/properties/sections)|false|none|
|»» sample|body|string|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Home Page Revision",
    "attributes": {
      "id": 1,
      "site_id": 1,
      "published": false,
      "sections": {
        "sample": "string"
      },
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-home_page_revision-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Home Page Revision|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-home_page_revision-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-home_page_revision

<a id="opIddelete-home_page_revision"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/home_page_revisions/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /home_page_revisions/{id}`

*Delete Home Page Revision*

Delete Home Page Revision

<h3 id="delete-home_page_revision-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-home_page_revision-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-home_page_revision-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## publish-home_page_revision

<a id="opIdpublish-home_page_revision"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/home_page_revisions/{id}/publish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /home_page_revisions/{id}/publish`

*Publish Home Page Revision*

Publish Home Page Revision

<h3 id="publish-home_page_revision-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Home Page Revision",
    "attributes": {
      "id": 1,
      "site_id": 1,
      "published": false,
      "sections": {
        "sample": "string"
      },
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="publish-home_page_revision-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Publish Home Page Revision|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="publish-home_page_revision-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-participant-communities">Participant Communities</h1>

Participant Communities Management

## get-participant_communities

<a id="opIdget-participant_communities"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/participant_communities',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /participant_communities`

*Get list of Participant Communities*

Get list of Participant Communities

<h3 id="get-participant_communities-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer|false|none|
|per_page|query|integer|false|none|
|filters|query|object|false|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Project",
      "attributes": {
        "id": 1,
        "description": "new_description",
        "name": "test",
        "meta_description": "new_meta_description",
        "meta_keywords": "new_meta_keywords",
        "redirect_url": "https://google.com",
        "permalink": "test123",
        "state": "draft",
        "banner_url": "http://test.com/test.png",
        "restrict_forum_creation": true,
        "description_display_mode": "truncated",
        "visibility_mode": "Public",
        "platform_analytics_tag_list": [
          "something",
          "nothing"
        ],
        "image_url": "http://test.com/image.png",
        "image_caption": "string",
        "image_description": "string",
        "text_wrap_mode": "textwrap_default",
        "parent_id": 1,
        "subscribers_count": 10,
        "view_count": 10,
        "home_project": true,
        "published_at": "string",
        "forum_topics": 10,
        "survey_tools": 10,
        "banner_caption": "string",
        "widget_resource_count": 10,
        "quick_poll_layout": "tool",
        "created_at": "2020-11-13T10:00:00.000Z",
        "archival_reason_message": "string",
        "contribution_count": 10,
        "scheduled_at": "2020-11-13T10:00:00.000Z"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-participant_communities-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Participant Communities|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|

<h3 id="get-participant_communities-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-participant_community

<a id="opIdcreate-participant_community"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/participant_communities',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /participant_communities`

*Create Project*

Create Project

> Body parameter

```json
{
  "name": "test",
  "description": "new_description",
  "redirect_url": "https://google.com",
  "meta_description": "new_meta_description",
  "parent_id": 1,
  "permalink": "test123",
  "meta_keywords": "new_meta_keywords",
  "banner_url": "http://test.com/test.png",
  "restrict_forum_creation": true,
  "description_display_mode": "truncated",
  "image_url": "http://test.com/image.png",
  "visibility_mode": "Public",
  "platform_analytics_tag_list": [
    "something",
    "nothing"
  ]
}
```

<h3 id="create-participant_community-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|A JSON object with project information|
|» name|body|[Project/properties/name](#schemaproject/properties/name)|false|none|
|» description|body|[Project/properties/description](#schemaproject/properties/description)|false|none|
|» redirect_url|body|[Project/properties/redirect_url](#schemaproject/properties/redirect_url)|false|none|
|» meta_description|body|[Project/properties/meta_description](#schemaproject/properties/meta_description)|false|none|
|» parent_id|body|[Project/properties/parent_id](#schemaproject/properties/parent_id)|false|none|
|» permalink|body|[Project/properties/permalink](#schemaproject/properties/permalink)|false|none|
|» meta_keywords|body|[Project/properties/meta_keywords](#schemaproject/properties/meta_keywords)|false|none|
|» banner_url|body|[Project/properties/banner_url](#schemaproject/properties/banner_url)|false|none|
|» restrict_forum_creation|body|[Project/properties/restrict_forum_creation](#schemaproject/properties/restrict_forum_creation)|false|none|
|» description_display_mode|body|[Project/properties/description_display_mode](#schemaproject/properties/description_display_mode)|false|none|
|» image_url|body|[Project/properties/image_url](#schemaproject/properties/image_url)|false|none|
|» visibility_mode|body|[Project/properties/visibility_mode](#schemaproject/properties/visibility_mode)|false|none|
|» platform_analytics_tag_list|body|[string]|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-participant_community-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Participant Community|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-participant_community-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-participant_community

<a id="opIdget-participant_community"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/participant_communities/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /participant_communities/{id}`

*Get Participant Community*

Get Participant Community

<h3 id="get-participant_community-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-participant_community-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Participant Community|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-participant_community-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-participant_community

<a id="opIdupdate-participant_community"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/participant_communities/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /participant_communities/{id}`

*Update Participant Community*

Update Participant Community

> Body parameter

```json
{
  "name": "test",
  "description": "new_description",
  "redirect_url": "https://google.com",
  "meta_description": "new_meta_description",
  "permalink": "test123",
  "meta_keywords": "new_meta_keywords",
  "banner_url": "http://test.com/test.png",
  "restrict_forum_creation": true,
  "description_display_mode": "truncated",
  "visibility_mode": "Public",
  "archival_reason_message": "string",
  "forum_tool_description": "string",
  "image_url": "http://test.com/image.png",
  "image_caption": "string",
  "image_description": "string",
  "text_wrap_mode": "textwrap_default",
  "parent_id": 1,
  "forum_tool_thank_you_message": "string",
  "story_moderation_type": "string",
  "forum_tool_commentable": "string",
  "allow_unverified_pariticipation_for_story_telling_tool": "string",
  "banner_caption": "string",
  "quick_poll_layout": "tool",
  "platform_analytics_tag_list": [
    "something",
    "nothing"
  ]
}
```

<h3 id="update-participant_community-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with project information|
|» name|body|[Project/properties/name](#schemaproject/properties/name)|false|none|
|» description|body|[Project/properties/description](#schemaproject/properties/description)|false|none|
|» redirect_url|body|[Project/properties/redirect_url](#schemaproject/properties/redirect_url)|false|none|
|» meta_description|body|[Project/properties/meta_description](#schemaproject/properties/meta_description)|false|none|
|» permalink|body|[Project/properties/permalink](#schemaproject/properties/permalink)|false|none|
|» meta_keywords|body|[Project/properties/meta_keywords](#schemaproject/properties/meta_keywords)|false|none|
|» banner_url|body|[Project/properties/banner_url](#schemaproject/properties/banner_url)|false|none|
|» restrict_forum_creation|body|[Project/properties/restrict_forum_creation](#schemaproject/properties/restrict_forum_creation)|false|none|
|» description_display_mode|body|[Project/properties/description_display_mode](#schemaproject/properties/description_display_mode)|false|none|
|» visibility_mode|body|[Project/properties/visibility_mode](#schemaproject/properties/visibility_mode)|false|none|
|» archival_reason_message|body|[Project/properties/archival_reason_message](#schemaproject/properties/archival_reason_message)|false|none|
|» forum_tool_description|body|string|false|none|
|» image_url|body|[Project/properties/image_url](#schemaproject/properties/image_url)|false|none|
|» image_caption|body|[Project/properties/image_caption](#schemaproject/properties/image_caption)|false|none|
|» image_description|body|[Project/properties/image_description](#schemaproject/properties/image_description)|false|none|
|» text_wrap_mode|body|[Project/properties/text_wrap_mode](#schemaproject/properties/text_wrap_mode)|false|none|
|» parent_id|body|[Project/properties/parent_id](#schemaproject/properties/parent_id)|false|none|
|» forum_tool_thank_you_message|body|string|false|none|
|» story_moderation_type|body|string|false|none|
|» forum_tool_commentable|body|string|false|none|
|» allow_unverified_pariticipation_for_story_telling_tool|body|string|false|none|
|» banner_caption|body|[Project/properties/banner_caption](#schemaproject/properties/banner_caption)|false|none|
|» quick_poll_layout|body|[Project/properties/quick_poll_layout](#schemaproject/properties/quick_poll_layout)|false|none|
|» platform_analytics_tag_list|body|[string]|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-participant_community-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Participant Community|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-participant_community-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-participant_community

<a id="opIddelete-participant_community"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/participant_communities/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /participant_communities/{id}`

*Delete Participant Community*

Delete Participant Community

> Body parameter

```json
{
  "password": "abcd1234"
}
```

<h3 id="delete-participant_community-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|
|body|body|object|false|none|
|» password|body|string|false|none|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-participant_community-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-participant_community-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## publish-participant_community

<a id="opIdpublish-participant_community"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/participant_communities/{id}/publish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /participant_communities/{id}/publish`

*Publish Participant Community*

Publish Participant Community

<h3 id="publish-participant_community-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="publish-participant_community-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Publish Participant Community|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="publish-participant_community-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unpublish-participant_community

<a id="opIdunpublish-participant_community"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/participant_communities/{id}/unpublish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /participant_communities/{id}/unpublish`

*Unpublish Participant Community*

Unpublish Participant Community

<h3 id="unpublish-participant_community-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unpublish-participant_community-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unpublish Participant Community|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unpublish-participant_community-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## archive-participant_community

<a id="opIdarchive-participant_community"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/participant_communities/{id}/archive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /participant_communities/{id}/archive`

*Archive Participant Community*

Archive Participant Community

> Body parameter

```json
{
  "hide": true
}
```

<h3 id="archive-participant_community-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with archive information|
|» hide|body|boolean|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="archive-participant_community-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Archive Participant Community|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="archive-participant_community-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unarchive-participant_community

<a id="opIdunarchive-participant_community"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/participant_communities/{id}/unarchive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /participant_communities/{id}/unarchive`

*Unarchive Participant Community*

Unarchive Participant Community

<h3 id="unarchive-participant_community-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unarchive-participant_community-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unarchive Participant Community|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unarchive-participant_community-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## hide-participant_community

<a id="opIdhide-participant_community"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/participant_communities/{id}/hide',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /participant_communities/{id}/hide`

*Hide Participant Community*

Hide Participant Community

<h3 id="hide-participant_community-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="hide-participant_community-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hide Participant Community|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="hide-participant_community-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## visible-participant_community

<a id="opIdvisible-participant_community"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/participant_communities/{id}/visible',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /participant_communities/{id}/visible`

*Visible Participant Community*

Visible Participant Community

<h3 id="visible-participant_community-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="visible-participant_community-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Visible Participant Community|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="visible-participant_community-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## permalink_status-participant_community

<a id="opIdpermalink_status-participant_community"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/participant_communities/permalink_status',
  params: {
  'permalink' => 'string'
}, headers: headers

p JSON.parse(result)

```

`GET /participant_communities/permalink_status`

*Participant Community Permalink Status*

Participant Community Permalink Status

<h3 id="permalink_status-participant_community-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|permalink|query|string|true|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="permalink_status-participant_community-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Participant Community Permalink Status|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|The participant community is Conflict|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="permalink_status-participant_community-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-community-forums">Community Forums</h1>

Community Forums Management

## get-community-forums

<a id="opIdget-community-forums"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/participant_communities/{participant_community_id}/forums',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /participant_communities/{participant_community_id}/forums`

*Get list of Community Forums*

Get list of Community Forums

<h3 id="get-community-forums-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|participant_community_id|path|integer|true|Participant Community ID|
|page|query|integer|false|none|
|per_page|query|integer|false|none|
|filters|query|object|false|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Forum",
      "attributes": {
        "id": 1,
        "name": "sample",
        "description": "sample description",
        "permalink": "permalink_137",
        "state": "published",
        "allow_unverified_participation": false,
        "description_display_mode": "truncated",
        "image_url": "string",
        "archival_reason_message": "string",
        "comments_count": 10,
        "tag_list": [
          "string"
        ],
        "sequence": 0,
        "created_at": "2020-11-13T10:00:00.000Z",
        "updated_at": "2020-11-13T10:00:00.000Z",
        "notifications_emails": "string",
        "send_acknowledgement_to_admins": false,
        "send_acknowledgement": false,
        "author": "user3977",
        "likes_count": 10,
        "has_liked_the_forum": true,
        "forum_liked_id": 1
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-community-forums-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Community Forums|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|

<h3 id="get-community-forums-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-community-forum

<a id="opIdcreate-community-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/participant_communities/{participant_community_id}/forums',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /participant_communities/{participant_community_id}/forums`

*Create Community Forum*

Create Community Forum

> Body parameter

```json
{
  "name": "sample",
  "description": "sample description",
  "description_display_mode": "truncated",
  "allow_unverified_participation": false,
  "permalink": "permalink_137",
  "image_url": "string",
  "notifications_emails": "string",
  "archival_reason_message": "string",
  "send_acknowledgement": false,
  "send_acknowledgement_to_admins": false,
  "tag_list": [
    "string"
  ]
}
```

<h3 id="create-community-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|participant_community_id|path|integer|true|Participant Community ID|
|body|body|object|true|A JSON object with forum information|
|» name|body|[Forum/properties/name](#schemaforum/properties/name)|false|none|
|» description|body|[Forum/properties/description](#schemaforum/properties/description)|false|none|
|» description_display_mode|body|[Forum/properties/description_display_mode](#schemaforum/properties/description_display_mode)|false|none|
|» allow_unverified_participation|body|[Forum/properties/allow_unverified_participation](#schemaforum/properties/allow_unverified_participation)|false|none|
|» permalink|body|[Forum/properties/permalink](#schemaforum/properties/permalink)|false|none|
|» image_url|body|[Forum/properties/image_url](#schemaforum/properties/image_url)|false|none|
|» notifications_emails|body|[Forum/properties/notifications_emails](#schemaforum/properties/notifications_emails)|false|none|
|» archival_reason_message|body|[Forum/properties/archival_reason_message](#schemaforum/properties/archival_reason_message)|false|none|
|» send_acknowledgement|body|[Forum/properties/send_acknowledgement](#schemaforum/properties/send_acknowledgement)|false|none|
|» send_acknowledgement_to_admins|body|[Forum/properties/send_acknowledgement_to_admins](#schemaforum/properties/send_acknowledgement_to_admins)|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-community-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Community Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-community-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-community-forum

<a id="opIdget-community-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/participant_communities/{participant_community_id}/forums/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /participant_communities/{participant_community_id}/forums/{id}`

*Get Community Forum*

Get Community Forum

<h3 id="get-community-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|participant_community_id|path|integer|true|Participant Community ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-community-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Community Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-community-forum-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-community-forum

<a id="opIdupdate-community-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/participant_communities/{participant_community_id}/forums/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /participant_communities/{participant_community_id}/forums/{id}`

*Update Community Forum*

Update Community Forum

> Body parameter

```json
{
  "name": "sample",
  "description": "sample description",
  "description_display_mode": "truncated",
  "allow_unverified_participation": false,
  "permalink": "permalink_137",
  "sequence": 0,
  "image_url": "string",
  "notifications_emails": "string",
  "archival_reason_message": "string",
  "send_acknowledgement": false,
  "send_acknowledgement_to_admins": false,
  "tag_list": [
    "string"
  ]
}
```

<h3 id="update-community-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|participant_community_id|path|integer|true|Participant Community ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with forum information|
|» name|body|[Forum/properties/name](#schemaforum/properties/name)|false|none|
|» description|body|[Forum/properties/description](#schemaforum/properties/description)|false|none|
|» description_display_mode|body|[Forum/properties/description_display_mode](#schemaforum/properties/description_display_mode)|false|none|
|» allow_unverified_participation|body|[Forum/properties/allow_unverified_participation](#schemaforum/properties/allow_unverified_participation)|false|none|
|» permalink|body|[Forum/properties/permalink](#schemaforum/properties/permalink)|false|none|
|» sequence|body|[Forum/properties/sequence](#schemaforum/properties/sequence)|false|none|
|» image_url|body|[Forum/properties/image_url](#schemaforum/properties/image_url)|false|none|
|» notifications_emails|body|[Forum/properties/notifications_emails](#schemaforum/properties/notifications_emails)|false|none|
|» archival_reason_message|body|[Forum/properties/archival_reason_message](#schemaforum/properties/archival_reason_message)|false|none|
|» send_acknowledgement|body|[Forum/properties/send_acknowledgement](#schemaforum/properties/send_acknowledgement)|false|none|
|» send_acknowledgement_to_admins|body|[Forum/properties/send_acknowledgement_to_admins](#schemaforum/properties/send_acknowledgement_to_admins)|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-community-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Community Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-community-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-community-forum

<a id="opIddelete-community-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/participant_communities/{participant_community_id}/forums/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /participant_communities/{participant_community_id}/forums/{id}`

*Delete Community Forum*

Delete Community Forum

<h3 id="delete-community-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|participant_community_id|path|integer|true|Participant Community ID|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-community-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-community-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## publish-community-forum

<a id="opIdpublish-community-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/participant_communities/{participant_community_id}/forums/{id}/publish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /participant_communities/{participant_community_id}/forums/{id}/publish`

*Publish Community Forum*

Publish Community Forum

<h3 id="publish-community-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|participant_community_id|path|integer|true|Participant Community ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="publish-community-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Publish Community Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="publish-community-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unpublish-community-forum

<a id="opIdunpublish-community-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/participant_communities/{participant_community_id}/forums/{id}/unpublish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /participant_communities/{participant_community_id}/forums/{id}/unpublish`

*Unpublish Community Forum*

Unpublish Community Forum

<h3 id="unpublish-community-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|participant_community_id|path|integer|true|Participant Community ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unpublish-community-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unpublish Community Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unpublish-community-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## archive-community-forum

<a id="opIdarchive-community-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/participant_communities/{participant_community_id}/forums/{id}/archive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /participant_communities/{participant_community_id}/forums/{id}/archive`

*Archive Community Forum*

Archive Community Forum

> Body parameter

```json
{
  "hide": true
}
```

<h3 id="archive-community-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|participant_community_id|path|integer|true|Participant Community ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with archive information|
|» hide|body|boolean|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="archive-community-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Archive Community Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="archive-community-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unarchive-community-forum

<a id="opIdunarchive-community-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/participant_communities/{participant_community_id}/forums/{id}/unarchive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /participant_communities/{participant_community_id}/forums/{id}/unarchive`

*Unarchive Community Forum*

Unarchive Community Forum

<h3 id="unarchive-community-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|participant_community_id|path|integer|true|Participant Community ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unarchive-community-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unarchive Community Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unarchive-community-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## hide-community-forum

<a id="opIdhide-community-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/participant_communities/{participant_community_id}/forums/{id}/hide',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /participant_communities/{participant_community_id}/forums/{id}/hide`

*Hide Community Forum*

Hide Community Forum

<h3 id="hide-community-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|participant_community_id|path|integer|true|Participant Community ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="hide-community-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hide Community Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="hide-community-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## visible-community-forum

<a id="opIdvisible-community-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/participant_communities/{participant_community_id}/forums/{id}/visible',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /participant_communities/{participant_community_id}/forums/{id}/visible`

*Visible Community Forum*

Visible Community Forum

<h3 id="visible-community-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|participant_community_id|path|integer|true|Participant Community ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="visible-community-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Visible Community Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="visible-community-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-community-forums-email_templates

<a id="opIdget-community-forums-email_templates"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/participant_communities/{participant_community_id}/forums/email_templates',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /participant_communities/{participant_community_id}/forums/email_templates`

*Get list of Community Forums Email Templates*

Get list of Community Forums Email Templates

<h3 id="get-community-forums-email_templates-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|participant_community_id|path|integer|true|Participant Community ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Email Template",
    "attributes": {
      "id": 1,
      "subject_template": "Subject Template",
      "body_template": "Body Template",
      "emails": "abc@gmail.com,xya@gmail.com",
      "show_emails": true,
      "identifier": "notify_admin_on_new_forum_topic"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-community-forums-email_templates-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Community Forums Email Templates|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-community-forums-email_templates-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-projects">Projects</h1>

Projects Management

## get-projects

<a id="opIdget-projects"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects`

*Get list of Projects*

Get list of Projects

<h3 id="get-projects-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer|false|none|
|per_page|query|integer|false|none|
|q|query|string|false|none|
|filter|query|string|false|none|
|sort|query|string|false|none|
|order|query|string|false|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Project",
      "attributes": {
        "id": 1,
        "description": "new_description",
        "name": "test",
        "meta_description": "new_meta_description",
        "meta_keywords": "new_meta_keywords",
        "redirect_url": "https://google.com",
        "permalink": "test123",
        "state": "draft",
        "banner_url": "http://test.com/test.png",
        "restrict_forum_creation": true,
        "description_display_mode": "truncated",
        "visibility_mode": "Public",
        "platform_analytics_tag_list": [
          "something",
          "nothing"
        ],
        "image_url": "http://test.com/image.png",
        "image_caption": "string",
        "image_description": "string",
        "text_wrap_mode": "textwrap_default",
        "parent_id": 1,
        "subscribers_count": 10,
        "view_count": 10,
        "home_project": true,
        "published_at": "string",
        "forum_topics": 10,
        "survey_tools": 10,
        "banner_caption": "string",
        "widget_resource_count": 10,
        "quick_poll_layout": "tool",
        "created_at": "2020-11-13T10:00:00.000Z",
        "archival_reason_message": "string",
        "contribution_count": 10,
        "scheduled_at": "2020-11-13T10:00:00.000Z"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-projects-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Projects|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|

<h3 id="get-projects-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-project

<a id="opIdcreate-project"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/projects',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /projects`

*Create Project*

Create Project

> Body parameter

```json
{
  "name": "test",
  "description": "new_description",
  "redirect_url": "https://google.com",
  "meta_description": "new_meta_description",
  "parent_id": 1,
  "permalink": "test123",
  "meta_keywords": "new_meta_keywords",
  "banner_url": "http://test.com/test.png",
  "restrict_forum_creation": true,
  "description_display_mode": "truncated",
  "image_url": "http://test.com/image.png",
  "visibility_mode": "Public",
  "platform_analytics_tag_list": [
    "something",
    "nothing"
  ]
}
```

<h3 id="create-project-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|A JSON object with project information|
|» name|body|[Project/properties/name](#schemaproject/properties/name)|false|none|
|» description|body|[Project/properties/description](#schemaproject/properties/description)|false|none|
|» redirect_url|body|[Project/properties/redirect_url](#schemaproject/properties/redirect_url)|false|none|
|» meta_description|body|[Project/properties/meta_description](#schemaproject/properties/meta_description)|false|none|
|» parent_id|body|[Project/properties/parent_id](#schemaproject/properties/parent_id)|false|none|
|» permalink|body|[Project/properties/permalink](#schemaproject/properties/permalink)|false|none|
|» meta_keywords|body|[Project/properties/meta_keywords](#schemaproject/properties/meta_keywords)|false|none|
|» banner_url|body|[Project/properties/banner_url](#schemaproject/properties/banner_url)|false|none|
|» restrict_forum_creation|body|[Project/properties/restrict_forum_creation](#schemaproject/properties/restrict_forum_creation)|false|none|
|» description_display_mode|body|[Project/properties/description_display_mode](#schemaproject/properties/description_display_mode)|false|none|
|» image_url|body|[Project/properties/image_url](#schemaproject/properties/image_url)|false|none|
|» visibility_mode|body|[Project/properties/visibility_mode](#schemaproject/properties/visibility_mode)|false|none|
|» platform_analytics_tag_list|body|[string]|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-project-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Project|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-project-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project

<a id="opIdget-project"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{id}`

*Get Project*

Get Project

<h3 id="get-project-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|

<h3 id="get-project-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-project

<a id="opIdupdate-project"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/projects/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /projects/{id}`

*Update Project*

Update Project

> Body parameter

```json
{
  "name": "test",
  "description": "new_description",
  "redirect_url": "https://google.com",
  "meta_description": "new_meta_description",
  "permalink": "test123",
  "meta_keywords": "new_meta_keywords",
  "banner_url": "http://test.com/test.png",
  "restrict_forum_creation": true,
  "description_display_mode": "truncated",
  "visibility_mode": "Public",
  "archival_reason_message": "string",
  "forum_tool_description": "string",
  "image_url": "http://test.com/image.png",
  "image_caption": "string",
  "image_description": "string",
  "text_wrap_mode": "textwrap_default",
  "parent_id": 1,
  "forum_tool_thank_you_message": "string",
  "story_moderation_type": "string",
  "forum_tool_commentable": "string",
  "allow_unverified_pariticipation_for_story_telling_tool": "string",
  "banner_caption": "string",
  "quick_poll_layout": "tool",
  "platform_analytics_tag_list": [
    "something",
    "nothing"
  ]
}
```

<h3 id="update-project-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with project information|
|» name|body|[Project/properties/name](#schemaproject/properties/name)|false|none|
|» description|body|[Project/properties/description](#schemaproject/properties/description)|false|none|
|» redirect_url|body|[Project/properties/redirect_url](#schemaproject/properties/redirect_url)|false|none|
|» meta_description|body|[Project/properties/meta_description](#schemaproject/properties/meta_description)|false|none|
|» permalink|body|[Project/properties/permalink](#schemaproject/properties/permalink)|false|none|
|» meta_keywords|body|[Project/properties/meta_keywords](#schemaproject/properties/meta_keywords)|false|none|
|» banner_url|body|[Project/properties/banner_url](#schemaproject/properties/banner_url)|false|none|
|» restrict_forum_creation|body|[Project/properties/restrict_forum_creation](#schemaproject/properties/restrict_forum_creation)|false|none|
|» description_display_mode|body|[Project/properties/description_display_mode](#schemaproject/properties/description_display_mode)|false|none|
|» visibility_mode|body|[Project/properties/visibility_mode](#schemaproject/properties/visibility_mode)|false|none|
|» archival_reason_message|body|[Project/properties/archival_reason_message](#schemaproject/properties/archival_reason_message)|false|none|
|» forum_tool_description|body|string|false|none|
|» image_url|body|[Project/properties/image_url](#schemaproject/properties/image_url)|false|none|
|» image_caption|body|[Project/properties/image_caption](#schemaproject/properties/image_caption)|false|none|
|» image_description|body|[Project/properties/image_description](#schemaproject/properties/image_description)|false|none|
|» text_wrap_mode|body|[Project/properties/text_wrap_mode](#schemaproject/properties/text_wrap_mode)|false|none|
|» parent_id|body|[Project/properties/parent_id](#schemaproject/properties/parent_id)|false|none|
|» forum_tool_thank_you_message|body|string|false|none|
|» story_moderation_type|body|string|false|none|
|» forum_tool_commentable|body|string|false|none|
|» allow_unverified_pariticipation_for_story_telling_tool|body|string|false|none|
|» banner_caption|body|[Project/properties/banner_caption](#schemaproject/properties/banner_caption)|false|none|
|» quick_poll_layout|body|[Project/properties/quick_poll_layout](#schemaproject/properties/quick_poll_layout)|false|none|
|» platform_analytics_tag_list|body|[string]|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-project-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Project|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-project-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-project

<a id="opIddelete-project"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/projects/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /projects/{id}`

*Delete Project*

Delete Project

<h3 id="delete-project-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-project-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-project-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## publish-project

<a id="opIdpublish-project"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{id}/publish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{id}/publish`

*Publish Project*

Publish Project

<h3 id="publish-project-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="publish-project-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Publish Project|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="publish-project-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unpublish-project

<a id="opIdunpublish-project"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{id}/unpublish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{id}/unpublish`

*Unpublish Project*

Unpublish Project

<h3 id="unpublish-project-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unpublish-project-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unpublish Project|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unpublish-project-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## archive-project

<a id="opIdarchive-project"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{id}/archive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{id}/archive`

*Archive Project*

Archive Project

> Body parameter

```json
{
  "hide": true
}
```

<h3 id="archive-project-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with archive information|
|» hide|body|boolean|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="archive-project-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Archive Project|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="archive-project-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unarchive-project

<a id="opIdunarchive-project"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{id}/unarchive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{id}/unarchive`

*Unarchive Project*

Unarchive Project

<h3 id="unarchive-project-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unarchive-project-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unarchive Project|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unarchive-project-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## hide-project

<a id="opIdhide-project"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{id}/hide',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{id}/hide`

*Hide Project*

Hide Project

<h3 id="hide-project-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="hide-project-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hide Project|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="hide-project-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## visible-project

<a id="opIdvisible-project"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{id}/visible',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{id}/visible`

*Visible Project*

Visible Project

<h3 id="visible-project-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="visible-project-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Visible Project|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="visible-project-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## permalink_status-project

<a id="opIdpermalink_status-project"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/permalink_status',
  params: {
  'permalink' => 'string'
}, headers: headers

p JSON.parse(result)

```

`GET /projects/permalink_status`

*Project Permalink Status*

Project Permalink Status

<h3 id="permalink_status-project-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|permalink|query|string|true|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Project",
    "attributes": {
      "id": 1,
      "description": "new_description",
      "name": "test",
      "meta_description": "new_meta_description",
      "meta_keywords": "new_meta_keywords",
      "redirect_url": "https://google.com",
      "permalink": "test123",
      "state": "draft",
      "banner_url": "http://test.com/test.png",
      "restrict_forum_creation": true,
      "description_display_mode": "truncated",
      "visibility_mode": "Public",
      "platform_analytics_tag_list": [
        "something",
        "nothing"
      ],
      "image_url": "http://test.com/image.png",
      "image_caption": "string",
      "image_description": "string",
      "text_wrap_mode": "textwrap_default",
      "parent_id": 1,
      "subscribers_count": 10,
      "view_count": 10,
      "home_project": true,
      "published_at": "string",
      "forum_topics": 10,
      "survey_tools": 10,
      "banner_caption": "string",
      "widget_resource_count": 10,
      "quick_poll_layout": "tool",
      "created_at": "2020-11-13T10:00:00.000Z",
      "archival_reason_message": "string",
      "contribution_count": 10,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="permalink_status-project-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Permalink Status|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|The project is Conflict|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="permalink_status-project-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-blog-posts">Blog Posts</h1>

Blog Posts Management

## get-project-blog_posts

<a id="opIdget-project-blog_posts"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/blog_posts`

*Get list of Project Blog Posts*

Get list of Project Blog Posts

<h3 id="get-project-blog_posts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|page|query|integer|false|none|
|per_page|query|integer|false|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "BlogPost",
      "attributes": {
        "id": 1,
        "name": "new topic",
        "description": "discuss",
        "permalink": "ft",
        "state": "published",
        "allow_unverified_participation": true,
        "description_display_mode": "string",
        "image_url": "example.com/image.png",
        "tag_list": [
          "a",
          "b",
          "c"
        ],
        "commentable": false,
        "archival_reason_message": "archival message",
        "sequence": 0,
        "comments_count": 0,
        "show_date": true,
        "custom_date": "2020-11-13T10:00:00.000Z",
        "created_at": "2020-11-13T10:00:00.000Z",
        "updated_at": "2020-11-13T10:00:00.000Z",
        "link": "http://something.abc.com",
        "scheduled_at": "2020-11-13T10:00:00.000Z"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-blog_posts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Project Blog Posts|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|

<h3 id="get-project-blog_posts-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-project-blog_post

<a id="opIdcreate-project-blog_post"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /projects/{project_id}/blog_posts`

*Create Project Blog Post*

Create Project Blog Post

> Body parameter

```json
{
  "name": "new topic",
  "description": "discuss",
  "commentable": false,
  "description_display_mode": "string",
  "allow_unverified_participation": true,
  "state": "published",
  "permalink": "ft",
  "sequence": 0,
  "image_url": "example.com/image.png",
  "link": "http://something.abc.com",
  "archival_reason_message": "archival message",
  "show_date": true,
  "custom_date": "2020-11-13T10:00:00.000Z",
  "tag_list": [
    "a",
    "b",
    "c"
  ]
}
```

<h3 id="create-project-blog_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|body|body|object|true|A JSON object with blog information|
|» name|body|[BlogPost/properties/name](#schemablogpost/properties/name)|false|none|
|» description|body|[BlogPost/properties/description](#schemablogpost/properties/description)|false|none|
|» commentable|body|[BlogPost/properties/commentable](#schemablogpost/properties/commentable)|false|none|
|» description_display_mode|body|[BlogPost/properties/description_display_mode](#schemablogpost/properties/description_display_mode)|false|none|
|» allow_unverified_participation|body|[BlogPost/properties/allow_unverified_participation](#schemablogpost/properties/allow_unverified_participation)|false|none|
|» state|body|[BlogPost/properties/state](#schemablogpost/properties/state)|false|none|
|» permalink|body|[BlogPost/properties/permalink](#schemablogpost/properties/permalink)|false|none|
|» sequence|body|[BlogPost/properties/sequence](#schemablogpost/properties/sequence)|false|none|
|» image_url|body|[BlogPost/properties/image_url](#schemablogpost/properties/image_url)|false|none|
|» link|body|[BlogPost/properties/link](#schemablogpost/properties/link)|false|none|
|» archival_reason_message|body|[BlogPost/properties/archival_reason_message](#schemablogpost/properties/archival_reason_message)|false|none|
|» show_date|body|[BlogPost/properties/show_date](#schemablogpost/properties/show_date)|false|none|
|» custom_date|body|[BlogPost/properties/custom_date](#schemablogpost/properties/custom_date)(date-time)|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "BlogPost",
    "attributes": {
      "id": 1,
      "name": "new topic",
      "description": "discuss",
      "permalink": "ft",
      "state": "published",
      "allow_unverified_participation": true,
      "description_display_mode": "string",
      "image_url": "example.com/image.png",
      "tag_list": [
        "a",
        "b",
        "c"
      ],
      "commentable": false,
      "archival_reason_message": "archival message",
      "sequence": 0,
      "comments_count": 0,
      "show_date": true,
      "custom_date": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "link": "http://something.abc.com",
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-project-blog_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Project Blog Post|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-project-blog_post-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-blog_post

<a id="opIdget-project-blog_post"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/blog_posts/{id}`

*Get Project Blog Post*

Get Project Blog Post

<h3 id="get-project-blog_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "BlogPost",
    "attributes": {
      "id": 1,
      "name": "new topic",
      "description": "discuss",
      "permalink": "ft",
      "state": "published",
      "allow_unverified_participation": true,
      "description_display_mode": "string",
      "image_url": "example.com/image.png",
      "tag_list": [
        "a",
        "b",
        "c"
      ],
      "commentable": false,
      "archival_reason_message": "archival message",
      "sequence": 0,
      "comments_count": 0,
      "show_date": true,
      "custom_date": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "link": "http://something.abc.com",
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-blog_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Blog Post|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|

<h3 id="get-project-blog_post-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-project-blog_post

<a id="opIdupdate-project-blog_post"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /projects/{project_id}/blog_posts/{id}`

*Update Project Blog Post*

Update Project Blog Post

> Body parameter

```json
{
  "name": "new topic",
  "description": "discuss",
  "commentable": false,
  "description_display_mode": "string",
  "allow_unverified_participation": true,
  "state": "published",
  "permalink": "ft",
  "sequence": 0,
  "image_url": "example.com/image.png",
  "link": "http://something.abc.com",
  "archival_reason_message": "archival message",
  "show_date": true,
  "custom_date": "2020-11-13T10:00:00.000Z",
  "tag_list": [
    "a",
    "b",
    "c"
  ]
}
```

<h3 id="update-project-blog_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with blog information|
|» name|body|[BlogPost/properties/name](#schemablogpost/properties/name)|false|none|
|» description|body|[BlogPost/properties/description](#schemablogpost/properties/description)|false|none|
|» commentable|body|[BlogPost/properties/commentable](#schemablogpost/properties/commentable)|false|none|
|» description_display_mode|body|[BlogPost/properties/description_display_mode](#schemablogpost/properties/description_display_mode)|false|none|
|» allow_unverified_participation|body|[BlogPost/properties/allow_unverified_participation](#schemablogpost/properties/allow_unverified_participation)|false|none|
|» state|body|[BlogPost/properties/state](#schemablogpost/properties/state)|false|none|
|» permalink|body|[BlogPost/properties/permalink](#schemablogpost/properties/permalink)|false|none|
|» sequence|body|[BlogPost/properties/sequence](#schemablogpost/properties/sequence)|false|none|
|» image_url|body|[BlogPost/properties/image_url](#schemablogpost/properties/image_url)|false|none|
|» link|body|[BlogPost/properties/link](#schemablogpost/properties/link)|false|none|
|» archival_reason_message|body|[BlogPost/properties/archival_reason_message](#schemablogpost/properties/archival_reason_message)|false|none|
|» show_date|body|[BlogPost/properties/show_date](#schemablogpost/properties/show_date)|false|none|
|» custom_date|body|[BlogPost/properties/custom_date](#schemablogpost/properties/custom_date)(date-time)|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "BlogPost",
    "attributes": {
      "id": 1,
      "name": "new topic",
      "description": "discuss",
      "permalink": "ft",
      "state": "published",
      "allow_unverified_participation": true,
      "description_display_mode": "string",
      "image_url": "example.com/image.png",
      "tag_list": [
        "a",
        "b",
        "c"
      ],
      "commentable": false,
      "archival_reason_message": "archival message",
      "sequence": 0,
      "comments_count": 0,
      "show_date": true,
      "custom_date": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "link": "http://something.abc.com",
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-project-blog_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Project Blog Post|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-project-blog_post-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-project-blog_post

<a id="opIddelete-project-blog_post"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /projects/{project_id}/blog_posts/{id}`

*Delete Project Blog Post*

Delete Project Blog Post

<h3 id="delete-project-blog_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-project-blog_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-project-blog_post-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## publish-project-blog_post

<a id="opIdpublish-project-blog_post"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{id}/publish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/blog_posts/{id}/publish`

*Publish Project Blog Post*

Publish Project Blog Post

<h3 id="publish-project-blog_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "BlogPost",
    "attributes": {
      "id": 1,
      "name": "new topic",
      "description": "discuss",
      "permalink": "ft",
      "state": "published",
      "allow_unverified_participation": true,
      "description_display_mode": "string",
      "image_url": "example.com/image.png",
      "tag_list": [
        "a",
        "b",
        "c"
      ],
      "commentable": false,
      "archival_reason_message": "archival message",
      "sequence": 0,
      "comments_count": 0,
      "show_date": true,
      "custom_date": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "link": "http://something.abc.com",
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="publish-project-blog_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Publish Project Blog Post|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="publish-project-blog_post-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unpublish-project-blog_post

<a id="opIdunpublish-project-blog_post"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{id}/unpublish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/blog_posts/{id}/unpublish`

*Unpublish Project Blog Post*

Unpublish Project Blog Post

<h3 id="unpublish-project-blog_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "BlogPost",
    "attributes": {
      "id": 1,
      "name": "new topic",
      "description": "discuss",
      "permalink": "ft",
      "state": "published",
      "allow_unverified_participation": true,
      "description_display_mode": "string",
      "image_url": "example.com/image.png",
      "tag_list": [
        "a",
        "b",
        "c"
      ],
      "commentable": false,
      "archival_reason_message": "archival message",
      "sequence": 0,
      "comments_count": 0,
      "show_date": true,
      "custom_date": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "link": "http://something.abc.com",
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unpublish-project-blog_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unpublish Project Blog Post|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unpublish-project-blog_post-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## archive-project-blog_post

<a id="opIdarchive-project-blog_post"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{id}/archive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/blog_posts/{id}/archive`

*Archive Project Blog Post*

Archive Project Blog Post

> Body parameter

```json
{
  "hide": true
}
```

<h3 id="archive-project-blog_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with archive information|
|» hide|body|boolean|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "BlogPost",
    "attributes": {
      "id": 1,
      "name": "new topic",
      "description": "discuss",
      "permalink": "ft",
      "state": "published",
      "allow_unverified_participation": true,
      "description_display_mode": "string",
      "image_url": "example.com/image.png",
      "tag_list": [
        "a",
        "b",
        "c"
      ],
      "commentable": false,
      "archival_reason_message": "archival message",
      "sequence": 0,
      "comments_count": 0,
      "show_date": true,
      "custom_date": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "link": "http://something.abc.com",
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="archive-project-blog_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Archive Project Blog Post|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="archive-project-blog_post-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unarchive-project-blog_post

<a id="opIdunarchive-project-blog_post"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{id}/unarchive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/blog_posts/{id}/unarchive`

*Unarchive Project Blog Post*

Unarchive Project Blog Post

<h3 id="unarchive-project-blog_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "BlogPost",
    "attributes": {
      "id": 1,
      "name": "new topic",
      "description": "discuss",
      "permalink": "ft",
      "state": "published",
      "allow_unverified_participation": true,
      "description_display_mode": "string",
      "image_url": "example.com/image.png",
      "tag_list": [
        "a",
        "b",
        "c"
      ],
      "commentable": false,
      "archival_reason_message": "archival message",
      "sequence": 0,
      "comments_count": 0,
      "show_date": true,
      "custom_date": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "link": "http://something.abc.com",
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unarchive-project-blog_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unarchive Project Blog Post|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unarchive-project-blog_post-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## hide-project-blog_post

<a id="opIdhide-project-blog_post"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{id}/hide',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/blog_posts/{id}/hide`

*Hide Project Blog Post*

Hide Project Blog Post

<h3 id="hide-project-blog_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "BlogPost",
    "attributes": {
      "id": 1,
      "name": "new topic",
      "description": "discuss",
      "permalink": "ft",
      "state": "published",
      "allow_unverified_participation": true,
      "description_display_mode": "string",
      "image_url": "example.com/image.png",
      "tag_list": [
        "a",
        "b",
        "c"
      ],
      "commentable": false,
      "archival_reason_message": "archival message",
      "sequence": 0,
      "comments_count": 0,
      "show_date": true,
      "custom_date": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "link": "http://something.abc.com",
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="hide-project-blog_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hide Project Blog Post|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="hide-project-blog_post-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## visible-project-blog_post

<a id="opIdvisible-project-blog_post"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{id}/visible',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/blog_posts/{id}/visible`

*Visible Project Blog Post*

Visible Project Blog Post

<h3 id="visible-project-blog_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "BlogPost",
    "attributes": {
      "id": 1,
      "name": "new topic",
      "description": "discuss",
      "permalink": "ft",
      "state": "published",
      "allow_unverified_participation": true,
      "description_display_mode": "string",
      "image_url": "example.com/image.png",
      "tag_list": [
        "a",
        "b",
        "c"
      ],
      "commentable": false,
      "archival_reason_message": "archival message",
      "sequence": 0,
      "comments_count": 0,
      "show_date": true,
      "custom_date": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "link": "http://something.abc.com",
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="visible-project-blog_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Visible Project Blog Post|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="visible-project-blog_post-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-blog_post-generate_permalink

<a id="opIdget-blog_post-generate_permalink"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/generate_permalink',
  params: {
  'name' => 'string'
}, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/blog_posts/generate_permalink`

*Get Blog Post Generate Permalink*

Get Blog Post Generate Permalink

<h3 id="get-blog_post-generate_permalink-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|name|query|string|true|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "type": "Permalink",
    "attributes": {
      "permalink": "sample"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-blog_post-generate_permalink-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Blog Post Generate Permalink|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="get-blog_post-generate_permalink-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» data|object|false|none|none|
|»» type|string|false|none|none|
|»» attributes|object|false|none|none|
|»»» permalink|string|false|none|none|

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-blog_post-schedule

<a id="opIdget-project-blog_post-schedule"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{blog_post_id}/schedule',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/blog_posts/{blog_post_id}/schedule`

*Get Project Blog Post Schedule*

Get Project Blog Post Schedule

<h3 id="get-project-blog_post-schedule-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|blog_post_id|path|integer|true|Blog Post ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Schedule",
    "attributes": {
      "id": 1,
      "action": "hide",
      "owner_id": 1,
      "owner_type": "BlogPost",
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "user_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-blog_post-schedule-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Blog Post Schedule|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-blog_post-schedule-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-project-blog_post-schedule

<a id="opIdupdate-project-blog_post-schedule"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{blog_post_id}/schedule',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /projects/{project_id}/blog_posts/{blog_post_id}/schedule`

*Update Project Blog Post Schedule*

Update Project Blog Post Schedule

> Body parameter

```json
{
  "action": "hide",
  "scheduled_at": "2020-11-13T10:00:00.000Z"
}
```

<h3 id="update-project-blog_post-schedule-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|blog_post_id|path|integer|true|Blog Post ID|
|body|body|object|true|A JSON object with schedule information|
|» action|body|[Schedule/properties/action](#schemaschedule/properties/action)|false|none|
|» scheduled_at|body|[Schedule/properties/scheduled_at](#schemaschedule/properties/scheduled_at)(date-time)|false|Date/Time of record schedule|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Schedule",
    "attributes": {
      "id": 1,
      "action": "hide",
      "owner_id": 1,
      "owner_type": "BlogPost",
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "user_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-project-blog_post-schedule-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Blog Post Schedule|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-project-blog_post-schedule-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-project-blog_post-schedule

<a id="opIddelete-project-blog_post-schedule"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{blog_post_id}/schedule',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /projects/{project_id}/blog_posts/{blog_post_id}/schedule`

*Delete Project Blog Post Schedule*

Delete Project Blog Post Schedule

<h3 id="delete-project-blog_post-schedule-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|blog_post_id|path|integer|true|Blog Post ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-project-blog_post-schedule-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-project-blog_post-schedule-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-blog_post-comments

<a id="opIdget-project-blog_post-comments"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{blog_post_id}/comments',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/blog_posts/{blog_post_id}/comments`

*Get list of Project Blog Post Comments*

Get list of Project Blog Post Comments

<h3 id="get-project-blog_post-comments-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|blog_post_id|path|integer|true|Blog Post ID|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Comment",
      "attributes": {
        "id": 2,
        "parent_id": 1,
        "comment": "testing comment",
        "image_url": "string",
        "author": "user5179",
        "created_at": "2020-11-13T10:00:00.000Z",
        "reply_count": 10,
        "email": "abc@example.com",
        "up_votes_count": 10,
        "down_votes_count": 10,
        "has_down_voted": false,
        "has_down_voted_id": 1,
        "has_up_voted": false,
        "has_up_voted_id": 1,
        "narrative_name": "testing"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-blog_post-comments-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Project Blog Post Comments|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="get-project-blog_post-comments-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-project-blog_post-comment

<a id="opIdcreate-project-blog_post-comment"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{blog_post_id}/comments',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /projects/{project_id}/blog_posts/{blog_post_id}/comments`

*Create Project Blog Post Comment*

Create Project Blog Post Comment

> Body parameter

```json
{
  "comment": "testing comment",
  "parent_id": 1
}
```

<h3 id="create-project-blog_post-comment-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|blog_post_id|path|integer|true|Blog Post ID|
|body|body|object|true|A JSON object with comment information|
|» comment|body|[Comment/properties/comment](#schemacomment/properties/comment)|false|none|
|» parent_id|body|[Comment/properties/parent_id](#schemacomment/properties/parent_id)|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Comment",
    "attributes": {
      "id": 2,
      "parent_id": 1,
      "comment": "testing comment",
      "image_url": "string",
      "author": "user5179",
      "created_at": "2020-11-13T10:00:00.000Z",
      "reply_count": 10,
      "email": "abc@example.com",
      "up_votes_count": 10,
      "down_votes_count": 10,
      "has_down_voted": false,
      "has_down_voted_id": 1,
      "has_up_voted": false,
      "has_up_voted_id": 1,
      "narrative_name": "testing"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-project-blog_post-comment-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Project Blog Post Comment|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-project-blog_post-comment-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-blog_post-comment

<a id="opIdget-project-blog_post-comment"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{blog_post_id}/comments/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/blog_posts/{blog_post_id}/comments/{id}`

*Get Project Blog Post Comment*

Get Project Blog Post Comment

<h3 id="get-project-blog_post-comment-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|blog_post_id|path|integer|true|Blog Post ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Comment",
    "attributes": {
      "id": 2,
      "parent_id": 1,
      "comment": "testing comment",
      "image_url": "string",
      "author": "user5179",
      "created_at": "2020-11-13T10:00:00.000Z",
      "reply_count": 10,
      "email": "abc@example.com",
      "up_votes_count": 10,
      "down_votes_count": 10,
      "has_down_voted": false,
      "has_down_voted_id": 1,
      "has_up_voted": false,
      "has_up_voted_id": 1,
      "narrative_name": "testing"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-blog_post-comment-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Blog Post Comment|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-blog_post-comment-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-project-blog_post-comment

<a id="opIddelete-project-blog_post-comment"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{blog_post_id}/comments/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /projects/{project_id}/blog_posts/{blog_post_id}/comments/{id}`

*Delete Project Blog Post Comment*

Delete Project Blog Post Comment

<h3 id="delete-project-blog_post-comment-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|blog_post_id|path|integer|true|Blog Post ID|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-project-blog_post-comment-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-project-blog_post-comment-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-blog_post-mention_suggestions

<a id="opIdget-project-blog_post-mention_suggestions"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/blog_posts/{id}/mention_suggestions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/blog_posts/{id}/mention_suggestions`

*Get list of Project Blog Post Mention Suggestions*

Get list of Project Blog Post Mention Suggestions

<h3 id="get-project-blog_post-mention_suggestions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Mention Suggestion",
      "attributes": {
        "id": 2,
        "login": "string",
        "type": "string",
        "created_at": "2020-11-13T10:00:00.000Z",
        "last_seen_at": "1 day ago"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-blog_post-mention_suggestions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Project Blog Post Mention Suggestions|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-blog_post-mention_suggestions-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-brainstormers">Brainstormers</h1>

Brainstormers Management

## get-project-brainstormers

<a id="opIdget-project-brainstormers"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/brainstormers`

*Get list of Project Brainstormers*

Get list of Project Brainstormers

<h3 id="get-project-brainstormers-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Brainstormer",
      "attributes": {
        "id": 1,
        "name": "testing",
        "description": "testing description",
        "permalink": "sample-brainstormer",
        "state": "published",
        "tag_list": [
          "abc",
          "xyz"
        ],
        "voting_start_at": "2020-11-13T10:00:00.000Z",
        "voting_end_at": "2020-11-13T10:00:00.000Z",
        "image_url": "string",
        "archival_reason_message": "archival message",
        "ideas_count": 10,
        "created_at": "2020-11-13T10:00:00.000Z",
        "sticked": false,
        "updated_at": "2020-11-13T10:00:00.000Z",
        "sequence": 1,
        "notifications_emails": "abc@example.com",
        "allow_comments_for_ideas": false,
        "allow_file_upload_for_ideas": false,
        "send_acknowledgement_to_admins": true,
        "send_acknowledgement": true,
        "allow_unverified_participation": true,
        "scheduled_at": "2020-11-13T10:00:00.000Z"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-brainstormers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Project Brainstormers|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-brainstormers-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-project-brainstormer

<a id="opIdcreate-project-brainstormer"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /projects/{project_id}/brainstormers`

*Create Project Brainstormer*

Create Project Brainstormer

> Body parameter

```json
{
  "name": "testing",
  "description": "testing description",
  "permalink": "sample-brainstormer",
  "voting_start_at": "2020-11-13T10:00:00.000Z",
  "voting_end_at": "2020-11-13T10:00:00.000Z",
  "image_url": "string",
  "sequence": 1,
  "notifications_emails": "abc@example.com",
  "archival_reason_message": "archival message",
  "send_acknowledgement": true,
  "send_acknowledgement_to_admins": true,
  "sticked": false,
  "allow_unverified_participation": true,
  "allow_comments_for_ideas": false,
  "allow_file_upload_for_ideas": false,
  "tag_list": [
    "abc",
    "xyz"
  ]
}
```

<h3 id="create-project-brainstormer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|body|body|object|true|A JSON object with brainstormer information|
|» name|body|[Brainstormer/properties/name](#schemabrainstormer/properties/name)|false|none|
|» description|body|[Brainstormer/properties/description](#schemabrainstormer/properties/description)|false|none|
|» permalink|body|[Brainstormer/properties/permalink](#schemabrainstormer/properties/permalink)|false|none|
|» voting_start_at|body|[Brainstormer/properties/voting_start_at](#schemabrainstormer/properties/voting_start_at)(date-time)|false|Date/Time of record voting_start_at|
|» voting_end_at|body|[Brainstormer/properties/voting_end_at](#schemabrainstormer/properties/voting_end_at)(date-time)|false|Date/Time of record voting_end_at|
|» image_url|body|[Brainstormer/properties/image_url](#schemabrainstormer/properties/image_url)|false|none|
|» sequence|body|[Brainstormer/properties/sequence](#schemabrainstormer/properties/sequence)|false|none|
|» notifications_emails|body|[Brainstormer/properties/notifications_emails](#schemabrainstormer/properties/notifications_emails)|false|none|
|» archival_reason_message|body|[Brainstormer/properties/archival_reason_message](#schemabrainstormer/properties/archival_reason_message)|false|none|
|» send_acknowledgement|body|[Brainstormer/properties/send_acknowledgement](#schemabrainstormer/properties/send_acknowledgement)|false|none|
|» send_acknowledgement_to_admins|body|[Brainstormer/properties/send_acknowledgement_to_admins](#schemabrainstormer/properties/send_acknowledgement_to_admins)|false|none|
|» sticked|body|[Brainstormer/properties/sticked](#schemabrainstormer/properties/sticked)|false|none|
|» allow_unverified_participation|body|[Brainstormer/properties/allow_unverified_participation](#schemabrainstormer/properties/allow_unverified_participation)|false|none|
|» allow_comments_for_ideas|body|[Brainstormer/properties/allow_comments_for_ideas](#schemabrainstormer/properties/allow_comments_for_ideas)|false|none|
|» allow_file_upload_for_ideas|body|[Brainstormer/properties/allow_file_upload_for_ideas](#schemabrainstormer/properties/allow_file_upload_for_ideas)|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Brainstormer",
    "attributes": {
      "id": 1,
      "name": "testing",
      "description": "testing description",
      "permalink": "sample-brainstormer",
      "state": "published",
      "tag_list": [
        "abc",
        "xyz"
      ],
      "voting_start_at": "2020-11-13T10:00:00.000Z",
      "voting_end_at": "2020-11-13T10:00:00.000Z",
      "image_url": "string",
      "archival_reason_message": "archival message",
      "ideas_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "sticked": false,
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 1,
      "notifications_emails": "abc@example.com",
      "allow_comments_for_ideas": false,
      "allow_file_upload_for_ideas": false,
      "send_acknowledgement_to_admins": true,
      "send_acknowledgement": true,
      "allow_unverified_participation": true,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-project-brainstormer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Project Brainstormer|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-project-brainstormer-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-brainstormer

<a id="opIdget-project-brainstormer"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/brainstormers/{id}`

*Get Project Brainstormer*

Get Project Brainstormer

<h3 id="get-project-brainstormer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Brainstormer",
    "attributes": {
      "id": 1,
      "name": "testing",
      "description": "testing description",
      "permalink": "sample-brainstormer",
      "state": "published",
      "tag_list": [
        "abc",
        "xyz"
      ],
      "voting_start_at": "2020-11-13T10:00:00.000Z",
      "voting_end_at": "2020-11-13T10:00:00.000Z",
      "image_url": "string",
      "archival_reason_message": "archival message",
      "ideas_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "sticked": false,
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 1,
      "notifications_emails": "abc@example.com",
      "allow_comments_for_ideas": false,
      "allow_file_upload_for_ideas": false,
      "send_acknowledgement_to_admins": true,
      "send_acknowledgement": true,
      "allow_unverified_participation": true,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-brainstormer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Brainstormer|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-brainstormer-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-project-brainstormer

<a id="opIdupdate-project-brainstormer"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /projects/{project_id}/brainstormers/{id}`

*Update Project Brainstormer*

Update Project Brainstormer

> Body parameter

```json
{
  "name": "testing",
  "description": "testing description",
  "permalink": "sample-brainstormer",
  "voting_start_at": "2020-11-13T10:00:00.000Z",
  "voting_end_at": "2020-11-13T10:00:00.000Z",
  "image_url": "string",
  "sequence": 1,
  "notifications_emails": "abc@example.com",
  "archival_reason_message": "archival message",
  "send_acknowledgement": true,
  "send_acknowledgement_to_admins": true,
  "sticked": false,
  "allow_unverified_participation": true,
  "allow_comments_for_ideas": false,
  "allow_file_upload_for_ideas": false,
  "tag_list": [
    "abc",
    "xyz"
  ]
}
```

<h3 id="update-project-brainstormer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with brainstormer information|
|» name|body|[Brainstormer/properties/name](#schemabrainstormer/properties/name)|false|none|
|» description|body|[Brainstormer/properties/description](#schemabrainstormer/properties/description)|false|none|
|» permalink|body|[Brainstormer/properties/permalink](#schemabrainstormer/properties/permalink)|false|none|
|» voting_start_at|body|[Brainstormer/properties/voting_start_at](#schemabrainstormer/properties/voting_start_at)(date-time)|false|Date/Time of record voting_start_at|
|» voting_end_at|body|[Brainstormer/properties/voting_end_at](#schemabrainstormer/properties/voting_end_at)(date-time)|false|Date/Time of record voting_end_at|
|» image_url|body|[Brainstormer/properties/image_url](#schemabrainstormer/properties/image_url)|false|none|
|» sequence|body|[Brainstormer/properties/sequence](#schemabrainstormer/properties/sequence)|false|none|
|» notifications_emails|body|[Brainstormer/properties/notifications_emails](#schemabrainstormer/properties/notifications_emails)|false|none|
|» archival_reason_message|body|[Brainstormer/properties/archival_reason_message](#schemabrainstormer/properties/archival_reason_message)|false|none|
|» send_acknowledgement|body|[Brainstormer/properties/send_acknowledgement](#schemabrainstormer/properties/send_acknowledgement)|false|none|
|» send_acknowledgement_to_admins|body|[Brainstormer/properties/send_acknowledgement_to_admins](#schemabrainstormer/properties/send_acknowledgement_to_admins)|false|none|
|» sticked|body|[Brainstormer/properties/sticked](#schemabrainstormer/properties/sticked)|false|none|
|» allow_unverified_participation|body|[Brainstormer/properties/allow_unverified_participation](#schemabrainstormer/properties/allow_unverified_participation)|false|none|
|» allow_comments_for_ideas|body|[Brainstormer/properties/allow_comments_for_ideas](#schemabrainstormer/properties/allow_comments_for_ideas)|false|none|
|» allow_file_upload_for_ideas|body|[Brainstormer/properties/allow_file_upload_for_ideas](#schemabrainstormer/properties/allow_file_upload_for_ideas)|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Brainstormer",
    "attributes": {
      "id": 1,
      "name": "testing",
      "description": "testing description",
      "permalink": "sample-brainstormer",
      "state": "published",
      "tag_list": [
        "abc",
        "xyz"
      ],
      "voting_start_at": "2020-11-13T10:00:00.000Z",
      "voting_end_at": "2020-11-13T10:00:00.000Z",
      "image_url": "string",
      "archival_reason_message": "archival message",
      "ideas_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "sticked": false,
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 1,
      "notifications_emails": "abc@example.com",
      "allow_comments_for_ideas": false,
      "allow_file_upload_for_ideas": false,
      "send_acknowledgement_to_admins": true,
      "send_acknowledgement": true,
      "allow_unverified_participation": true,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-project-brainstormer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Project Brainstormer|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-project-brainstormer-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-project-brainstormer

<a id="opIddelete-project-brainstormer"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /projects/{project_id}/brainstormers/{id}`

*Delete Project Brainstormer*

Delete Project Brainstormer

<h3 id="delete-project-brainstormer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-project-brainstormer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-project-brainstormer-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## publish-project-brainstormer

<a id="opIdpublish-project-brainstormer"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{id}/publish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/brainstormers/{id}/publish`

*Publish Project Brainstormer*

Publish Project Brainstormer

<h3 id="publish-project-brainstormer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Brainstormer",
    "attributes": {
      "id": 1,
      "name": "testing",
      "description": "testing description",
      "permalink": "sample-brainstormer",
      "state": "published",
      "tag_list": [
        "abc",
        "xyz"
      ],
      "voting_start_at": "2020-11-13T10:00:00.000Z",
      "voting_end_at": "2020-11-13T10:00:00.000Z",
      "image_url": "string",
      "archival_reason_message": "archival message",
      "ideas_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "sticked": false,
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 1,
      "notifications_emails": "abc@example.com",
      "allow_comments_for_ideas": false,
      "allow_file_upload_for_ideas": false,
      "send_acknowledgement_to_admins": true,
      "send_acknowledgement": true,
      "allow_unverified_participation": true,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="publish-project-brainstormer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Publish Project Brainstormer|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="publish-project-brainstormer-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unpublish-project-brainstormer

<a id="opIdunpublish-project-brainstormer"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{id}/unpublish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/brainstormers/{id}/unpublish`

*Unpublish Project Brainstormer*

Unpublish Project Brainstormer

<h3 id="unpublish-project-brainstormer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Brainstormer",
    "attributes": {
      "id": 1,
      "name": "testing",
      "description": "testing description",
      "permalink": "sample-brainstormer",
      "state": "published",
      "tag_list": [
        "abc",
        "xyz"
      ],
      "voting_start_at": "2020-11-13T10:00:00.000Z",
      "voting_end_at": "2020-11-13T10:00:00.000Z",
      "image_url": "string",
      "archival_reason_message": "archival message",
      "ideas_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "sticked": false,
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 1,
      "notifications_emails": "abc@example.com",
      "allow_comments_for_ideas": false,
      "allow_file_upload_for_ideas": false,
      "send_acknowledgement_to_admins": true,
      "send_acknowledgement": true,
      "allow_unverified_participation": true,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unpublish-project-brainstormer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unpublish Project Brainstormer|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unpublish-project-brainstormer-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## archive-project-brainstormer

<a id="opIdarchive-project-brainstormer"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{id}/archive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/brainstormers/{id}/archive`

*Archive Project Brainstormer*

Archive Project Brainstormer

> Body parameter

```json
{
  "hide": true
}
```

<h3 id="archive-project-brainstormer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with archive information|
|» hide|body|boolean|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Brainstormer",
    "attributes": {
      "id": 1,
      "name": "testing",
      "description": "testing description",
      "permalink": "sample-brainstormer",
      "state": "published",
      "tag_list": [
        "abc",
        "xyz"
      ],
      "voting_start_at": "2020-11-13T10:00:00.000Z",
      "voting_end_at": "2020-11-13T10:00:00.000Z",
      "image_url": "string",
      "archival_reason_message": "archival message",
      "ideas_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "sticked": false,
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 1,
      "notifications_emails": "abc@example.com",
      "allow_comments_for_ideas": false,
      "allow_file_upload_for_ideas": false,
      "send_acknowledgement_to_admins": true,
      "send_acknowledgement": true,
      "allow_unverified_participation": true,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="archive-project-brainstormer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Archive Project Brainstormer|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="archive-project-brainstormer-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unarchive-project-brainstormer

<a id="opIdunarchive-project-brainstormer"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{id}/unarchive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/brainstormers/{id}/unarchive`

*Unarchive Project Brainstormer*

Unarchive Project Brainstormer

<h3 id="unarchive-project-brainstormer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Brainstormer",
    "attributes": {
      "id": 1,
      "name": "testing",
      "description": "testing description",
      "permalink": "sample-brainstormer",
      "state": "published",
      "tag_list": [
        "abc",
        "xyz"
      ],
      "voting_start_at": "2020-11-13T10:00:00.000Z",
      "voting_end_at": "2020-11-13T10:00:00.000Z",
      "image_url": "string",
      "archival_reason_message": "archival message",
      "ideas_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "sticked": false,
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 1,
      "notifications_emails": "abc@example.com",
      "allow_comments_for_ideas": false,
      "allow_file_upload_for_ideas": false,
      "send_acknowledgement_to_admins": true,
      "send_acknowledgement": true,
      "allow_unverified_participation": true,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unarchive-project-brainstormer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unarchive Project Brainstormer|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unarchive-project-brainstormer-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## hide-project-brainstormer

<a id="opIdhide-project-brainstormer"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{id}/hide',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/brainstormers/{id}/hide`

*Hide Project Brainstormer*

Hide Project Brainstormer

<h3 id="hide-project-brainstormer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Brainstormer",
    "attributes": {
      "id": 1,
      "name": "testing",
      "description": "testing description",
      "permalink": "sample-brainstormer",
      "state": "published",
      "tag_list": [
        "abc",
        "xyz"
      ],
      "voting_start_at": "2020-11-13T10:00:00.000Z",
      "voting_end_at": "2020-11-13T10:00:00.000Z",
      "image_url": "string",
      "archival_reason_message": "archival message",
      "ideas_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "sticked": false,
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 1,
      "notifications_emails": "abc@example.com",
      "allow_comments_for_ideas": false,
      "allow_file_upload_for_ideas": false,
      "send_acknowledgement_to_admins": true,
      "send_acknowledgement": true,
      "allow_unverified_participation": true,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="hide-project-brainstormer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hide Project Brainstormer|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="hide-project-brainstormer-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## visible-project-brainstormer

<a id="opIdvisible-project-brainstormer"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{id}/visible',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/brainstormers/{id}/visible`

*Visible Project Brainstormer*

Visible Project Brainstormer

<h3 id="visible-project-brainstormer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Brainstormer",
    "attributes": {
      "id": 1,
      "name": "testing",
      "description": "testing description",
      "permalink": "sample-brainstormer",
      "state": "published",
      "tag_list": [
        "abc",
        "xyz"
      ],
      "voting_start_at": "2020-11-13T10:00:00.000Z",
      "voting_end_at": "2020-11-13T10:00:00.000Z",
      "image_url": "string",
      "archival_reason_message": "archival message",
      "ideas_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "sticked": false,
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 1,
      "notifications_emails": "abc@example.com",
      "allow_comments_for_ideas": false,
      "allow_file_upload_for_ideas": false,
      "send_acknowledgement_to_admins": true,
      "send_acknowledgement": true,
      "allow_unverified_participation": true,
      "scheduled_at": "2020-11-13T10:00:00.000Z"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="visible-project-brainstormer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Visible Project Brainstormer|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="visible-project-brainstormer-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-brainstormer-votes

<a id="opIdget-project-brainstormer-votes"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{brainstormer_id}/votes',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/brainstormers/{brainstormer_id}/votes`

*Get list of Project Brainstormer Votes*

Get list of Project Brainstormer Votes

<h3 id="get-project-brainstormer-votes-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|brainstormer_id|path|integer|true|Brainstormer ID|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Idea",
      "attributes": {
        "id": 1,
        "name": "Test",
        "description": "description 122",
        "image_url": "string",
        "author": "user8179",
        "votes_count": 10,
        "created_at": "2020-11-13T10:00:00.000Z",
        "email": "user9245@example.com"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-brainstormer-votes-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Project Brainstormer Votes|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-brainstormer-votes-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-brainstormer-schedule

<a id="opIdget-project-brainstormer-schedule"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{brainstormer_id}/schedule',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/brainstormers/{brainstormer_id}/schedule`

*Get Project Brainstormer Schedule*

Get Project Brainstormer Schedule

<h3 id="get-project-brainstormer-schedule-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|brainstormer_id|path|integer|true|Brainstormer ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Schedule",
    "attributes": {
      "id": 1,
      "action": "hide",
      "owner_id": 1,
      "owner_type": "BlogPost",
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "user_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-brainstormer-schedule-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Brainstormer Schedule|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="get-project-brainstormer-schedule-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-project-brainstormer-schedule

<a id="opIdupdate-project-brainstormer-schedule"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{brainstormer_id}/schedule',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /projects/{project_id}/brainstormers/{brainstormer_id}/schedule`

*Update Project Brainstormer Schedule*

Update Project Brainstormer Schedule

> Body parameter

```json
{
  "action": "hide",
  "scheduled_at": "2020-11-13T10:00:00.000Z"
}
```

<h3 id="update-project-brainstormer-schedule-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|brainstormer_id|path|integer|true|Brainstormer ID|
|body|body|object|true|A JSON object with schedule information|
|» action|body|[Schedule/properties/action](#schemaschedule/properties/action)|false|none|
|» scheduled_at|body|[Schedule/properties/scheduled_at](#schemaschedule/properties/scheduled_at)(date-time)|false|Date/Time of record schedule|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Schedule",
    "attributes": {
      "id": 1,
      "action": "hide",
      "owner_id": 1,
      "owner_type": "BlogPost",
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "user_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-project-brainstormer-schedule-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Brainstormer Schedule|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-project-brainstormer-schedule-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-project-brainstormer-schedule

<a id="opIddelete-project-brainstormer-schedule"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{brainstormer_id}/schedule',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /projects/{project_id}/brainstormers/{brainstormer_id}/schedule`

*Delete Project Brainstormer Schedule*

Delete Project Brainstormer Schedule

<h3 id="delete-project-brainstormer-schedule-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|brainstormer_id|path|integer|true|Brainstormer ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-project-brainstormer-schedule-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-project-brainstormer-schedule-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-brainstormers-generate_permalink

<a id="opIdget-project-brainstormers-generate_permalink"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/generate_permalink',
  params: {
  'name' => 'string'
}, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/brainstormers/generate_permalink`

*Get Brainstormer Generate Permalink*

Get Brainstormer Generate Permalink

<h3 id="get-project-brainstormers-generate_permalink-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|name|query|string|true|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "type": "Permalink",
    "attributes": {
      "permalink": "sample"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-brainstormers-generate_permalink-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Brainstormer Generate Permalink|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="get-project-brainstormers-generate_permalink-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» data|object|false|none|none|
|»» type|string|false|none|none|
|»» attributes|object|false|none|none|
|»»» permalink|string|false|none|none|

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-brainstormers-comments

<a id="opIdget-project-brainstormers-comments"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/brainstormers/{brainstormer_id}/comments',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/brainstormers/{brainstormer_id}/comments`

*Get list of Project Brainstormer Comments*

Get list of Project Brainstormer Comments

<h3 id="get-project-brainstormers-comments-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|brainstormer_id|path|integer|true|Brainstormer ID|
|page|query|integer|false|none|
|per_page|query|integer|false|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Comment",
      "attributes": {
        "id": 2,
        "parent_id": 1,
        "comment": "testing comment",
        "image_url": "string",
        "author": "user5179",
        "created_at": "2020-11-13T10:00:00.000Z",
        "reply_count": 10,
        "email": "abc@example.com",
        "up_votes_count": 10,
        "down_votes_count": 10,
        "has_down_voted": false,
        "has_down_voted_id": 1,
        "has_up_voted": false,
        "has_up_voted_id": 1,
        "narrative_name": "testing"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-brainstormers-comments-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Project Brainstormer Comments|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-brainstormers-comments-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-survey-tools">Survey Tools</h1>

Survey Tools Management

## get-project-survey_tools

<a id="opIdget-project-survey_tools"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/survey_tools',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/survey_tools`

*Get list of Project Survey Tools*

Get list of Project Survey Tools

<h3 id="get-project-survey_tools-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Survey Tool",
      "attributes": {
        "id": 1,
        "name": "survey 353",
        "description": "<img src=\"something.png\" /> Description",
        "permalink": "survey_tool355-92",
        "state": "draft",
        "image_url": "another_thing.png",
        "archival_reason_message": "archival message",
        "send_acknowledgement": true,
        "send_acknowledgement_to_admin": true,
        "notification_emails": "devteam@bangthetable.com",
        "allow_anonymous_participation": false,
        "allow_user_to_post_multiple_times": false,
        "allow_unverified_participation": true,
        "thanks_msg": "string",
        "pinned": true,
        "tag_list": [
          "string"
        ],
        "responses_count": 10,
        "created_at": "2020-11-13T10:00:00.000Z",
        "updated_at": "2020-11-13T10:00:00.000Z",
        "sequence": 0,
        "randomize_pages": false,
        "randomize_questions": false,
        "randomize_options": false,
        "modified_at": "2020-11-13T10:00:00.000Z",
        "submit_button_text": "string",
        "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
        "show_response_count": false,
        "show_results": true,
        "is_new_survey": true,
        "show_progress_bar": true,
        "file_question_count": 0,
        "scheduled_at": "2020-11-13T10:00:00.000Z",
        "visibility": "inherit"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-survey_tools-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Project Survey Tools|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-survey_tools-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-project-survey_tool

<a id="opIdcreate-project-survey_tool"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/projects/{project_id}/survey_tools',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /projects/{project_id}/survey_tools`

*Create Project Survey Tool*

Create Project Survey Tool

> Body parameter

```json
{
  "name": "survey 353",
  "description": "<img src=\"something.png\" /> Description",
  "permalink": "survey_tool355-92",
  "send_acknowledgement": true,
  "send_acknowledgement_to_admin": true,
  "notification_emails": "devteam@bangthetable.com",
  "allow_anonymous_participation": false,
  "allow_unverified_participation": true,
  "allow_user_to_post_multiple_times": false,
  "thanks_msg": "string",
  "owner_id": 1,
  "owner_type": "string",
  "sequence": 0,
  "randomize_pages": false,
  "randomize_options": false,
  "image_url": "another_thing.png",
  "randomize_questions": false,
  "archival_reason_message": "archival message",
  "submit_button_text": "string",
  "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
  "show_progress_bar": true,
  "show_response_count": false,
  "visibility": "inherit",
  "tag_list": [
    "string"
  ]
}
```

<h3 id="create-project-survey_tool-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|body|body|object|true|A JSON object with survey tool information|
|» name|body|[SurveyTool/properties/name](#schemasurveytool/properties/name)|false|none|
|» description|body|[SurveyTool/properties/description](#schemasurveytool/properties/description)|false|none|
|» permalink|body|[SurveyTool/properties/permalink](#schemasurveytool/properties/permalink)|false|none|
|» send_acknowledgement|body|[SurveyTool/properties/send_acknowledgement](#schemasurveytool/properties/send_acknowledgement)|false|none|
|» send_acknowledgement_to_admin|body|[SurveyTool/properties/send_acknowledgement_to_admin](#schemasurveytool/properties/send_acknowledgement_to_admin)|false|none|
|» notification_emails|body|[SurveyTool/properties/notification_emails](#schemasurveytool/properties/notification_emails)|false|none|
|» allow_anonymous_participation|body|[SurveyTool/properties/allow_anonymous_participation](#schemasurveytool/properties/allow_anonymous_participation)|false|none|
|» allow_unverified_participation|body|[SurveyTool/properties/allow_unverified_participation](#schemasurveytool/properties/allow_unverified_participation)|false|none|
|» allow_user_to_post_multiple_times|body|[SurveyTool/properties/allow_user_to_post_multiple_times](#schemasurveytool/properties/allow_user_to_post_multiple_times)|false|none|
|» thanks_msg|body|[SurveyTool/properties/thanks_msg](#schemasurveytool/properties/thanks_msg)|false|none|
|» owner_id|body|integer|false|none|
|» owner_type|body|string|false|none|
|» sequence|body|[SurveyTool/properties/sequence](#schemasurveytool/properties/sequence)|false|none|
|» randomize_pages|body|[SurveyTool/properties/randomize_pages](#schemasurveytool/properties/randomize_pages)|false|none|
|» randomize_options|body|[SurveyTool/properties/randomize_options](#schemasurveytool/properties/randomize_options)|false|none|
|» image_url|body|[SurveyTool/properties/image_url](#schemasurveytool/properties/image_url)|false|none|
|» randomize_questions|body|[SurveyTool/properties/randomize_questions](#schemasurveytool/properties/randomize_questions)|false|none|
|» archival_reason_message|body|[SurveyTool/properties/archival_reason_message](#schemasurveytool/properties/archival_reason_message)|false|none|
|» submit_button_text|body|[SurveyTool/properties/submit_button_text](#schemasurveytool/properties/submit_button_text)|false|none|
|» multiple_times_msg|body|[SurveyTool/properties/multiple_times_msg](#schemasurveytool/properties/multiple_times_msg)|false|none|
|» show_progress_bar|body|[SurveyTool/properties/show_progress_bar](#schemasurveytool/properties/show_progress_bar)|false|none|
|» show_response_count|body|[SurveyTool/properties/show_response_count](#schemasurveytool/properties/show_response_count)|false|none|
|» visibility|body|[SurveyTool/properties/visibility](#schemasurveytool/properties/visibility)|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Survey Tool",
    "attributes": {
      "id": 1,
      "name": "survey 353",
      "description": "<img src=\"something.png\" /> Description",
      "permalink": "survey_tool355-92",
      "state": "draft",
      "image_url": "another_thing.png",
      "archival_reason_message": "archival message",
      "send_acknowledgement": true,
      "send_acknowledgement_to_admin": true,
      "notification_emails": "devteam@bangthetable.com",
      "allow_anonymous_participation": false,
      "allow_user_to_post_multiple_times": false,
      "allow_unverified_participation": true,
      "thanks_msg": "string",
      "pinned": true,
      "tag_list": [
        "string"
      ],
      "responses_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 0,
      "randomize_pages": false,
      "randomize_questions": false,
      "randomize_options": false,
      "modified_at": "2020-11-13T10:00:00.000Z",
      "submit_button_text": "string",
      "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
      "show_response_count": false,
      "show_results": true,
      "is_new_survey": true,
      "show_progress_bar": true,
      "file_question_count": 0,
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-project-survey_tool-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Project Survey Tool|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-project-survey_tool-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-survey_tool

<a id="opIdget-project-survey_tool"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/survey_tools/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/survey_tools/{id}`

*Get Project Survey Tool*

Get Project Survey Tool

<h3 id="get-project-survey_tool-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Survey Tool",
    "attributes": {
      "id": 1,
      "name": "survey 353",
      "description": "<img src=\"something.png\" /> Description",
      "permalink": "survey_tool355-92",
      "state": "draft",
      "image_url": "another_thing.png",
      "archival_reason_message": "archival message",
      "send_acknowledgement": true,
      "send_acknowledgement_to_admin": true,
      "notification_emails": "devteam@bangthetable.com",
      "allow_anonymous_participation": false,
      "allow_user_to_post_multiple_times": false,
      "allow_unverified_participation": true,
      "thanks_msg": "string",
      "pinned": true,
      "tag_list": [
        "string"
      ],
      "responses_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 0,
      "randomize_pages": false,
      "randomize_questions": false,
      "randomize_options": false,
      "modified_at": "2020-11-13T10:00:00.000Z",
      "submit_button_text": "string",
      "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
      "show_response_count": false,
      "show_results": true,
      "is_new_survey": true,
      "show_progress_bar": true,
      "file_question_count": 0,
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-survey_tool-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Survey Tool|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-survey_tool-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-project-survey_tool

<a id="opIdupdate-project-survey_tool"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/projects/{project_id}/survey_tools/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /projects/{project_id}/survey_tools/{id}`

*Update Project Survey Tool*

Update Project Survey Tool

> Body parameter

```json
{
  "name": "survey 353",
  "description": "<img src=\"something.png\" /> Description",
  "permalink": "survey_tool355-92",
  "send_acknowledgement": true,
  "send_acknowledgement_to_admin": true,
  "notification_emails": "devteam@bangthetable.com",
  "allow_anonymous_participation": false,
  "allow_unverified_participation": true,
  "allow_user_to_post_multiple_times": false,
  "thanks_msg": "string",
  "owner_id": 1,
  "owner_type": "string",
  "sequence": 0,
  "randomize_pages": false,
  "randomize_options": false,
  "image_url": "another_thing.png",
  "randomize_questions": false,
  "archival_reason_message": "archival message",
  "submit_button_text": "string",
  "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
  "show_progress_bar": true,
  "show_response_count": false,
  "visibility": "inherit",
  "tag_list": [
    "string"
  ]
}
```

<h3 id="update-project-survey_tool-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with survey tool information|
|» name|body|[SurveyTool/properties/name](#schemasurveytool/properties/name)|false|none|
|» description|body|[SurveyTool/properties/description](#schemasurveytool/properties/description)|false|none|
|» permalink|body|[SurveyTool/properties/permalink](#schemasurveytool/properties/permalink)|false|none|
|» send_acknowledgement|body|[SurveyTool/properties/send_acknowledgement](#schemasurveytool/properties/send_acknowledgement)|false|none|
|» send_acknowledgement_to_admin|body|[SurveyTool/properties/send_acknowledgement_to_admin](#schemasurveytool/properties/send_acknowledgement_to_admin)|false|none|
|» notification_emails|body|[SurveyTool/properties/notification_emails](#schemasurveytool/properties/notification_emails)|false|none|
|» allow_anonymous_participation|body|[SurveyTool/properties/allow_anonymous_participation](#schemasurveytool/properties/allow_anonymous_participation)|false|none|
|» allow_unverified_participation|body|[SurveyTool/properties/allow_unverified_participation](#schemasurveytool/properties/allow_unverified_participation)|false|none|
|» allow_user_to_post_multiple_times|body|[SurveyTool/properties/allow_user_to_post_multiple_times](#schemasurveytool/properties/allow_user_to_post_multiple_times)|false|none|
|» thanks_msg|body|[SurveyTool/properties/thanks_msg](#schemasurveytool/properties/thanks_msg)|false|none|
|» owner_id|body|integer|false|none|
|» owner_type|body|string|false|none|
|» sequence|body|[SurveyTool/properties/sequence](#schemasurveytool/properties/sequence)|false|none|
|» randomize_pages|body|[SurveyTool/properties/randomize_pages](#schemasurveytool/properties/randomize_pages)|false|none|
|» randomize_options|body|[SurveyTool/properties/randomize_options](#schemasurveytool/properties/randomize_options)|false|none|
|» image_url|body|[SurveyTool/properties/image_url](#schemasurveytool/properties/image_url)|false|none|
|» randomize_questions|body|[SurveyTool/properties/randomize_questions](#schemasurveytool/properties/randomize_questions)|false|none|
|» archival_reason_message|body|[SurveyTool/properties/archival_reason_message](#schemasurveytool/properties/archival_reason_message)|false|none|
|» submit_button_text|body|[SurveyTool/properties/submit_button_text](#schemasurveytool/properties/submit_button_text)|false|none|
|» multiple_times_msg|body|[SurveyTool/properties/multiple_times_msg](#schemasurveytool/properties/multiple_times_msg)|false|none|
|» show_progress_bar|body|[SurveyTool/properties/show_progress_bar](#schemasurveytool/properties/show_progress_bar)|false|none|
|» show_response_count|body|[SurveyTool/properties/show_response_count](#schemasurveytool/properties/show_response_count)|false|none|
|» visibility|body|[SurveyTool/properties/visibility](#schemasurveytool/properties/visibility)|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Survey Tool",
    "attributes": {
      "id": 1,
      "name": "survey 353",
      "description": "<img src=\"something.png\" /> Description",
      "permalink": "survey_tool355-92",
      "state": "draft",
      "image_url": "another_thing.png",
      "archival_reason_message": "archival message",
      "send_acknowledgement": true,
      "send_acknowledgement_to_admin": true,
      "notification_emails": "devteam@bangthetable.com",
      "allow_anonymous_participation": false,
      "allow_user_to_post_multiple_times": false,
      "allow_unverified_participation": true,
      "thanks_msg": "string",
      "pinned": true,
      "tag_list": [
        "string"
      ],
      "responses_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 0,
      "randomize_pages": false,
      "randomize_questions": false,
      "randomize_options": false,
      "modified_at": "2020-11-13T10:00:00.000Z",
      "submit_button_text": "string",
      "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
      "show_response_count": false,
      "show_results": true,
      "is_new_survey": true,
      "show_progress_bar": true,
      "file_question_count": 0,
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-project-survey_tool-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Project Survey Tool|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-project-survey_tool-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-project-survey_tool

<a id="opIddelete-project-survey_tool"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/projects/{project_id}/survey_tools/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /projects/{project_id}/survey_tools/{id}`

*Delete Project Survey Tool*

Delete Project Survey Tool

<h3 id="delete-project-survey_tool-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-project-survey_tool-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-project-survey_tool-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## publish-project-survey_tool

<a id="opIdpublish-project-survey_tool"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/survey_tools/{id}/publish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/survey_tools/{id}/publish`

*Publish Project Survey Tool*

Publish Project Survey Tool

<h3 id="publish-project-survey_tool-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Survey Tool",
    "attributes": {
      "id": 1,
      "name": "survey 353",
      "description": "<img src=\"something.png\" /> Description",
      "permalink": "survey_tool355-92",
      "state": "draft",
      "image_url": "another_thing.png",
      "archival_reason_message": "archival message",
      "send_acknowledgement": true,
      "send_acknowledgement_to_admin": true,
      "notification_emails": "devteam@bangthetable.com",
      "allow_anonymous_participation": false,
      "allow_user_to_post_multiple_times": false,
      "allow_unverified_participation": true,
      "thanks_msg": "string",
      "pinned": true,
      "tag_list": [
        "string"
      ],
      "responses_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 0,
      "randomize_pages": false,
      "randomize_questions": false,
      "randomize_options": false,
      "modified_at": "2020-11-13T10:00:00.000Z",
      "submit_button_text": "string",
      "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
      "show_response_count": false,
      "show_results": true,
      "is_new_survey": true,
      "show_progress_bar": true,
      "file_question_count": 0,
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="publish-project-survey_tool-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Publish Project Survey Tool|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="publish-project-survey_tool-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unpublish-project-survey_tool

<a id="opIdunpublish-project-survey_tool"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/survey_tools/{id}/unpublish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/survey_tools/{id}/unpublish`

*Unpublish Project Survey Tool*

Unpublish Project Survey Tool

<h3 id="unpublish-project-survey_tool-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Survey Tool",
    "attributes": {
      "id": 1,
      "name": "survey 353",
      "description": "<img src=\"something.png\" /> Description",
      "permalink": "survey_tool355-92",
      "state": "draft",
      "image_url": "another_thing.png",
      "archival_reason_message": "archival message",
      "send_acknowledgement": true,
      "send_acknowledgement_to_admin": true,
      "notification_emails": "devteam@bangthetable.com",
      "allow_anonymous_participation": false,
      "allow_user_to_post_multiple_times": false,
      "allow_unverified_participation": true,
      "thanks_msg": "string",
      "pinned": true,
      "tag_list": [
        "string"
      ],
      "responses_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 0,
      "randomize_pages": false,
      "randomize_questions": false,
      "randomize_options": false,
      "modified_at": "2020-11-13T10:00:00.000Z",
      "submit_button_text": "string",
      "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
      "show_response_count": false,
      "show_results": true,
      "is_new_survey": true,
      "show_progress_bar": true,
      "file_question_count": 0,
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unpublish-project-survey_tool-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unpublish Project Survey Tool|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unpublish-project-survey_tool-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## archive-project-survey_tool

<a id="opIdarchive-project-survey_tool"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/survey_tools/{id}/archive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/survey_tools/{id}/archive`

*Archive Project Survey Tool*

Archive Project Survey Tool

> Body parameter

```json
{
  "hide": true
}
```

<h3 id="archive-project-survey_tool-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with archive information|
|» hide|body|boolean|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Survey Tool",
    "attributes": {
      "id": 1,
      "name": "survey 353",
      "description": "<img src=\"something.png\" /> Description",
      "permalink": "survey_tool355-92",
      "state": "draft",
      "image_url": "another_thing.png",
      "archival_reason_message": "archival message",
      "send_acknowledgement": true,
      "send_acknowledgement_to_admin": true,
      "notification_emails": "devteam@bangthetable.com",
      "allow_anonymous_participation": false,
      "allow_user_to_post_multiple_times": false,
      "allow_unverified_participation": true,
      "thanks_msg": "string",
      "pinned": true,
      "tag_list": [
        "string"
      ],
      "responses_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 0,
      "randomize_pages": false,
      "randomize_questions": false,
      "randomize_options": false,
      "modified_at": "2020-11-13T10:00:00.000Z",
      "submit_button_text": "string",
      "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
      "show_response_count": false,
      "show_results": true,
      "is_new_survey": true,
      "show_progress_bar": true,
      "file_question_count": 0,
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="archive-project-survey_tool-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Archive Project Survey Tool|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="archive-project-survey_tool-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unarchive-project-survey_tool

<a id="opIdunarchive-project-survey_tool"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/survey_tools/{id}/unarchive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/survey_tools/{id}/unarchive`

*Unarchive Project Survey Tool*

Unarchive Project Survey Tool

<h3 id="unarchive-project-survey_tool-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Survey Tool",
    "attributes": {
      "id": 1,
      "name": "survey 353",
      "description": "<img src=\"something.png\" /> Description",
      "permalink": "survey_tool355-92",
      "state": "draft",
      "image_url": "another_thing.png",
      "archival_reason_message": "archival message",
      "send_acknowledgement": true,
      "send_acknowledgement_to_admin": true,
      "notification_emails": "devteam@bangthetable.com",
      "allow_anonymous_participation": false,
      "allow_user_to_post_multiple_times": false,
      "allow_unverified_participation": true,
      "thanks_msg": "string",
      "pinned": true,
      "tag_list": [
        "string"
      ],
      "responses_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 0,
      "randomize_pages": false,
      "randomize_questions": false,
      "randomize_options": false,
      "modified_at": "2020-11-13T10:00:00.000Z",
      "submit_button_text": "string",
      "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
      "show_response_count": false,
      "show_results": true,
      "is_new_survey": true,
      "show_progress_bar": true,
      "file_question_count": 0,
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unarchive-project-survey_tool-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unarchive Project Survey Tool|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unarchive-project-survey_tool-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## hide-project-survey_tool

<a id="opIdhide-project-survey_tool"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/survey_tools/{id}/hide',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/survey_tools/{id}/hide`

*Hide Project Survey Tool*

Hide Project Survey Tool

<h3 id="hide-project-survey_tool-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Survey Tool",
    "attributes": {
      "id": 1,
      "name": "survey 353",
      "description": "<img src=\"something.png\" /> Description",
      "permalink": "survey_tool355-92",
      "state": "draft",
      "image_url": "another_thing.png",
      "archival_reason_message": "archival message",
      "send_acknowledgement": true,
      "send_acknowledgement_to_admin": true,
      "notification_emails": "devteam@bangthetable.com",
      "allow_anonymous_participation": false,
      "allow_user_to_post_multiple_times": false,
      "allow_unverified_participation": true,
      "thanks_msg": "string",
      "pinned": true,
      "tag_list": [
        "string"
      ],
      "responses_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 0,
      "randomize_pages": false,
      "randomize_questions": false,
      "randomize_options": false,
      "modified_at": "2020-11-13T10:00:00.000Z",
      "submit_button_text": "string",
      "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
      "show_response_count": false,
      "show_results": true,
      "is_new_survey": true,
      "show_progress_bar": true,
      "file_question_count": 0,
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="hide-project-survey_tool-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hide Project Survey Tool|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="hide-project-survey_tool-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## visible-project-survey_tool

<a id="opIdvisible-project-survey_tool"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/survey_tools/{id}/visible',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/survey_tools/{id}/visible`

*Visible Project Survey Tool*

Visible Project Survey Tool

<h3 id="visible-project-survey_tool-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Survey Tool",
    "attributes": {
      "id": 1,
      "name": "survey 353",
      "description": "<img src=\"something.png\" /> Description",
      "permalink": "survey_tool355-92",
      "state": "draft",
      "image_url": "another_thing.png",
      "archival_reason_message": "archival message",
      "send_acknowledgement": true,
      "send_acknowledgement_to_admin": true,
      "notification_emails": "devteam@bangthetable.com",
      "allow_anonymous_participation": false,
      "allow_user_to_post_multiple_times": false,
      "allow_unverified_participation": true,
      "thanks_msg": "string",
      "pinned": true,
      "tag_list": [
        "string"
      ],
      "responses_count": 10,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "sequence": 0,
      "randomize_pages": false,
      "randomize_questions": false,
      "randomize_options": false,
      "modified_at": "2020-11-13T10:00:00.000Z",
      "submit_button_text": "string",
      "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
      "show_response_count": false,
      "show_results": true,
      "is_new_survey": true,
      "show_progress_bar": true,
      "file_question_count": 0,
      "scheduled_at": "2020-11-13T10:00:00.000Z",
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="visible-project-survey_tool-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Visible Project Survey Tool|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="visible-project-survey_tool-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-forums">Forums</h1>

Forums Management

## get-project-forums

<a id="opIdget-project-forums"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/forums',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/forums`

*Get list of Project Forums*

Get list of Project Forums

<h3 id="get-project-forums-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|page|query|integer|false|none|
|per_page|query|integer|false|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Forum",
      "attributes": {
        "id": 1,
        "name": "sample",
        "description": "sample description",
        "permalink": "permalink_137",
        "state": "published",
        "allow_unverified_participation": false,
        "description_display_mode": "truncated",
        "image_url": "string",
        "archival_reason_message": "string",
        "comments_count": 10,
        "tag_list": [
          "string"
        ],
        "sequence": 0,
        "created_at": "2020-11-13T10:00:00.000Z",
        "updated_at": "2020-11-13T10:00:00.000Z",
        "notifications_emails": "string",
        "send_acknowledgement_to_admins": false,
        "send_acknowledgement": false,
        "author": "user3977",
        "likes_count": 10,
        "has_liked_the_forum": true,
        "forum_liked_id": 1
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-forums-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Project Forums|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-forums-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-project-forum

<a id="opIdcreate-project-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/projects/{project_id}/forums',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /projects/{project_id}/forums`

*Create Project Forum*

Create Project Forum

> Body parameter

```json
{
  "name": "sample",
  "description": "sample description",
  "description_display_mode": "truncated",
  "allow_unverified_participation": false,
  "permalink": "permalink_137",
  "image_url": "string",
  "notifications_emails": "string",
  "archival_reason_message": "string",
  "send_acknowledgement": false,
  "send_acknowledgement_to_admins": false,
  "tag_list": [
    "string"
  ]
}
```

<h3 id="create-project-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|body|body|object|true|A JSON object with forum information|
|» name|body|[Forum/properties/name](#schemaforum/properties/name)|false|none|
|» description|body|[Forum/properties/description](#schemaforum/properties/description)|false|none|
|» description_display_mode|body|[Forum/properties/description_display_mode](#schemaforum/properties/description_display_mode)|false|none|
|» allow_unverified_participation|body|[Forum/properties/allow_unverified_participation](#schemaforum/properties/allow_unverified_participation)|false|none|
|» permalink|body|[Forum/properties/permalink](#schemaforum/properties/permalink)|false|none|
|» image_url|body|[Forum/properties/image_url](#schemaforum/properties/image_url)|false|none|
|» notifications_emails|body|[Forum/properties/notifications_emails](#schemaforum/properties/notifications_emails)|false|none|
|» archival_reason_message|body|[Forum/properties/archival_reason_message](#schemaforum/properties/archival_reason_message)|false|none|
|» send_acknowledgement|body|[Forum/properties/send_acknowledgement](#schemaforum/properties/send_acknowledgement)|false|none|
|» send_acknowledgement_to_admins|body|[Forum/properties/send_acknowledgement_to_admins](#schemaforum/properties/send_acknowledgement_to_admins)|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-project-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Project Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-project-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-forum

<a id="opIdget-project-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/forums/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/forums/{id}`

*Get Project Forum*

Get Project Forum

<h3 id="get-project-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-forum-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-project-forum

<a id="opIdupdate-project-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/projects/{project_id}/forums/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /projects/{project_id}/forums/{id}`

*Update Project Forum*

Update Project Forum

> Body parameter

```json
{
  "name": "sample",
  "description": "sample description",
  "description_display_mode": "truncated",
  "allow_unverified_participation": false,
  "permalink": "permalink_137",
  "sequence": 0,
  "image_url": "string",
  "notifications_emails": "string",
  "archival_reason_message": "string",
  "send_acknowledgement": false,
  "send_acknowledgement_to_admins": false,
  "tag_list": [
    "string"
  ]
}
```

<h3 id="update-project-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with forum information|
|» name|body|[Forum/properties/name](#schemaforum/properties/name)|false|none|
|» description|body|[Forum/properties/description](#schemaforum/properties/description)|false|none|
|» description_display_mode|body|[Forum/properties/description_display_mode](#schemaforum/properties/description_display_mode)|false|none|
|» allow_unverified_participation|body|[Forum/properties/allow_unverified_participation](#schemaforum/properties/allow_unverified_participation)|false|none|
|» permalink|body|[Forum/properties/permalink](#schemaforum/properties/permalink)|false|none|
|» sequence|body|[Forum/properties/sequence](#schemaforum/properties/sequence)|false|none|
|» image_url|body|[Forum/properties/image_url](#schemaforum/properties/image_url)|false|none|
|» notifications_emails|body|[Forum/properties/notifications_emails](#schemaforum/properties/notifications_emails)|false|none|
|» archival_reason_message|body|[Forum/properties/archival_reason_message](#schemaforum/properties/archival_reason_message)|false|none|
|» send_acknowledgement|body|[Forum/properties/send_acknowledgement](#schemaforum/properties/send_acknowledgement)|false|none|
|» send_acknowledgement_to_admins|body|[Forum/properties/send_acknowledgement_to_admins](#schemaforum/properties/send_acknowledgement_to_admins)|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-project-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Project Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-project-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-project-forum

<a id="opIddelete-project-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/projects/{project_id}/forums/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /projects/{project_id}/forums/{id}`

*Delete Project Forum*

Delete Project Forum

<h3 id="delete-project-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-project-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-project-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## publish-project-forum

<a id="opIdpublish-project-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/forums/{id}/publish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/forums/{id}/publish`

*Publish Project Forum*

Publish Project Forum

<h3 id="publish-project-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="publish-project-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Publish Project Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="publish-project-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unpublish-project-forum

<a id="opIdunpublish-project-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/forums/{id}/unpublish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/forums/{id}/unpublish`

*Unpublish Project Forum*

Unpublish Project Forum

<h3 id="unpublish-project-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unpublish-project-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unpublish Project Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unpublish-project-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## archive-project-forum

<a id="opIdarchive-project-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/forums/{id}/archive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/forums/{id}/archive`

*Archive Project Forum*

Archive Project Forum

> Body parameter

```json
{
  "hide": true
}
```

<h3 id="archive-project-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with archive information|
|» hide|body|boolean|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="archive-project-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Archive Project Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="archive-project-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unarchive-project-forum

<a id="opIdunarchive-project-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/forums/{id}/unarchive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/forums/{id}/unarchive`

*Unarchive Project Forum*

Unarchive Project Forum

<h3 id="unarchive-project-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unarchive-project-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unarchive Project Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unarchive-project-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## hide-project-forum

<a id="opIdhide-project-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/forums/{id}/hide',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/forums/{id}/hide`

*Hide Project Forum*

Hide Project Forum

<h3 id="hide-project-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="hide-project-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hide Project Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="hide-project-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## visible-project-forum

<a id="opIdvisible-project-forum"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/forums/{id}/visible',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/forums/{id}/visible`

*Visible Project Forum*

Visible Project Forum

<h3 id="visible-project-forum-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Forum",
    "attributes": {
      "id": 1,
      "name": "sample",
      "description": "sample description",
      "permalink": "permalink_137",
      "state": "published",
      "allow_unverified_participation": false,
      "description_display_mode": "truncated",
      "image_url": "string",
      "archival_reason_message": "string",
      "comments_count": 10,
      "tag_list": [
        "string"
      ],
      "sequence": 0,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "notifications_emails": "string",
      "send_acknowledgement_to_admins": false,
      "send_acknowledgement": false,
      "author": "user3977",
      "likes_count": 10,
      "has_liked_the_forum": true,
      "forum_liked_id": 1
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="visible-project-forum-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Visible Project Forum|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="visible-project-forum-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-forums-email_templates

<a id="opIdget-project-forums-email_templates"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/forums/email_templates',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/forums/email_templates`

*Get list of Project Forums Email Templates*

Get list of Project Forums Email Templates

<h3 id="get-project-forums-email_templates-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Email Template",
    "attributes": {
      "id": 1,
      "subject_template": "Subject Template",
      "body_template": "Body Template",
      "emails": "abc@gmail.com,xya@gmail.com",
      "show_emails": true,
      "identifier": "notify_admin_on_new_forum_topic"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-forums-email_templates-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Project Forums Email Templates|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-forums-email_templates-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-quick-polls">Quick Polls</h1>

Quick Polls Management

## get-project-quick_polls

<a id="opIdget-project-quick_polls"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/quick_polls',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/quick_polls`

*Get list of Quick Polls*

Get list of Quick Polls

<h3 id="get-project-quick_polls-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Quick Poll",
      "attributes": {
        "id": 1,
        "name": "QuickPoll 137",
        "description": "This is a quick poll.",
        "permalink": "quickpoll-137",
        "state": "published",
        "archival_reason_message": "archival message",
        "allow_unverified_participation": true,
        "allow_anonymous_participation": false,
        "results": "string",
        "thanks_msg": "string",
        "image_url": "string",
        "sequence": 1,
        "created_at": "2020-11-13T10:00:00.000Z",
        "updated_at": "2020-11-13T10:00:00.000Z",
        "tag_list": [
          "a",
          "b"
        ],
        "visibility": "inherit"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-quick_polls-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Quick Polls|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-quick_polls-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-project-quick_poll

<a id="opIdcreate-project-quick_poll"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/projects/{project_id}/quick_polls',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /projects/{project_id}/quick_polls`

*Create Project Quick Poll*

Create Project Quick Poll

> Body parameter

```json
{
  "name": "QuickPoll 137",
  "description": "This is a quick poll.",
  "permalink": "quickpoll-137",
  "thanks_msg": "string",
  "image_url": "string",
  "allow_unverified_participation": true,
  "allow_anonymous_participation": false,
  "sequence": 1,
  "archival_reason_message": "archival message",
  "visibility": "inherit",
  "options": "string",
  "tag_list": [
    "a",
    "b"
  ]
}
```

<h3 id="create-project-quick_poll-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|body|body|object|true|A JSON object with quick poll information|
|» name|body|[QuickPoll/properties/name](#schemaquickpoll/properties/name)|false|none|
|» description|body|[QuickPoll/properties/description](#schemaquickpoll/properties/description)|false|none|
|» permalink|body|[QuickPoll/properties/permalink](#schemaquickpoll/properties/permalink)|false|none|
|» thanks_msg|body|[QuickPoll/properties/thanks_msg](#schemaquickpoll/properties/thanks_msg)|false|none|
|» image_url|body|[QuickPoll/properties/image_url](#schemaquickpoll/properties/image_url)|false|none|
|» allow_unverified_participation|body|[QuickPoll/properties/allow_unverified_participation](#schemaquickpoll/properties/allow_unverified_participation)|false|none|
|» allow_anonymous_participation|body|[QuickPoll/properties/allow_anonymous_participation](#schemaquickpoll/properties/allow_anonymous_participation)|false|none|
|» sequence|body|[QuickPoll/properties/sequence](#schemaquickpoll/properties/sequence)|false|none|
|» archival_reason_message|body|[QuickPoll/properties/archival_reason_message](#schemaquickpoll/properties/archival_reason_message)|false|none|
|» visibility|body|[QuickPoll/properties/visibility](#schemaquickpoll/properties/visibility)|false|none|
|» options|body|string|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Quick Poll",
    "attributes": {
      "id": 1,
      "name": "QuickPoll 137",
      "description": "This is a quick poll.",
      "permalink": "quickpoll-137",
      "state": "published",
      "archival_reason_message": "archival message",
      "allow_unverified_participation": true,
      "allow_anonymous_participation": false,
      "results": "string",
      "thanks_msg": "string",
      "image_url": "string",
      "sequence": 1,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-project-quick_poll-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Project Quick Poll|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-project-quick_poll-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-quick_poll

<a id="opIdget-project-quick_poll"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/quick_polls/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/quick_polls/{id}`

*Get Project Quick Poll*

Get Project Quick Poll

<h3 id="get-project-quick_poll-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Quick Poll",
    "attributes": {
      "id": 1,
      "name": "QuickPoll 137",
      "description": "This is a quick poll.",
      "permalink": "quickpoll-137",
      "state": "published",
      "archival_reason_message": "archival message",
      "allow_unverified_participation": true,
      "allow_anonymous_participation": false,
      "results": "string",
      "thanks_msg": "string",
      "image_url": "string",
      "sequence": 1,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-quick_poll-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Quick Poll|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-quick_poll-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-project-quick_poll

<a id="opIdupdate-project-quick_poll"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/projects/{project_id}/quick_polls/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /projects/{project_id}/quick_polls/{id}`

*Update Project Quick Poll*

Update Project Quick Poll

> Body parameter

```json
{
  "name": "QuickPoll 137",
  "description": "This is a quick poll.",
  "permalink": "quickpoll-137",
  "thanks_msg": "string",
  "image_url": "string",
  "allow_unverified_participation": true,
  "allow_anonymous_participation": false,
  "sequence": 1,
  "archival_reason_message": "archival message",
  "visibility": "inherit",
  "options": "string",
  "tag_list": [
    "a",
    "b"
  ]
}
```

<h3 id="update-project-quick_poll-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with quick poll information|
|» name|body|[QuickPoll/properties/name](#schemaquickpoll/properties/name)|false|none|
|» description|body|[QuickPoll/properties/description](#schemaquickpoll/properties/description)|false|none|
|» permalink|body|[QuickPoll/properties/permalink](#schemaquickpoll/properties/permalink)|false|none|
|» thanks_msg|body|[QuickPoll/properties/thanks_msg](#schemaquickpoll/properties/thanks_msg)|false|none|
|» image_url|body|[QuickPoll/properties/image_url](#schemaquickpoll/properties/image_url)|false|none|
|» allow_unverified_participation|body|[QuickPoll/properties/allow_unverified_participation](#schemaquickpoll/properties/allow_unverified_participation)|false|none|
|» allow_anonymous_participation|body|[QuickPoll/properties/allow_anonymous_participation](#schemaquickpoll/properties/allow_anonymous_participation)|false|none|
|» sequence|body|[QuickPoll/properties/sequence](#schemaquickpoll/properties/sequence)|false|none|
|» archival_reason_message|body|[QuickPoll/properties/archival_reason_message](#schemaquickpoll/properties/archival_reason_message)|false|none|
|» visibility|body|[QuickPoll/properties/visibility](#schemaquickpoll/properties/visibility)|false|none|
|» options|body|string|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Quick Poll",
    "attributes": {
      "id": 1,
      "name": "QuickPoll 137",
      "description": "This is a quick poll.",
      "permalink": "quickpoll-137",
      "state": "published",
      "archival_reason_message": "archival message",
      "allow_unverified_participation": true,
      "allow_anonymous_participation": false,
      "results": "string",
      "thanks_msg": "string",
      "image_url": "string",
      "sequence": 1,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-project-quick_poll-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Project Quick Poll|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-project-quick_poll-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-project-quick_poll

<a id="opIddelete-project-quick_poll"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/projects/{project_id}/quick_polls/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /projects/{project_id}/quick_polls/{id}`

*Delete Project Quick Poll*

Delete Project Quick Poll

<h3 id="delete-project-quick_poll-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-project-quick_poll-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-project-quick_poll-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## publish-project-quick_poll

<a id="opIdpublish-project-quick_poll"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/quick_polls/{id}/publish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/quick_polls/{id}/publish`

*Publish Project Quick Poll*

Publish Project Quic Poll

<h3 id="publish-project-quick_poll-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Quick Poll",
    "attributes": {
      "id": 1,
      "name": "QuickPoll 137",
      "description": "This is a quick poll.",
      "permalink": "quickpoll-137",
      "state": "published",
      "archival_reason_message": "archival message",
      "allow_unverified_participation": true,
      "allow_anonymous_participation": false,
      "results": "string",
      "thanks_msg": "string",
      "image_url": "string",
      "sequence": 1,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="publish-project-quick_poll-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Publish Project Quick Poll|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="publish-project-quick_poll-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unpublish-project-quick_poll

<a id="opIdunpublish-project-quick_poll"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/quick_polls/{id}/unpublish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/quick_polls/{id}/unpublish`

*Unpublish Project Quick Poll*

Unpublish Project Quick Poll

<h3 id="unpublish-project-quick_poll-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Quick Poll",
    "attributes": {
      "id": 1,
      "name": "QuickPoll 137",
      "description": "This is a quick poll.",
      "permalink": "quickpoll-137",
      "state": "published",
      "archival_reason_message": "archival message",
      "allow_unverified_participation": true,
      "allow_anonymous_participation": false,
      "results": "string",
      "thanks_msg": "string",
      "image_url": "string",
      "sequence": 1,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unpublish-project-quick_poll-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unpublish Project Quick Poll|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unpublish-project-quick_poll-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## archive-project-quick_poll

<a id="opIdarchive-project-quick_poll"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/quick_polls/{id}/archive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/quick_polls/{id}/archive`

*Archive Project Quick Poll*

Archive Project Quick Poll

> Body parameter

```json
{
  "hide": true
}
```

<h3 id="archive-project-quick_poll-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with archive information|
|» hide|body|boolean|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Quick Poll",
    "attributes": {
      "id": 1,
      "name": "QuickPoll 137",
      "description": "This is a quick poll.",
      "permalink": "quickpoll-137",
      "state": "published",
      "archival_reason_message": "archival message",
      "allow_unverified_participation": true,
      "allow_anonymous_participation": false,
      "results": "string",
      "thanks_msg": "string",
      "image_url": "string",
      "sequence": 1,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="archive-project-quick_poll-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Archive Project Quick Poll|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="archive-project-quick_poll-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unarchive-project-quick_poll

<a id="opIdunarchive-project-quick_poll"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/quick_polls/{id}/unarchive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/quick_polls/{id}/unarchive`

*Unarchive Project Quick Poll*

Unarchive Project Quick Poll

<h3 id="unarchive-project-quick_poll-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Quick Poll",
    "attributes": {
      "id": 1,
      "name": "QuickPoll 137",
      "description": "This is a quick poll.",
      "permalink": "quickpoll-137",
      "state": "published",
      "archival_reason_message": "archival message",
      "allow_unverified_participation": true,
      "allow_anonymous_participation": false,
      "results": "string",
      "thanks_msg": "string",
      "image_url": "string",
      "sequence": 1,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unarchive-project-quick_poll-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unarchive Project Quick Poll|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unarchive-project-quick_poll-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## hide-project-quick_poll

<a id="opIdhide-project-quick_poll"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/quick_polls/{id}/hide',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/quick_polls/{id}/hide`

*Hide Project Quick Poll*

Hide Project Quick Poll

<h3 id="hide-project-quick_poll-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Quick Poll",
    "attributes": {
      "id": 1,
      "name": "QuickPoll 137",
      "description": "This is a quick poll.",
      "permalink": "quickpoll-137",
      "state": "published",
      "archival_reason_message": "archival message",
      "allow_unverified_participation": true,
      "allow_anonymous_participation": false,
      "results": "string",
      "thanks_msg": "string",
      "image_url": "string",
      "sequence": 1,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="hide-project-quick_poll-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hide Project Quick Poll|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="hide-project-quick_poll-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## visible-project-quick_poll

<a id="opIdvisible-project-quick_poll"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/quick_polls/{id}/visible',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/quick_polls/{id}/visible`

*Visible Project Quick Poll*

Visible Project Quick Poll

<h3 id="visible-project-quick_poll-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Quick Poll",
    "attributes": {
      "id": 1,
      "name": "QuickPoll 137",
      "description": "This is a quick poll.",
      "permalink": "quickpoll-137",
      "state": "published",
      "archival_reason_message": "archival message",
      "allow_unverified_participation": true,
      "allow_anonymous_participation": false,
      "results": "string",
      "thanks_msg": "string",
      "image_url": "string",
      "sequence": 1,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "visibility": "inherit"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="visible-project-quick_poll-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Visible Project Quick Poll|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="visible-project-quick_poll-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-maps">Maps</h1>

Maps Management

## get-project-maps

<a id="opIdget-project-maps"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/maps',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/maps`

*Get list of Maps*

Get list of Maps

<h3 id="get-project-maps-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Map",
      "attributes": {
        "id": 1,
        "name": "new sample",
        "description": "new description",
        "permalink": "sample-permalink",
        "state": "draft",
        "image_url": "abc.png",
        "archival_reason_message": "string",
        "lat": 1,
        "lng": 3,
        "polygon": "abcdef",
        "zoom": 1,
        "bounds": "abc",
        "gis_enabled": false,
        "gis_version": "3.0",
        "gis_url": "http://abc.def",
        "gis_layer": "abc",
        "image_visibility": true,
        "show_address": false,
        "allow_unverified_participation": false,
        "optional_comment": false,
        "created_at": "2020-11-13T10:00:00.000Z",
        "updated_at": "2020-11-13T10:00:00.000Z",
        "tag_list": [
          "a",
          "b"
        ],
        "responses_count": 10,
        "style": "string",
        "survey": {},
        "sequence": 1,
        "target_srs": "EPSG:3826",
        "description_display_mode": "string",
        "snapshot_url": "string",
        "mapboxgl_enabled": true,
        "hide_survey_response": false,
        "restrict_marker_creation": false
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-maps-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Maps|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-maps-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-project-map

<a id="opIdcreate-project-map"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/projects/{project_id}/maps',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /projects/{project_id}/maps`

*Create Project Map*

Create Project Map

> Body parameter

```json
{
  "name": "new sample",
  "description": "new description",
  "permalink": "sample-permalink",
  "zoom": 1,
  "bounds": "abc",
  "polygon": "abcdef",
  "lat": 1,
  "lng": 3,
  "style": "string",
  "gis_enabled": false,
  "gis_layer": "abc",
  "gis_version": "3.0",
  "gis_url": "http://abc.def",
  "image_visibility": true,
  "show_address": false,
  "allow_unverified_participation": false,
  "optional_comment": false,
  "image_url": "abc.png",
  "sequence": 1,
  "target_srs": "EPSG:3826",
  "archival_reason_message": "string",
  "restrict_marker_creation": false,
  "hide_survey_response": false,
  "description_display_mode": "string",
  "snapshot_url": "string",
  "tag_list": [
    "a",
    "b"
  ]
}
```

<h3 id="create-project-map-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|body|body|object|true|A JSON object with map information|
|» name|body|[Map/properties/name](#schemamap/properties/name)|false|none|
|» description|body|[Map/properties/description](#schemamap/properties/description)|false|none|
|» permalink|body|[Map/properties/permalink](#schemamap/properties/permalink)|false|none|
|» zoom|body|[Map/properties/zoom](#schemamap/properties/zoom)|false|none|
|» bounds|body|[Map/properties/bounds](#schemamap/properties/bounds)|false|none|
|» polygon|body|[Map/properties/polygon](#schemamap/properties/polygon)|false|none|
|» lat|body|[Map/properties/lat](#schemamap/properties/lat)(float)|false|latitude of the map|
|» lng|body|[Map/properties/lng](#schemamap/properties/lng)(float)|false|longitude of the map|
|» style|body|[Map/properties/style](#schemamap/properties/style)|false|none|
|» gis_enabled|body|[Map/properties/gis_enabled](#schemamap/properties/gis_enabled)|false|none|
|» gis_layer|body|[Map/properties/gis_layer](#schemamap/properties/gis_layer)|false|none|
|» gis_version|body|[Map/properties/gis_version](#schemamap/properties/gis_version)|false|none|
|» gis_url|body|[Map/properties/gis_url](#schemamap/properties/gis_url)|false|none|
|» image_visibility|body|[Map/properties/image_visibility](#schemamap/properties/image_visibility)|false|none|
|» show_address|body|[Map/properties/show_address](#schemamap/properties/show_address)|false|none|
|» allow_unverified_participation|body|[Map/properties/allow_unverified_participation](#schemamap/properties/allow_unverified_participation)|false|none|
|» optional_comment|body|[Map/properties/optional_comment](#schemamap/properties/optional_comment)|false|none|
|» image_url|body|[Map/properties/image_url](#schemamap/properties/image_url)|false|none|
|» sequence|body|[Map/properties/sequence](#schemamap/properties/sequence)|false|none|
|» target_srs|body|[Map/properties/target_srs](#schemamap/properties/target_srs)|false|none|
|» archival_reason_message|body|[Map/properties/archival_reason_message](#schemamap/properties/archival_reason_message)|false|none|
|» restrict_marker_creation|body|[Map/properties/restrict_marker_creation](#schemamap/properties/restrict_marker_creation)|false|none|
|» hide_survey_response|body|[Map/properties/hide_survey_response](#schemamap/properties/hide_survey_response)|false|none|
|» description_display_mode|body|[Map/properties/description_display_mode](#schemamap/properties/description_display_mode)|false|none|
|» snapshot_url|body|[Map/properties/snapshot_url](#schemamap/properties/snapshot_url)|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Map",
    "attributes": {
      "id": 1,
      "name": "new sample",
      "description": "new description",
      "permalink": "sample-permalink",
      "state": "draft",
      "image_url": "abc.png",
      "archival_reason_message": "string",
      "lat": 1,
      "lng": 3,
      "polygon": "abcdef",
      "zoom": 1,
      "bounds": "abc",
      "gis_enabled": false,
      "gis_version": "3.0",
      "gis_url": "http://abc.def",
      "gis_layer": "abc",
      "image_visibility": true,
      "show_address": false,
      "allow_unverified_participation": false,
      "optional_comment": false,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "responses_count": 10,
      "style": "string",
      "survey": {},
      "sequence": 1,
      "target_srs": "EPSG:3826",
      "description_display_mode": "string",
      "snapshot_url": "string",
      "mapboxgl_enabled": true,
      "hide_survey_response": false,
      "restrict_marker_creation": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-project-map-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Project Map|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-project-map-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-project-map

<a id="opIdget-project-map"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/projects/{project_id}/maps/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /projects/{project_id}/maps/{id}`

*Get Project Maps*

Get Project Maps

<h3 id="get-project-map-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Map",
    "attributes": {
      "id": 1,
      "name": "new sample",
      "description": "new description",
      "permalink": "sample-permalink",
      "state": "draft",
      "image_url": "abc.png",
      "archival_reason_message": "string",
      "lat": 1,
      "lng": 3,
      "polygon": "abcdef",
      "zoom": 1,
      "bounds": "abc",
      "gis_enabled": false,
      "gis_version": "3.0",
      "gis_url": "http://abc.def",
      "gis_layer": "abc",
      "image_visibility": true,
      "show_address": false,
      "allow_unverified_participation": false,
      "optional_comment": false,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "responses_count": 10,
      "style": "string",
      "survey": {},
      "sequence": 1,
      "target_srs": "EPSG:3826",
      "description_display_mode": "string",
      "snapshot_url": "string",
      "mapboxgl_enabled": true,
      "hide_survey_response": false,
      "restrict_marker_creation": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-project-map-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Project Maps|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-project-map-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-project-map

<a id="opIdupdate-project-map"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/projects/{project_id}/maps/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /projects/{project_id}/maps/{id}`

*Update Project Map*

Update Project Map

> Body parameter

```json
{
  "name": "new sample",
  "description": "new description",
  "permalink": "sample-permalink",
  "zoom": 1,
  "bounds": "abc",
  "polygon": "abcdef",
  "lat": 1,
  "lng": 3,
  "style": "string",
  "gis_enabled": false,
  "gis_layer": "abc",
  "gis_version": "3.0",
  "gis_url": "http://abc.def",
  "image_visibility": true,
  "show_address": false,
  "allow_unverified_participation": false,
  "optional_comment": false,
  "image_url": "abc.png",
  "sequence": 1,
  "target_srs": "EPSG:3826",
  "archival_reason_message": "string",
  "restrict_marker_creation": false,
  "hide_survey_response": false,
  "description_display_mode": "string",
  "snapshot_url": "string",
  "tag_list": [
    "a",
    "b"
  ]
}
```

<h3 id="update-project-map-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with map information|
|» name|body|[Map/properties/name](#schemamap/properties/name)|false|none|
|» description|body|[Map/properties/description](#schemamap/properties/description)|false|none|
|» permalink|body|[Map/properties/permalink](#schemamap/properties/permalink)|false|none|
|» zoom|body|[Map/properties/zoom](#schemamap/properties/zoom)|false|none|
|» bounds|body|[Map/properties/bounds](#schemamap/properties/bounds)|false|none|
|» polygon|body|[Map/properties/polygon](#schemamap/properties/polygon)|false|none|
|» lat|body|[Map/properties/lat](#schemamap/properties/lat)(float)|false|latitude of the map|
|» lng|body|[Map/properties/lng](#schemamap/properties/lng)(float)|false|longitude of the map|
|» style|body|[Map/properties/style](#schemamap/properties/style)|false|none|
|» gis_enabled|body|[Map/properties/gis_enabled](#schemamap/properties/gis_enabled)|false|none|
|» gis_layer|body|[Map/properties/gis_layer](#schemamap/properties/gis_layer)|false|none|
|» gis_version|body|[Map/properties/gis_version](#schemamap/properties/gis_version)|false|none|
|» gis_url|body|[Map/properties/gis_url](#schemamap/properties/gis_url)|false|none|
|» image_visibility|body|[Map/properties/image_visibility](#schemamap/properties/image_visibility)|false|none|
|» show_address|body|[Map/properties/show_address](#schemamap/properties/show_address)|false|none|
|» allow_unverified_participation|body|[Map/properties/allow_unverified_participation](#schemamap/properties/allow_unverified_participation)|false|none|
|» optional_comment|body|[Map/properties/optional_comment](#schemamap/properties/optional_comment)|false|none|
|» image_url|body|[Map/properties/image_url](#schemamap/properties/image_url)|false|none|
|» sequence|body|[Map/properties/sequence](#schemamap/properties/sequence)|false|none|
|» target_srs|body|[Map/properties/target_srs](#schemamap/properties/target_srs)|false|none|
|» archival_reason_message|body|[Map/properties/archival_reason_message](#schemamap/properties/archival_reason_message)|false|none|
|» restrict_marker_creation|body|[Map/properties/restrict_marker_creation](#schemamap/properties/restrict_marker_creation)|false|none|
|» hide_survey_response|body|[Map/properties/hide_survey_response](#schemamap/properties/hide_survey_response)|false|none|
|» description_display_mode|body|[Map/properties/description_display_mode](#schemamap/properties/description_display_mode)|false|none|
|» snapshot_url|body|[Map/properties/snapshot_url](#schemamap/properties/snapshot_url)|false|none|
|» tag_list|body|[string]|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Map",
    "attributes": {
      "id": 1,
      "name": "new sample",
      "description": "new description",
      "permalink": "sample-permalink",
      "state": "draft",
      "image_url": "abc.png",
      "archival_reason_message": "string",
      "lat": 1,
      "lng": 3,
      "polygon": "abcdef",
      "zoom": 1,
      "bounds": "abc",
      "gis_enabled": false,
      "gis_version": "3.0",
      "gis_url": "http://abc.def",
      "gis_layer": "abc",
      "image_visibility": true,
      "show_address": false,
      "allow_unverified_participation": false,
      "optional_comment": false,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "responses_count": 10,
      "style": "string",
      "survey": {},
      "sequence": 1,
      "target_srs": "EPSG:3826",
      "description_display_mode": "string",
      "snapshot_url": "string",
      "mapboxgl_enabled": true,
      "hide_survey_response": false,
      "restrict_marker_creation": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-project-map-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Project Map|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-project-map-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-project-map

<a id="opIddelete-project-map"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/projects/{project_id}/maps/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /projects/{project_id}/maps/{id}`

*Delete Project Map*

Delete Project Map

<h3 id="delete-project-map-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-project-map-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-project-map-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## publish-project-map

<a id="opIdpublish-project-map"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/maps/{id}/publish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/maps/{id}/publish`

*Publish Project Map*

Publish Project Map

<h3 id="publish-project-map-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Map",
    "attributes": {
      "id": 1,
      "name": "new sample",
      "description": "new description",
      "permalink": "sample-permalink",
      "state": "draft",
      "image_url": "abc.png",
      "archival_reason_message": "string",
      "lat": 1,
      "lng": 3,
      "polygon": "abcdef",
      "zoom": 1,
      "bounds": "abc",
      "gis_enabled": false,
      "gis_version": "3.0",
      "gis_url": "http://abc.def",
      "gis_layer": "abc",
      "image_visibility": true,
      "show_address": false,
      "allow_unverified_participation": false,
      "optional_comment": false,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "responses_count": 10,
      "style": "string",
      "survey": {},
      "sequence": 1,
      "target_srs": "EPSG:3826",
      "description_display_mode": "string",
      "snapshot_url": "string",
      "mapboxgl_enabled": true,
      "hide_survey_response": false,
      "restrict_marker_creation": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="publish-project-map-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Publish Project Map|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="publish-project-map-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unpublish-project-map

<a id="opIdunpublish-project-map"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/maps/{id}/unpublish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/maps/{id}/unpublish`

*Unpublish Project Map*

Unpublish Project Map

<h3 id="unpublish-project-map-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Map",
    "attributes": {
      "id": 1,
      "name": "new sample",
      "description": "new description",
      "permalink": "sample-permalink",
      "state": "draft",
      "image_url": "abc.png",
      "archival_reason_message": "string",
      "lat": 1,
      "lng": 3,
      "polygon": "abcdef",
      "zoom": 1,
      "bounds": "abc",
      "gis_enabled": false,
      "gis_version": "3.0",
      "gis_url": "http://abc.def",
      "gis_layer": "abc",
      "image_visibility": true,
      "show_address": false,
      "allow_unverified_participation": false,
      "optional_comment": false,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "responses_count": 10,
      "style": "string",
      "survey": {},
      "sequence": 1,
      "target_srs": "EPSG:3826",
      "description_display_mode": "string",
      "snapshot_url": "string",
      "mapboxgl_enabled": true,
      "hide_survey_response": false,
      "restrict_marker_creation": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unpublish-project-map-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unpublish Project Map|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unpublish-project-map-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## archive-project-map

<a id="opIdarchive-project-map"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/maps/{id}/archive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/maps/{id}/archive`

*Archive Project Map*

Archive Project Map

> Body parameter

```json
{
  "hide": true
}
```

<h3 id="archive-project-map-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with archive information|
|» hide|body|boolean|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Map",
    "attributes": {
      "id": 1,
      "name": "new sample",
      "description": "new description",
      "permalink": "sample-permalink",
      "state": "draft",
      "image_url": "abc.png",
      "archival_reason_message": "string",
      "lat": 1,
      "lng": 3,
      "polygon": "abcdef",
      "zoom": 1,
      "bounds": "abc",
      "gis_enabled": false,
      "gis_version": "3.0",
      "gis_url": "http://abc.def",
      "gis_layer": "abc",
      "image_visibility": true,
      "show_address": false,
      "allow_unverified_participation": false,
      "optional_comment": false,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "responses_count": 10,
      "style": "string",
      "survey": {},
      "sequence": 1,
      "target_srs": "EPSG:3826",
      "description_display_mode": "string",
      "snapshot_url": "string",
      "mapboxgl_enabled": true,
      "hide_survey_response": false,
      "restrict_marker_creation": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="archive-project-map-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Archive Project Map|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="archive-project-map-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## unarchive-project-map

<a id="opIdunarchive-project-map"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/maps/{id}/unarchive',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/maps/{id}/unarchive`

*Unarchive Project Map*

Unarchive Project Map

<h3 id="unarchive-project-map-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Map",
    "attributes": {
      "id": 1,
      "name": "new sample",
      "description": "new description",
      "permalink": "sample-permalink",
      "state": "draft",
      "image_url": "abc.png",
      "archival_reason_message": "string",
      "lat": 1,
      "lng": 3,
      "polygon": "abcdef",
      "zoom": 1,
      "bounds": "abc",
      "gis_enabled": false,
      "gis_version": "3.0",
      "gis_url": "http://abc.def",
      "gis_layer": "abc",
      "image_visibility": true,
      "show_address": false,
      "allow_unverified_participation": false,
      "optional_comment": false,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "responses_count": 10,
      "style": "string",
      "survey": {},
      "sequence": 1,
      "target_srs": "EPSG:3826",
      "description_display_mode": "string",
      "snapshot_url": "string",
      "mapboxgl_enabled": true,
      "hide_survey_response": false,
      "restrict_marker_creation": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="unarchive-project-map-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Unarchive Project Map|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="unarchive-project-map-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## hide-project-map

<a id="opIdhide-project-map"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/maps/{id}/hide',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/maps/{id}/hide`

*Hide Project Map*

Hide Project Map

<h3 id="hide-project-map-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Map",
    "attributes": {
      "id": 1,
      "name": "new sample",
      "description": "new description",
      "permalink": "sample-permalink",
      "state": "draft",
      "image_url": "abc.png",
      "archival_reason_message": "string",
      "lat": 1,
      "lng": 3,
      "polygon": "abcdef",
      "zoom": 1,
      "bounds": "abc",
      "gis_enabled": false,
      "gis_version": "3.0",
      "gis_url": "http://abc.def",
      "gis_layer": "abc",
      "image_visibility": true,
      "show_address": false,
      "allow_unverified_participation": false,
      "optional_comment": false,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "responses_count": 10,
      "style": "string",
      "survey": {},
      "sequence": 1,
      "target_srs": "EPSG:3826",
      "description_display_mode": "string",
      "snapshot_url": "string",
      "mapboxgl_enabled": true,
      "hide_survey_response": false,
      "restrict_marker_creation": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="hide-project-map-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Hide Project Map|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="hide-project-map-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## visible-project-map

<a id="opIdvisible-project-map"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/projects/{project_id}/maps/{id}/visible',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /projects/{project_id}/maps/{id}/visible`

*Visible Project Map*

Visible Project Map

<h3 id="visible-project-map-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Project ID|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Map",
    "attributes": {
      "id": 1,
      "name": "new sample",
      "description": "new description",
      "permalink": "sample-permalink",
      "state": "draft",
      "image_url": "abc.png",
      "archival_reason_message": "string",
      "lat": 1,
      "lng": 3,
      "polygon": "abcdef",
      "zoom": 1,
      "bounds": "abc",
      "gis_enabled": false,
      "gis_version": "3.0",
      "gis_url": "http://abc.def",
      "gis_layer": "abc",
      "image_visibility": true,
      "show_address": false,
      "allow_unverified_participation": false,
      "optional_comment": false,
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "tag_list": [
        "a",
        "b"
      ],
      "responses_count": 10,
      "style": "string",
      "survey": {},
      "sequence": 1,
      "target_srs": "EPSG:3826",
      "description_display_mode": "string",
      "snapshot_url": "string",
      "mapboxgl_enabled": true,
      "hide_survey_response": false,
      "restrict_marker_creation": false
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="visible-project-map-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Visible Project Map|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="visible-project-map-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

<h1 id="bang-the-table-newsletters">Newsletters</h1>

Newsletters Management

## get-newsletters

<a id="opIdget-newsletters"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/newsletters',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /newsletters`

*Get list of Newsletters*

Get list of Newsletters

<h3 id="get-newsletters-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer|false|none|
|per_page|query|integer|false|none|
|filters|query|object|false|none|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "id": 1,
      "type": "Newsletter",
      "attributes": {
        "id": 1,
        "subject": "New Newsletter",
        "state": "preview",
        "banner_source": "3224",
        "banner_source_url": "new/new_test_image.png",
        "show_logo": true,
        "sent_at": "2020-11-13T10:00:00.000Z",
        "created_at": "2020-11-13T10:00:00.000Z",
        "updated_at": "2020-11-13T10:00:00.000Z",
        "published": false,
        "recipient_count": 10,
        "body": "<p>This is ze Tesla Newsletter.</p>"
      }
    }
  ]
}
```

> 400 Response

```
"string"
```

<h3 id="get-newsletters-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Newsletters|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-newsletters-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## create-newsletter

<a id="opIdcreate-newsletter"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.post 'https://dev.ehq.test/api/v2/newsletters',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /newsletters`

*Create Newsletter*

Create Newsletter

> Body parameter

```json
{
  "state": "preview",
  "subject": "New Newsletter",
  "show_logo": true,
  "banner_source": "3224",
  "body": "<p>This is ze Tesla Newsletter.</p>"
}
```

<h3 id="create-newsletter-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|A JSON object with newsletter information|
|» state|body|[Newsletter/properties/state](#schemanewsletter/properties/state)|false|none|
|» subject|body|[Newsletter/properties/subject](#schemanewsletter/properties/subject)|false|none|
|» show_logo|body|[Newsletter/properties/show_logo](#schemanewsletter/properties/show_logo)|false|none|
|» banner_source|body|[Newsletter/properties/banner_source](#schemanewsletter/properties/banner_source)|false|none|
|» body|body|[Newsletter/properties/body](#schemanewsletter/properties/body)|false|none|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 1,
    "type": "Newsletter",
    "attributes": {
      "id": 1,
      "subject": "New Newsletter",
      "state": "preview",
      "banner_source": "3224",
      "banner_source_url": "new/new_test_image.png",
      "show_logo": true,
      "sent_at": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "published": false,
      "recipient_count": 10,
      "body": "<p>This is ze Tesla Newsletter.</p>"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="create-newsletter-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created Newsletter|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="create-newsletter-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## get-newsletter

<a id="opIdget-newsletter"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.get 'https://dev.ehq.test/api/v2/newsletters/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /newsletters/{id}`

*Get Newsletter*

Get Newsletter

<h3 id="get-newsletter-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Newsletter",
    "attributes": {
      "id": 1,
      "subject": "New Newsletter",
      "state": "preview",
      "banner_source": "3224",
      "banner_source_url": "new/new_test_image.png",
      "show_logo": true,
      "sent_at": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "published": false,
      "recipient_count": 10,
      "body": "<p>This is ze Tesla Newsletter.</p>"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="get-newsletter-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Newsletter|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|

<h3 id="get-newsletter-responseschema">Response Schema</h3>

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## update-newsletter

<a id="opIdupdate-newsletter"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.put 'https://dev.ehq.test/api/v2/newsletters/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /newsletters/{id}`

*Update Newsletter*

Update Newsletter

> Body parameter

```json
{
  "state": "preview",
  "subject": "New Newsletter",
  "show_logo": true,
  "banner_source": "3224",
  "body": "<p>This is ze Tesla Newsletter.</p>"
}
```

<h3 id="update-newsletter-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|
|body|body|object|true|A JSON object with newsletter information|
|» state|body|[Newsletter/properties/state](#schemanewsletter/properties/state)|false|none|
|» subject|body|[Newsletter/properties/subject](#schemanewsletter/properties/subject)|false|none|
|» show_logo|body|[Newsletter/properties/show_logo](#schemanewsletter/properties/show_logo)|false|none|
|» banner_source|body|[Newsletter/properties/banner_source](#schemanewsletter/properties/banner_source)|false|none|
|» body|body|[Newsletter/properties/body](#schemanewsletter/properties/body)|false|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Newsletter",
    "attributes": {
      "id": 1,
      "subject": "New Newsletter",
      "state": "preview",
      "banner_source": "3224",
      "banner_source_url": "new/new_test_image.png",
      "show_logo": true,
      "sent_at": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "published": false,
      "recipient_count": 10,
      "body": "<p>This is ze Tesla Newsletter.</p>"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="update-newsletter-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Updated Newsletter|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="update-newsletter-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## delete-newsletter

<a id="opIddelete-newsletter"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'text/html',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.delete 'https://dev.ehq.test/api/v2/newsletters/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`DELETE /newsletters/{id}`

*Delete Newsletter*

Delete Newsletter

<h3 id="delete-newsletter-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 400 Response

```
"string"
```

> 422 Response

```json
{
  "errors": [
    {
      "source": {
        "pointer": "/data/attributes/name",
        "parameter": "string"
      },
      "code": "blank",
      "meta": {}
    }
  ]
}
```

<h3 id="delete-newsletter-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|The record was deleted successfully|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="delete-newsletter-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## publish-newsletter

<a id="opIdpublish-newsletter"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'X-API-Token' => 'API_KEY'
}

result = RestClient.patch 'https://dev.ehq.test/api/v2/newsletters/{id}/publish',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /newsletters/{id}/publish`

*Publish Newsletter*

Publish Newsletter

<h3 id="publish-newsletter-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Record ID|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 1,
    "type": "Newsletter",
    "attributes": {
      "id": 1,
      "subject": "New Newsletter",
      "state": "preview",
      "banner_source": "3224",
      "banner_source_url": "new/new_test_image.png",
      "show_logo": true,
      "sent_at": "2020-11-13T10:00:00.000Z",
      "created_at": "2020-11-13T10:00:00.000Z",
      "updated_at": "2020-11-13T10:00:00.000Z",
      "published": false,
      "recipient_count": 10,
      "body": "<p>This is ze Tesla Newsletter.</p>"
    }
  }
}
```

> 400 Response

```
"string"
```

<h3 id="publish-newsletter-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Publish Project Newsletter|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Something is wrong with the parameters or the request itself|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Returns bad request when invalid token is passed|string|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Record not found|string|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|The server could not process the entity due to some reason.|Inline|

<h3 id="publish-newsletter-responseschema">Response Schema</h3>

Status Code **422**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» errors|[object]|false|none|none|
|»» source|object|false|none|none|
|»»» pointer|string|false|none|none|
|»»» parameter|string|false|none|none|
|»» code|string|false|none|none|
|»» meta|object|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

# Schemas

<h2 id="tocS_Single">Single</h2>
<!-- backwards compatibility -->
<a id="schemasingle"></a>
<a id="schema_Single"></a>
<a id="tocSsingle"></a>
<a id="tocssingle"></a>

```json
{
  "data": {
    "id": 1,
    "type": "Model Name",
    "attributes": {}
  }
}

```

Single

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|object|false|none|Model entity.|
|» id|string|false|none|none|
|» type|string|false|none|none|
|» attributes|object|false|none|none|

<h2 id="tocS_List">List</h2>
<!-- backwards compatibility -->
<a id="schemalist"></a>
<a id="schema_List"></a>
<a id="tocSlist"></a>
<a id="tocslist"></a>

```json
{
  "data": [
    {
      "id": 1,
      "type": "Model Name",
      "attributes": {}
    }
  ]
}

```

List

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[object]|false|none|An array of model entities.|
|» id|string|false|none|none|
|» type|string|false|none|none|
|» attributes|object|false|none|none|

<h2 id="tocS_Permalink">Permalink</h2>
<!-- backwards compatibility -->
<a id="schemapermalink"></a>
<a id="schema_Permalink"></a>
<a id="tocSpermalink"></a>
<a id="tocspermalink"></a>

```json
{
  "data": {
    "type": "Permalink",
    "attributes": {
      "permalink": "sample"
    }
  }
}

```

Permalink

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|object|false|none|none|
|» type|string|false|none|none|
|» attributes|object|false|none|none|
|»» permalink|string|false|none|none|

<h2 id="tocS_Site">Site</h2>
<!-- backwards compatibility -->
<a id="schemasite"></a>
<a id="schema_Site"></a>
<a id="tocSsite"></a>
<a id="tocssite"></a>

```json
{
  "id": 1,
  "name": "Mark Jaundoo",
  "blocked": false,
  "block_username": "Mark Jaundoo",
  "block_password": 123123,
  "moderated": true,
  "client_id": 1,
  "email_sender_name": "Mark Jaundoo",
  "email_address": "mark@example.com",
  "demo": false,
  "logo_url": "string",
  "locale": "en",
  "licence_type": "plus",
  "theme_name": "bondi",
  "timezone": "Sydney",
  "banner_url": "string",
  "favicon_url": "string",
  "background_image_url": "string",
  "display_site_banner": false,
  "display_project_banner": false
}

```

Review Request

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|true|none|Id of the site|
|name|string|true|none|Name of the person to send review request|
|blocked|boolean|false|none|Set true for block this site|
|block_username|string|false|none|none|
|block_password|string|false|none|none|
|moderated|boolean|false|none|none|
|client_id|integer|false|none|none|
|email_sender_name|string|false|none|none|
|email_address|string|false|none|none|
|demo|boolean|false|none|none|
|logo_url|string|false|none|none|
|locale|string|false|none|none|
|licence_type|string|false|none|none|
|theme_name|string|false|none|none|
|timezone|string|false|none|none|
|banner_url|string|false|none|none|
|favicon_url|string|false|none|none|
|background_image_url|string|false|none|none|
|display_site_banner|boolean|false|none|none|
|display_project_banner|boolean|false|none|none|

<h2 id="tocS_User">User</h2>
<!-- backwards compatibility -->
<a id="schemauser"></a>
<a id="schema_User"></a>
<a id="tocSuser"></a>
<a id="tocsuser"></a>

```json
{
  "id": 1,
  "login": "user5040",
  "email": "user6145@example.com",
  "created_at": "2020-11-13T10:00:00.000Z",
  "last_seen_at": "2020-11-13T10:00:00.000Z",
  "role_name": "participant",
  "blocked": false,
  "unconfirmed": false,
  "role_before_blocking": "role_name",
  "accessible_projects_count": false,
  "accessible_hubs_count": false,
  "accessible_projects_ids": [
    1,
    2
  ],
  "image_url": "string",
  "confirmed": false,
  "subscribed": true,
  "type": "string",
  "unconfirmed_email": "string",
  "login_count": 2
}

```

User

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the user|
|login|string|false|none|Login of the user|
|email|string(email)|false|none|Email of the user (UNIQUE)|
|created_at|string(date-time)|false|none|Date/Time of record created|
|last_seen_at|string(date-time)|false|none|Date/Time of user last seen at|
|role_name|string|false|none|role_name assign to the user|
|blocked|boolean|false|none|User is block or not|
|unconfirmed|boolean|false|none|User is unconfirmed or not|
|role_before_blocking|string|false|none|role_name assign to the user|
|accessible_projects_count|boolean|false|none|Accessible Projects number of count that user can access|
|accessible_hubs_count|boolean|false|none|Accessible Hubs number of count that user can access|
|accessible_projects_ids|[integer]|false|none|Accessible Project ids for user|
|image_url|string|false|none|none|
|confirmed|boolean|false|none|User is confirmed or not|
|subscribed|boolean|false|none|none|
|type|string|false|none|none|
|unconfirmed_email|string|false|none|none|
|login_count|integer|false|none|none|

<h2 id="tocS_BlogPost">BlogPost</h2>
<!-- backwards compatibility -->
<a id="schemablogpost"></a>
<a id="schema_BlogPost"></a>
<a id="tocSblogpost"></a>
<a id="tocsblogpost"></a>

```json
{
  "id": 1,
  "name": "new topic",
  "description": "discuss",
  "permalink": "ft",
  "state": "published",
  "allow_unverified_participation": true,
  "description_display_mode": "string",
  "image_url": "example.com/image.png",
  "tag_list": [
    "a",
    "b",
    "c"
  ],
  "commentable": false,
  "archival_reason_message": "archival message",
  "sequence": 0,
  "comments_count": 0,
  "show_date": true,
  "custom_date": "2020-11-13T10:00:00.000Z",
  "created_at": "2020-11-13T10:00:00.000Z",
  "updated_at": "2020-11-13T10:00:00.000Z",
  "link": "http://something.abc.com",
  "scheduled_at": "2020-11-13T10:00:00.000Z"
}

```

Blog Post

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the blog post|
|name|string|false|none|none|
|description|string|false|none|none|
|permalink|string|false|none|none|
|state|string|false|none|none|
|allow_unverified_participation|boolean|false|none|none|
|description_display_mode|string|false|none|none|
|image_url|string|false|none|none|
|tag_list|[string]|false|none|none|
|commentable|boolean|false|none|none|
|archival_reason_message|string|false|none|none|
|sequence|integer|false|none|none|
|comments_count|integer|false|none|none|
|show_date|boolean|false|none|none|
|custom_date|string(date-time)|false|none|none|
|created_at|string(date-time)|false|none|Date/Time of record created_at|
|updated_at|string(date-time)|false|none|Date/Time of record updated_at|
|link|string|false|none|none|
|scheduled_at|string(date-time)|false|none|Date/Time of record schedule|

<h2 id="tocS_Schedule">Schedule</h2>
<!-- backwards compatibility -->
<a id="schemaschedule"></a>
<a id="schema_Schedule"></a>
<a id="tocSschedule"></a>
<a id="tocsschedule"></a>

```json
{
  "id": 1,
  "action": "hide",
  "owner_id": 1,
  "owner_type": "BlogPost",
  "scheduled_at": "2020-11-13T10:00:00.000Z",
  "user_id": 1
}

```

Schedule

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the blog post|
|action|string|false|none|none|
|owner_id|integer|false|none|none|
|owner_type|string|false|none|none|
|scheduled_at|string(date-time)|false|none|Date/Time of record schedule|
|user_id|integer|false|none|none|

<h2 id="tocS_Comment">Comment</h2>
<!-- backwards compatibility -->
<a id="schemacomment"></a>
<a id="schema_Comment"></a>
<a id="tocScomment"></a>
<a id="tocscomment"></a>

```json
{
  "id": 2,
  "parent_id": 1,
  "comment": "testing comment",
  "image_url": "string",
  "author": "user5179",
  "created_at": "2020-11-13T10:00:00.000Z",
  "reply_count": 10,
  "email": "abc@example.com",
  "up_votes_count": 10,
  "down_votes_count": 10,
  "has_down_voted": false,
  "has_down_voted_id": 1,
  "has_up_voted": false,
  "has_up_voted_id": 1,
  "narrative_name": "testing"
}

```

Comment

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the comment|
|parent_id|integer|false|none|none|
|comment|string|false|none|none|
|image_url|string|false|none|none|
|author|string|false|none|none|
|created_at|string(date-time)|false|none|Date/Time of record created|
|reply_count|integer|false|none|none|
|email|string|false|none|none|
|up_votes_count|integer|false|none|none|
|down_votes_count|integer|false|none|none|
|has_down_voted|boolean|false|none|none|
|has_down_voted_id|integer|false|none|none|
|has_up_voted|boolean|false|none|none|
|has_up_voted_id|integer|false|none|none|
|narrative_name|string|false|none|none|

<h2 id="tocS_Client">Client</h2>
<!-- backwards compatibility -->
<a id="schemaclient"></a>
<a id="schema_Client"></a>
<a id="tocSclient"></a>
<a id="tocsclient"></a>

```json
{
  "id": 2,
  "name": "Test client"
}

```

Client

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the client|
|name|string|false|none|none|

<h2 id="tocS_MentionSuggestion">MentionSuggestion</h2>
<!-- backwards compatibility -->
<a id="schemamentionsuggestion"></a>
<a id="schema_MentionSuggestion"></a>
<a id="tocSmentionsuggestion"></a>
<a id="tocsmentionsuggestion"></a>

```json
{
  "id": 2,
  "login": "string",
  "type": "string",
  "created_at": "2020-11-13T10:00:00.000Z",
  "last_seen_at": "1 day ago"
}

```

MentionSuggestion

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the mention suggestion|
|login|string|false|none|none|
|type|string|false|none|none|
|created_at|string(date-time)|false|none|Date/Time of record created|
|last_seen_at|string|false|none|none|

<h2 id="tocS_Dashboard">Dashboard</h2>
<!-- backwards compatibility -->
<a id="schemadashboard"></a>
<a id="schema_Dashboard"></a>
<a id="tocSdashboard"></a>
<a id="tocsdashboard"></a>

```json
{
  "id": 1,
  "title": "Nice Dashboard",
  "embed_link": "<iframe>ABCDE</iframe>",
  "description": "Very Nice Dashboard, Please Use",
  "sequence": 1
}

```

Dashboard

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the dashboard|
|title|string|false|none|none|
|embed_link|string|false|none|none|
|description|string|false|none|none|
|sequence|integer|false|none|none|

<h2 id="tocS_GuestBook">GuestBook</h2>
<!-- backwards compatibility -->
<a id="schemaguestbook"></a>
<a id="schema_GuestBook"></a>
<a id="tocSguestbook"></a>
<a id="tocsguestbook"></a>

```json
{
  "id": 1,
  "name": "Guest book",
  "permalink": "guest-book",
  "intro_msg": "string",
  "thank_you_message": "string",
  "moderated": false,
  "premoderated": true,
  "allow_unverified_participation": false,
  "state": "draft",
  "description_display_mode": "truncated",
  "image_url": "string",
  "send_acknowledgement_to_admins": false,
  "send_acknowledgement": false,
  "archival_reason_message": "archival message",
  "notifications_emails": "devteam@bangthetable.com",
  "comment_text_limit": 250,
  "limit_comment": false
}

```

Guest Book

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the guest book|
|name|string|false|none|none|
|permalink|string|false|none|none|
|intro_msg|string|false|none|none|
|thank_you_message|string|false|none|none|
|moderated|boolean|false|none|none|
|premoderated|boolean|false|none|none|
|allow_unverified_participation|boolean|false|none|none|
|state|string|false|none|none|
|description_display_mode|string|false|none|none|
|image_url|string|false|none|none|
|send_acknowledgement_to_admins|boolean|false|none|none|
|send_acknowledgement|boolean|false|none|none|
|archival_reason_message|string|false|none|none|
|notifications_emails|string|false|none|none|
|comment_text_limit|integer|false|none|none|
|limit_comment|boolean|false|none|none|

<h2 id="tocS_Hub">Hub</h2>
<!-- backwards compatibility -->
<a id="schemahub"></a>
<a id="schema_Hub"></a>
<a id="tocShub"></a>
<a id="tocshub"></a>

```json
{
  "id": 1,
  "description": "new_description",
  "name": "longtext",
  "meta_description": "new_meta_description",
  "meta_keywords": "new_meta_keywords",
  "permalink": "string",
  "description_display_mode": "truncated",
  "image_url": "http://test.com/image.png",
  "image_caption": "string",
  "image_description": "string",
  "is_new_hub": false,
  "visibility_mode": "Protected",
  "text_wrap_mode": "string",
  "user_ids": [
    0
  ],
  "platform_analytics_tag_list": [
    "string"
  ]
}

```

Hub

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the hub|
|description|string|false|none|none|
|name|string|false|none|none|
|meta_description|string|false|none|none|
|meta_keywords|string|false|none|none|
|permalink|string|false|none|none|
|description_display_mode|string|false|none|none|
|image_url|string|false|none|none|
|image_caption|string|false|none|none|
|image_description|string|false|none|none|
|is_new_hub|boolean|false|none|none|
|visibility_mode|string|false|none|none|
|text_wrap_mode|string|false|none|none|
|user_ids|[integer]|false|none|none|
|platform_analytics_tag_list|[string]|false|none|none|

<h2 id="tocS_HubPageRevision">HubPageRevision</h2>
<!-- backwards compatibility -->
<a id="schemahubpagerevision"></a>
<a id="schema_HubPageRevision"></a>
<a id="tocShubpagerevision"></a>
<a id="tocshubpagerevision"></a>

```json
{
  "id": 1,
  "hub_id": 1,
  "published": false,
  "sections": {
    "sample_meta": {
      "brand-color": "string"
    }
  },
  "created_at": "2020-11-13T10:00:00.000Z",
  "updated_at": "2020-11-13T10:00:00.000Z"
}

```

HubPageRevision

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the hub page revision|
|hub_id|integer|false|none|Hub Id of that belongs to hub page revision|
|published|boolean|false|none|none|
|sections|object|false|none|none|
|» sample_meta|object|false|none|none|
|»» brand-color|string|false|none|none|
|created_at|string(date-time)|false|none|Date/Time of record created|
|updated_at|string(date-time)|false|none|Date/Time of record updated|

<h2 id="tocS_HomePageRevision">HomePageRevision</h2>
<!-- backwards compatibility -->
<a id="schemahomepagerevision"></a>
<a id="schema_HomePageRevision"></a>
<a id="tocShomepagerevision"></a>
<a id="tocshomepagerevision"></a>

```json
{
  "id": 1,
  "site_id": 1,
  "published": false,
  "sections": {
    "sample": "string"
  },
  "created_at": "2020-11-13T10:00:00.000Z",
  "updated_at": "2020-11-13T10:00:00.000Z"
}

```

HomePageRevision

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the home page revision|
|site_id|integer|false|none|Site Id of that belongs to home page revision|
|published|boolean|false|none|none|
|sections|object|false|none|none|
|» sample|string|false|none|none|
|created_at|string(date-time)|false|none|Date/Time of record created|
|updated_at|string(date-time)|false|none|Date/Time of record updated|

<h2 id="tocS_Idea">Idea</h2>
<!-- backwards compatibility -->
<a id="schemaidea"></a>
<a id="schema_Idea"></a>
<a id="tocSidea"></a>
<a id="tocsidea"></a>

```json
{
  "id": 1,
  "name": "Test",
  "description": "description 122",
  "image_url": "string",
  "author": "user8179",
  "votes_count": 10,
  "created_at": "2020-11-13T10:00:00.000Z",
  "email": "user9245@example.com"
}

```

Idea

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the idea|
|name|string|false|none|none|
|description|string|false|none|none|
|image_url|string|false|none|none|
|author|string|false|none|none|
|votes_count|integer|false|none|none|
|created_at|string(date-time)|false|none|Date/Time of record created|
|email|string|false|none|none|

<h2 id="tocS_Tag">Tag</h2>
<!-- backwards compatibility -->
<a id="schematag"></a>
<a id="schema_Tag"></a>
<a id="tocStag"></a>
<a id="tocstag"></a>

```json
{
  "id": 1,
  "name": "New"
}

```

Tag

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the tag|
|name|string|false|none|none|

<h2 id="tocS_Project">Project</h2>
<!-- backwards compatibility -->
<a id="schemaproject"></a>
<a id="schema_Project"></a>
<a id="tocSproject"></a>
<a id="tocsproject"></a>

```json
{
  "id": 1,
  "description": "new_description",
  "name": "test",
  "meta_description": "new_meta_description",
  "meta_keywords": "new_meta_keywords",
  "redirect_url": "https://google.com",
  "permalink": "test123",
  "state": "draft",
  "banner_url": "http://test.com/test.png",
  "restrict_forum_creation": true,
  "description_display_mode": "truncated",
  "visibility_mode": "Public",
  "platform_analytics_tag_list": [
    "something",
    "nothing"
  ],
  "image_url": "http://test.com/image.png",
  "image_caption": "string",
  "image_description": "string",
  "text_wrap_mode": "textwrap_default",
  "parent_id": 1,
  "subscribers_count": 10,
  "view_count": 10,
  "home_project": true,
  "published_at": "string",
  "forum_topics": 10,
  "survey_tools": 10,
  "banner_caption": "string",
  "widget_resource_count": 10,
  "quick_poll_layout": "tool",
  "created_at": "2020-11-13T10:00:00.000Z",
  "archival_reason_message": "string",
  "contribution_count": 10,
  "scheduled_at": "2020-11-13T10:00:00.000Z"
}

```

Project

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the project|
|description|string|false|none|none|
|name|string|false|none|none|
|meta_description|string|false|none|none|
|meta_keywords|string|false|none|none|
|redirect_url|string|false|none|none|
|permalink|string|false|none|none|
|state|string|false|none|none|
|banner_url|string|false|none|none|
|restrict_forum_creation|boolean|false|none|none|
|description_display_mode|string|false|none|none|
|visibility_mode|string|false|none|none|
|platform_analytics_tag_list|[string]|false|none|none|
|image_url|string|false|none|none|
|image_caption|string|false|none|none|
|image_description|string|false|none|none|
|text_wrap_mode|string|false|none|none|
|parent_id|integer|false|none|none|
|subscribers_count|integer|false|none|none|
|view_count|integer|false|none|none|
|home_project|boolean|false|none|none|
|published_at|string|false|none|none|
|forum_topics|integer|false|none|none|
|survey_tools|integer|false|none|none|
|banner_caption|string|false|none|none|
|widget_resource_count|integer|false|none|none|
|quick_poll_layout|string|false|none|none|
|created_at|string(date-time)|false|none|Date/Time of record created|
|archival_reason_message|string|false|none|none|
|contribution_count|integer|false|none|none|
|scheduled_at|string(date-time)|false|none|Date/Time of record schedule|

<h2 id="tocS_Brainstormer">Brainstormer</h2>
<!-- backwards compatibility -->
<a id="schemabrainstormer"></a>
<a id="schema_Brainstormer"></a>
<a id="tocSbrainstormer"></a>
<a id="tocsbrainstormer"></a>

```json
{
  "id": 1,
  "name": "testing",
  "description": "testing description",
  "permalink": "sample-brainstormer",
  "state": "published",
  "tag_list": [
    "abc",
    "xyz"
  ],
  "voting_start_at": "2020-11-13T10:00:00.000Z",
  "voting_end_at": "2020-11-13T10:00:00.000Z",
  "image_url": "string",
  "archival_reason_message": "archival message",
  "ideas_count": 10,
  "created_at": "2020-11-13T10:00:00.000Z",
  "sticked": false,
  "updated_at": "2020-11-13T10:00:00.000Z",
  "sequence": 1,
  "notifications_emails": "abc@example.com",
  "allow_comments_for_ideas": false,
  "allow_file_upload_for_ideas": false,
  "send_acknowledgement_to_admins": true,
  "send_acknowledgement": true,
  "allow_unverified_participation": true,
  "scheduled_at": "2020-11-13T10:00:00.000Z"
}

```

Brainstormer

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the brainstormer|
|name|string|false|none|none|
|description|string|false|none|none|
|permalink|string|false|none|none|
|state|string|false|none|none|
|tag_list|[string]|false|none|none|
|voting_start_at|string(date-time)|false|none|Date/Time of record voting_start_at|
|voting_end_at|string(date-time)|false|none|Date/Time of record voting_end_at|
|image_url|string|false|none|none|
|archival_reason_message|string|false|none|none|
|ideas_count|integer|false|none|none|
|created_at|string(date-time)|false|none|Date/Time of record created_at|
|sticked|boolean|false|none|none|
|updated_at|string(date-time)|false|none|Date/Time of record updated_at|
|sequence|integer|false|none|none|
|notifications_emails|string|false|none|none|
|allow_comments_for_ideas|boolean|false|none|none|
|allow_file_upload_for_ideas|boolean|false|none|none|
|send_acknowledgement_to_admins|boolean|false|none|none|
|send_acknowledgement|boolean|false|none|none|
|allow_unverified_participation|boolean|false|none|none|
|scheduled_at|string(date-time)|false|none|Date/Time of record scheduled_at|

<h2 id="tocS_SurveyTool">SurveyTool</h2>
<!-- backwards compatibility -->
<a id="schemasurveytool"></a>
<a id="schema_SurveyTool"></a>
<a id="tocSsurveytool"></a>
<a id="tocssurveytool"></a>

```json
{
  "id": 1,
  "name": "survey 353",
  "description": "<img src=\"something.png\" /> Description",
  "permalink": "survey_tool355-92",
  "state": "draft",
  "image_url": "another_thing.png",
  "archival_reason_message": "archival message",
  "send_acknowledgement": true,
  "send_acknowledgement_to_admin": true,
  "notification_emails": "devteam@bangthetable.com",
  "allow_anonymous_participation": false,
  "allow_user_to_post_multiple_times": false,
  "allow_unverified_participation": true,
  "thanks_msg": "string",
  "pinned": true,
  "tag_list": [
    "string"
  ],
  "responses_count": 10,
  "created_at": "2020-11-13T10:00:00.000Z",
  "updated_at": "2020-11-13T10:00:00.000Z",
  "sequence": 0,
  "randomize_pages": false,
  "randomize_questions": false,
  "randomize_options": false,
  "modified_at": "2020-11-13T10:00:00.000Z",
  "submit_button_text": "string",
  "multiple_times_msg": "You have already responded. You cannot take this survey more than once. Thank You.",
  "show_response_count": false,
  "show_results": true,
  "is_new_survey": true,
  "show_progress_bar": true,
  "file_question_count": 0,
  "scheduled_at": "2020-11-13T10:00:00.000Z",
  "visibility": "inherit"
}

```

SurveyTool

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the surveytool|
|name|string|false|none|none|
|description|string|false|none|none|
|permalink|string|false|none|none|
|state|string|false|none|none|
|image_url|string|false|none|none|
|archival_reason_message|string|false|none|none|
|send_acknowledgement|boolean|false|none|none|
|send_acknowledgement_to_admin|boolean|false|none|none|
|notification_emails|string|false|none|none|
|allow_anonymous_participation|boolean|false|none|none|
|allow_user_to_post_multiple_times|boolean|false|none|none|
|allow_unverified_participation|boolean|false|none|none|
|thanks_msg|string|false|none|none|
|pinned|boolean|false|none|none|
|tag_list|[string]|false|none|none|
|responses_count|integer|false|none|none|
|created_at|string(date-time)|false|none|Date/Time of record created_at|
|updated_at|string(date-time)|false|none|Date/Time of record updated_at|
|sequence|integer|false|none|none|
|randomize_pages|boolean|false|none|none|
|randomize_questions|boolean|false|none|none|
|randomize_options|boolean|false|none|none|
|modified_at|string(date-time)|false|none|Date/Time of record modified_at|
|submit_button_text|string|false|none|none|
|multiple_times_msg|string|false|none|none|
|show_response_count|boolean|false|none|none|
|show_results|boolean|false|none|none|
|is_new_survey|boolean|false|none|none|
|show_progress_bar|boolean|false|none|none|
|file_question_count|integer|false|none|none|
|scheduled_at|string(date-time)|false|none|Date/Time of record scheduled_at|
|visibility|string|false|none|none|

<h2 id="tocS_Forum">Forum</h2>
<!-- backwards compatibility -->
<a id="schemaforum"></a>
<a id="schema_Forum"></a>
<a id="tocSforum"></a>
<a id="tocsforum"></a>

```json
{
  "id": 1,
  "name": "sample",
  "description": "sample description",
  "permalink": "permalink_137",
  "state": "published",
  "allow_unverified_participation": false,
  "description_display_mode": "truncated",
  "image_url": "string",
  "archival_reason_message": "string",
  "comments_count": 10,
  "tag_list": [
    "string"
  ],
  "sequence": 0,
  "created_at": "2020-11-13T10:00:00.000Z",
  "updated_at": "2020-11-13T10:00:00.000Z",
  "notifications_emails": "string",
  "send_acknowledgement_to_admins": false,
  "send_acknowledgement": false,
  "author": "user3977",
  "likes_count": 10,
  "has_liked_the_forum": true,
  "forum_liked_id": 1
}

```

Forum

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the forum|
|name|string|false|none|none|
|description|string|false|none|none|
|permalink|string|false|none|none|
|state|string|false|none|none|
|allow_unverified_participation|boolean|false|none|none|
|description_display_mode|string|false|none|none|
|image_url|string|false|none|none|
|archival_reason_message|string|false|none|none|
|comments_count|integer|false|none|none|
|tag_list|[string]|false|none|none|
|sequence|integer|false|none|none|
|created_at|string(date-time)|false|none|Date/Time of record created_at|
|updated_at|string(date-time)|false|none|Date/Time of record updated_at|
|notifications_emails|string|false|none|none|
|send_acknowledgement_to_admins|boolean|false|none|none|
|send_acknowledgement|boolean|false|none|none|
|author|string|false|none|none|
|likes_count|integer|false|none|none|
|has_liked_the_forum|boolean|false|none|none|
|forum_liked_id|integer|false|none|none|

<h2 id="tocS_QuickPoll">QuickPoll</h2>
<!-- backwards compatibility -->
<a id="schemaquickpoll"></a>
<a id="schema_QuickPoll"></a>
<a id="tocSquickpoll"></a>
<a id="tocsquickpoll"></a>

```json
{
  "id": 1,
  "name": "QuickPoll 137",
  "description": "This is a quick poll.",
  "permalink": "quickpoll-137",
  "state": "published",
  "archival_reason_message": "archival message",
  "allow_unverified_participation": true,
  "allow_anonymous_participation": false,
  "results": "string",
  "thanks_msg": "string",
  "image_url": "string",
  "sequence": 1,
  "created_at": "2020-11-13T10:00:00.000Z",
  "updated_at": "2020-11-13T10:00:00.000Z",
  "tag_list": [
    "a",
    "b"
  ],
  "visibility": "inherit"
}

```

Quick Poll

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the quick poll|
|name|string|false|none|none|
|description|string|false|none|none|
|permalink|string|false|none|none|
|state|string|false|none|none|
|archival_reason_message|string|false|none|none|
|allow_unverified_participation|boolean|false|none|none|
|allow_anonymous_participation|boolean|false|none|none|
|results|string|false|none|none|
|thanks_msg|string|false|none|none|
|image_url|string|false|none|none|
|sequence|integer|false|none|none|
|created_at|string(date-time)|false|none|Date/Time of record created_at|
|updated_at|string(date-time)|false|none|Date/Time of record updated_at|
|tag_list|[string]|false|none|none|
|visibility|string|false|none|none|

<h2 id="tocS_Map">Map</h2>
<!-- backwards compatibility -->
<a id="schemamap"></a>
<a id="schema_Map"></a>
<a id="tocSmap"></a>
<a id="tocsmap"></a>

```json
{
  "id": 1,
  "name": "new sample",
  "description": "new description",
  "permalink": "sample-permalink",
  "state": "draft",
  "image_url": "abc.png",
  "archival_reason_message": "string",
  "lat": 1,
  "lng": 3,
  "polygon": "abcdef",
  "zoom": 1,
  "bounds": "abc",
  "gis_enabled": false,
  "gis_version": "3.0",
  "gis_url": "http://abc.def",
  "gis_layer": "abc",
  "image_visibility": true,
  "show_address": false,
  "allow_unverified_participation": false,
  "optional_comment": false,
  "created_at": "2020-11-13T10:00:00.000Z",
  "updated_at": "2020-11-13T10:00:00.000Z",
  "tag_list": [
    "a",
    "b"
  ],
  "responses_count": 10,
  "style": "string",
  "survey": {},
  "sequence": 1,
  "target_srs": "EPSG:3826",
  "description_display_mode": "string",
  "snapshot_url": "string",
  "mapboxgl_enabled": true,
  "hide_survey_response": false,
  "restrict_marker_creation": false
}

```

Map

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the map|
|name|string|false|none|none|
|description|string|false|none|none|
|permalink|string|false|none|none|
|state|string|false|none|none|
|image_url|string|false|none|none|
|archival_reason_message|string|false|none|none|
|lat|number(float)|false|none|latitude of the map|
|lng|number(float)|false|none|longitude of the map|
|polygon|string|false|none|none|
|zoom|integer|false|none|none|
|bounds|string|false|none|none|
|gis_enabled|boolean|false|none|none|
|gis_version|string|false|none|none|
|gis_url|string|false|none|none|
|gis_layer|string|false|none|none|
|image_visibility|boolean|false|none|none|
|show_address|boolean|false|none|none|
|allow_unverified_participation|boolean|false|none|none|
|optional_comment|boolean|false|none|none|
|created_at|string(date-time)|false|none|Date/Time of record created_at|
|updated_at|string(date-time)|false|none|Date/Time of record updated_at|
|tag_list|[string]|false|none|none|
|responses_count|integer|false|none|none|
|style|string|false|none|none|
|survey|object|false|none|none|
|sequence|integer|false|none|none|
|target_srs|string|false|none|none|
|description_display_mode|string|false|none|none|
|snapshot_url|string|false|none|none|
|mapboxgl_enabled|boolean|false|none|none|
|hide_survey_response|boolean|false|none|none|
|restrict_marker_creation|boolean|false|none|none|

<h2 id="tocS_Newsletter">Newsletter</h2>
<!-- backwards compatibility -->
<a id="schemanewsletter"></a>
<a id="schema_Newsletter"></a>
<a id="tocSnewsletter"></a>
<a id="tocsnewsletter"></a>

```json
{
  "id": 1,
  "subject": "New Newsletter",
  "state": "preview",
  "banner_source": "3224",
  "banner_source_url": "new/new_test_image.png",
  "show_logo": true,
  "sent_at": "2020-11-13T10:00:00.000Z",
  "created_at": "2020-11-13T10:00:00.000Z",
  "updated_at": "2020-11-13T10:00:00.000Z",
  "published": false,
  "recipient_count": 10,
  "body": "<p>This is ze Tesla Newsletter.</p>"
}

```

Newsletter

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the newsletter|
|subject|string|false|none|none|
|state|string|false|none|none|
|banner_source|string|false|none|none|
|banner_source_url|string|false|none|none|
|show_logo|boolean|false|none|none|
|sent_at|string(date-time)|false|none|Date/Time of record sent_at|
|created_at|string(date-time)|false|none|Date/Time of record created|
|updated_at|string(date-time)|false|none|Date/Time of record updated|
|published|boolean|false|none|none|
|recipient_count|integer|false|none|none|
|body|string|false|none|none|

<h2 id="tocS_EmailTemplate">EmailTemplate</h2>
<!-- backwards compatibility -->
<a id="schemaemailtemplate"></a>
<a id="schema_EmailTemplate"></a>
<a id="tocSemailtemplate"></a>
<a id="tocsemailtemplate"></a>

```json
{
  "id": 1,
  "subject_template": "Subject Template",
  "body_template": "Body Template",
  "emails": "abc@gmail.com,xya@gmail.com",
  "show_emails": true,
  "identifier": "notify_admin_on_new_forum_topic"
}

```

Email Template

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|Id of the email template|
|subject_template|string|false|none|none|
|body_template|string|false|none|none|
|emails|string|false|none|none|
|show_emails|boolean|false|none|none|
|identifier|string|false|none|none|

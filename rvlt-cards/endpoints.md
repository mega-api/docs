---
description: RVLT Cards Endpoints
---

# Endpoints

{% hint style="info" %}
To gain access to use this API you must donate $4 or more. You can get one API Key per every $4. Please contact Best after donating.
{% endhint %}

{% hint style="info" %}
The rvlt cards API will become more customizable in the future with the ability to create more than rank cards.
{% endhint %}

The rvlt cards URL is: [https://rvlt-cards.vercel.app](https://rvlt-cards.vercel.app)

## Render a card

<mark style="color:green;">`GET`</mark>`/v1/card`

Image rendering

**Headers**

| Name         | Value       |
| ------------ | ----------- |
| Content-Type | `image/png` |
| api-key      | `api-key`   |

**Body**

<table><thead><tr><th>Name</th><th>Type</th><th>Description</th><th data-type="checkbox">Required</th></tr></thead><tbody><tr><td>user<code>name</code></td><td>string</td><td>Name/Username of the user</td><td>true</td></tr><tr><td><code>level</code></td><td>number</td><td>Current level</td><td>true</td></tr><tr><td><code>xp</code></td><td>number</td><td>Current XP</td><td>true</td></tr><tr><td><code>maxXp</code></td><td>number</td><td>XP needed for next level</td><td>true</td></tr><tr><td><code>placement</code></td><td>number</td><td>Users current position in the leaderbaord</td><td>false</td></tr><tr><td><code>totalUsers</code></td><td>number</td><td>Total number of users in the server</td><td>false</td></tr><tr><td><code>avatar</code></td><td>string</td><td>URL of the users avatar</td><td>false</td></tr><tr><td><code>banner</code></td><td>string</td><td>URL of the users banner/background</td><td>false</td></tr></tbody></table>

**Response**

{% tabs %}
{% tab title="200" %}
```
Image URL
```
{% endtab %}

{% tab title="403" %}
```json
{
    "error": "Unauthorized request"
}
```
{% endtab %}

{% tab title="500" %}
```json
{
  "error": "Card generation failed"
}
```
{% endtab %}
{% endtabs %}

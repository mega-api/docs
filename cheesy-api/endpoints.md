---
description: Cheesy API Endpoints
---

# Endpoints

The cheesy-api URL is: [https://cheesy-api.vercel.app/](https://cheesy-api.vercel.app/)

## Upload a Cheese

<mark style="color:green;">`POST`</mark> `api/v1/upload`

Upload a cheese image (jpeg, png, gif)

**Headers**

| Name         | Value              |
| ------------ | ------------------ |
| Content-Type | `application/json` |
| x-api-key    | `API Key`          |

**Body**

| Name       | Type   | Description                         |
| ---------- | ------ | ----------------------------------- |
| `imageUrl` | string | URL of the Image you wish to upload |

**Response**

{% tabs %}
{% tab title="200" %}
```json
{
    "message": "Image uploaded successfully!",
    "imageUrl": "https://res.cloudinary.com/your-cloud-name/image/upload/v1234567890/cheeses/your-image-id.jpg"
}
```
{% endtab %}

{% tab title="400" %}
```json
{
  "error": "Invalid request"
}
```
{% endtab %}
{% endtabs %}

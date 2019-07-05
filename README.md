__AudioBuku API Reference__

API Base URL

https://api.audiobuku.com

**HTTP(S) Request / HTTP(S) Header**

| Header | Value |
| --- | --- |
| Content-Type | application/json |
| Accept | application/json |
| Authorization | Bearer key |

## List API Methods
| End Point | HTTP Method | Deskripsi |
| --- | --- | --- |
| [`/api/v1/collections`](#collections1) | GET | Show data audiobook filter by collection id |
| [`/api/v1/audiobooks?collection_id={id}`](#audiobooks1) | GET | Show data audiobook filter by collection id |
| [`/api/v1/audiobooks?category_id={id}`](#audiobooks1) | GET | Show data audiobook filter by category audiobook id |
| [`/api/v1/audiobooks?narrator_id={id}`](#audiobooks1) | GET | Show data audiobook filter by narrator id |
| [`/api/v1/audiobooks?author_id={id}`](#audiobooks1) | GET | Show data audiobook filter by author id |
| [`/api/v1/audiobooks?publisher_book_id={id}`](#audiobooks1) | GET | Show data audiobook filter by publisher book id |
| [`/api/v1/audiobooks?publisher_audiobook_id={id}`](#audiobooks1) | GET | Show data audiobook filter by publisher audio id |
| [`/api/v1/audiobooks?search={character}`](#audiobooks1) | GET | Show data audiobook filter by character or title |
| [`/api/v1/categories`](#category) | GET | Show data category audiobook |
| [`/api/v1/categories/{id}`](#category) | GET | Show data subcategory audiobook |

<a name="collections1"/>
## Result collection  

```json
[
    {
        "id": 338,
        "title": "Best Seller",
        "picture_url": null,
        "subtitle": "most wanted audiobook",
        "visibility": 1,
        "audiobook": [
            {
                "id": 631,
                "cover_picture_url": "https://storage.googleapis.com/audiobukucover/631_20170202061506.png",
                "title": "Keluarga Tak Kasat Mata",
                "pivot": {
                    "collection_id": 338,
                    "audiobook_id": 631
                }
            }
        ]
    }
]
```


<a name="audiobooks1"/>
## Result audiobooks  

```json
[
    {
        "id": 631,
        "title": "Keluarga Tak Kasat Mata",
        "cover_picture_url": "https://storage.googleapis.com/audiobukucover/631_20170202061506.png",
        "updated_at": "2019-07-05 08:33:50",
        "price": 75000,
        "author": "Bonaventura Genta",
        "created_at": "2017-02-02 12:45:35",
        "released_at": "2019-06-14 13:02:46",
        "audiobook_id": 631,
        "reviews_count": 10,
        "ratings_average": 4.1,
        "wishlisted": null,
        "purchased": null,
        "review": [
            {
                "id": 5745,
                "rating": 3,
                "content": "lumayan lahh . first horror story gue nih",
                "created_at": "2017-12-29 12:50:45",
                "updated_at": "2017-12-29 12:50:45",
                "name": "riezka rahma",
                "photo_url": "https://lh3.googleusercontent.com/-0F1d6t5LSLI/AAAAAAAAAAI/AAAAAAAAAHo/qEtJE25RCYc/s96-c/photo.jpg"
            }
        ],
        "purchase_count": 209,
        "authorslist": [
            {
                "audiobook_id": 631,
                "id": 53,
                "username": "Bonaventura Genta",
                "photo_url": null
            }
        ],
        "narratorslist": [
            {
                "audiobook_id": 631,
                "id": 37,
                "username": "Dian Tedjo",
                "photo_url": null
            }
        ]
    }
    ]
```
<a name="category"/>
## Result category  

```json
{
    "error": true,
    "userMessage": "success",
    "data": [
        {
            "id": 83,
            "title": "BELAJAR BAHASA",
            "picture_url": "https://storage.googleapis.com/audiobukucover/456_20161227175855.jpg"
        },
        {
            "id": 99,
            "title": "BIOGRAFI & MEMOAR",
            "picture_url": "https://storage.googleapis.com/audiobukucover/490_20161226030219.jpg"
        }
    ]
}
```

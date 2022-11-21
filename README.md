# API guide for Network Subscription Payment


## List all Network Billing Profile 


```Endpoint:- https://api.random.com/api/v1/premium/membership/network/billing/all/```


```Methods allowed:- GET```


```javascript

Headers = {
    Authorization: `Bearer ${token}`
}

```

```javascript

Response = {
    "count": 1,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": 1,
            "network": {
                "id": "NQP8ZPEB",
                "user": "0s6xuw6g1el3jp",
                "category": {
                    "id": 1,
                    "name": "Clothes",
                    "priority": 2,
                    "image": "https://random-alpha.s3-us-west-2.amazonaws.com/Content/images/undraw_team_up_ip2x.svg",
                    "created": "1603048978000"
                },
                "network_url": null,
                "thumbnail_image": "https://content.radom.com/images/ne-image.jpg",
                "network_type": {
                    "id": 1,
                    "name": "Importer",
                    "image": "https://radom-alpha.s3-us-west-2.amazonaws.com/Content/images/undraw_team_up_ip2x.svg",
                    "created": "1603048999000"
                },
                "name": "Nikom Coolpix Store",
                "address": "20, B-47, New Awas Vikas Colony",
                "landmark": "Near ASG Grand Plaza Mall",
                "city": "Muzaffarnagar",
                "state": "Uttar Pradesh",
                "country": "India",
                "pincode": "251001",
                "timings": [
                    {
                        "day": "Weekday",
                        "opening": "10:00 AM",
                        "closing": "08:00 PM",
                        "status": true
                    }
                ],
                "rating": "5.0",
                "no_of_reviews": 0,
                "registered_stores": 1,
                "followers": 0,
                "is_verified": false,
                "is_active": true,
                "is_premium": false,
                "is_spam": false,
                "is_video": true,
                "is_document": true
            },
            "full_name": "Manoj Tyagi",
            "email": "manoj@gmail.com",
            "address": "20, Avaas Vikas",
            "landmark": "Near Hanuman Mandir",
            "city": "Muzaffarnagar",
            "state": "Uttar Pradesh",
            "country": "India",
            "pincode": "251202",
            "is_active": true,
            "added": "1603054722000",
            "updated": "1603054722000"
        }
    ]
}

```

##### Details of the fields

```javascript

{
    id: "Int, Primary Key of Billing Profile",
    network: {
        // Network information who created the billing profile
    },
    full_name: "String, Full name of the user who created the billing profile",
    email: "String, Email of the user",
    address: "String, Detailed address of the user who created the billing profile",
    landmark: "String, Landmark of the locality",
    city: "String, City of the User",
    state: "String, State of the user",
    country: "String, Country of the User",
    pincode: "String, Pincode of the locality",
    is_active: "bool, true only if the user have an active billing profile",
    added: "Timestamp at which billing profile added",
    updated: "Timestamp at which billing profile added"
}

```

##### Possible use cases of the API

- To get all the billing profiles for a particular network
    - ```https://api.random.com/api/v1/premium/membership/network/billing/all/?network={Network_id}```

- To get all the billing profiles that are active currently 
    - ```https://api.random.com/api/v1/premium/membership/network/billing/all/?is_active=true```

<hr />



## Create new Network Billing Profile 


```Endpoint:- https://api.random.com/api/v1/premium/membership/network/billing/create/```


```Methods allowed:- POST```


```javascript

Headers = {
    Authorization: `Bearer ${token}`
}

```

```javascript


Request = {
    "network": "NQP8ZPEB",
    "full_name": "Manoj Tyagi",
    "email": "manoj@gmail.com",
    "address": "20, Avaas Vikas",
    "landmark": "Near Hanuman Mandir",
    "city": "Muzaffarnagar",
    "state": "Uttar Pradesh",
    "country": "India",
    "pincode": "251202",
    "is_active": true
}

Response = {
    "id": 1,
    "network": "NQP8ZPEB",
    "full_name": "Manoj Tyagi",
    "email": "manoj@gmail.com",
    "address": "20, Avaas Vikas",
    "landmark": "Near Hanuman Mandir",
    "city": "Muzaffarnagar",
    "state": "Uttar Pradesh",
    "country": "India",
    "pincode": "251202",
    "is_active": true,
    "added": "1603054722000",
    "updated": "1603054722000"
}

```

##### Details of the fields

```javascript

{
    id: "Int, Primary Key of Billing Profile",
    network: "String, Network ID who is creating the billing profile - Foreign Key",
    full_name: "String, Full name of the user who created the billing profile",
    email: "String, Email of the user",
    address: "String, Detailed address of the user who created the billing profile",
    landmark: "String, Landmark of the locality",
    city: "String, City of the User",
    state: "String, State of the user",
    country: "String, Country of the User",
    pincode: "String, Pincode of the locality",
    is_active: "bool, true only if the user have an active billing profile",
    added: "Timestamp at which billing profile added",
    updated: "Timestamp at which billing profile added"
}

```


<hr />



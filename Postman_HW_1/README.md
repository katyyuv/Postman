# Homework 1

## Create requests in Postman
```
Protocol: http
IP: 162.55.220.72
Port: 5007
```
### EP_1
Method: GET

EndPoint: /get_method

request url params: 
- name: str
- age: int

Request:

`http://162.55.220.72:5007/get_method?name=Kate&age=21`

Response:
```
[
    "Kate",
    "21"
]
```

### EP_2
Method: POST

EndPoint: /user_info_3

request url params: 
- name: str
- age: int
- salary: int

Request:

`http://162.55.220.72:5007/user_info_3`

Response:
```
{
    "age": "21",
    "family": {
        "children": [
            [
                "Alex",
                24
            ],
            [
                "Kate",
                12
            ]
        ],
        "u_salary_1_5_year": 1600
    },
    "name": "Kate",
    "salary": 400
}
```

### EP_3
Method: GET

EndPoint: /object_info_1

request url params: 
- name: str
- age: int
- weight: int 

Request:

`http://162.55.220.72:5007/object_info_1?name=Kate&age=21&weight=56`

Response:
```
{
    "age": 21,
    "daily_food": 0.672,
    "daily_sleep": 140.0,
    "name": "Kate"
}
```

### EP_4
Method: GET

EndPoint: /object_info_2

request url params: 
- name: str
- age: int
- salary: int

Request:

`http://162.55.220.72:5007/object_info_2?name=Kate&age=21&salary=400`

Response:
```
{
    "person": {
        "u_age": 21,
        "u_name": [
            "Kate",
            400,
            21
        ],
        "u_salary_5_years": 1680.0
    },
    "qa_salary_after_1.5_year": 1320.0,
    "qa_salary_after_12_months": 1080.0,
    "qa_salary_after_3.5_years": 1520.0,
    "qa_salary_after_6_months": 800,
    "start_qa_salary": 400
}
```

### EP_5
Method: GET

EndPoint: /object_info_3

request url params: 
- name: str
- age: int
- salary: int

Request:

`http://162.55.220.72:5007/object_info_3?name=Kate&age=21&salary=400`

Response:
```
{
    "age": "21",
    "family": {
        "children": [
            [
                "Alex",
                24
            ],
            [
                "Kate",
                12
            ]
        ],
        "pets": {
            "cat": {
                "age": 3,
                "name": "Sunny"
            },
            "dog": {
                "age": 4,
                "name": "Luky"
            }
        },
        "u_salary_1_5_year": 1600
    },
    "name": "Kate",
    "salary": 400
}
```

### EP_6
Method: GET

EndPoint: /object_info_4

request url params: 
- name: str
- age: int
- salary: int

Request:

`http://162.55.220.72:5007/object_info_4?name=Kate&age=21&salary=400`

Response:
```
{
    "age": 21,
    "name": "Kate",
    "salary": [
        400,
        "800",
        "1200"
    ]
}
```

### EP_7
Method: POST

EndPoint: /get_method

request url params: 
- name: str
- age: int
- salary: int

Request:

`http://162.55.220.72:5007/user_info_2`

Response:
```
{
    "person": {
        "u_age": 21,
        "u_name": [
            "Kate",
            400,
            21
        ],
        "u_salary_5_years": 1680.0
    },
    "qa_salary_after_1.5_year": 1320.0,
    "qa_salary_after_12_months": 1080.0,
    "qa_salary_after_3.5_years": 1520.0,
    "qa_salary_after_6_months": 800,
    "start_qa_salary": 400
}
```

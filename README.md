# api_final

Description: API cоциальной сети Yatube.
Install: 
git clone git@github.com:antkrav/api_final_yatube.git
python3 -m venv venv
source venv/bin/activate
python3 -m pip install --upgrade pip
pip3 install -r requirements.txt
cd yatube_api
python3 manage.py migrate
python3 manage.py runserver
Examples: 
GET http://127.0.0.1:8000/api/v1/posts/
{
    "count": 123,
    "next": "http://api.example.org/accounts/?offset=400&limit=100",
    "previous": "http://api.example.org/accounts/?offset=200&limit=100",
    "results": [
        {
            "id": 0,
            "author": "string",
            "text": "string",
            "pub_date": "2021-10-14T20:41:29.648Z",
            "image": "string",
            "group": 0
        }
    ]
}
POST http://127.0.0.1:8000/api/v1/posts/
запрос:
{
    "text": "string",
    "image": "string",
    "group": 0
}
ответ:
{
    "id": 0,
    "author": "string",
    "text": "string",
    "pub_date": "2019-08-24T14:15:22Z",
    "image": "string",
    "group": 0
}

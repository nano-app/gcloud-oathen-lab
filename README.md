# gcloud-oathen-lab

## INTRO 
-----
1. Create gcloud (drive, sheets) API, credential for web authentication (public)
2. Authenticate a user (gmail) from web form (javascript/ get ulr)
3. Using return/ call back info (access-token) to read/list drive content from API get
-----

## ref.
https://developers.google.com/identity/protocols/oauth2/javascript-implicit-flow?hl=vi

## Main steps

@ gcloud console
  - create gcloud api  
    - API List (drive, sheets, gmail...)
      - Lib/api METRIC: selection/map: version > creadential > Method (read, write?)..
    - Credential:
      - client-id, secret (json file download if need for server app)
      - redirect uri (http://localhost): call back .. port modifiy if needed
      - Make public (testing: need to add list user)


@ localhost laptop:
  1. Authen user page and get the access-token
  - create index.html file
  - run webserver with http://localhost (or redirect url setting)
  - click and authen user + consense
  - copy the access-token in call back url
  
  2. Call the API with obtained access-token:
  GET https://www.googleapis.com/drive/v2/files?access_token=<the access-token here!!>

     
    

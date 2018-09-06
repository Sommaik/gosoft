# gosoft

### PROJECT REST API
#### get all project 
- GET http://train-api.pnpsw.com/api/v1/project 

#### insert new project
- POST http://train-api.pnpsw.com/api/v1/project
- HEADER 
```
Authorization : JWT eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyQ29kZSI6Ik5vb3RpM3ciLCJ1c2VyTmFtZSI6IkNob25uaXNhIiwidXNlckxhc3ROYW1lIjoiVGhpZW1idW5kaXQiLCJ1c2VyRW1haWwiOiJ0aWV3d2FfaGFoYUBob3RtYWlsLmNvbSJ9.Gnb5Wx3jDi-6IVtGpfG64atQMaX6brBjRozitU0nlcQ

Content-Type : application/json
```
- BODY
```
{
  "projCode" : "PROJ1",
  "projImage" : "proj1.png",
  "projName" : "Project1",
  "status" : "N"
}
```

#### update project
- PUT http://train-api.pnpsw.com/api/v1/project
- HEADER 
```
Authorization : JWT eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyQ29kZSI6Ik5vb3RpM3ciLCJ1c2VyTmFtZSI6IkNob25uaXNhIiwidXNlckxhc3ROYW1lIjoiVGhpZW1idW5kaXQiLCJ1c2VyRW1haWwiOiJ0aWV3d2FfaGFoYUBob3RtYWlsLmNvbSJ9.Gnb5Wx3jDi-6IVtGpfG64atQMaX6brBjRozitU0nlcQ
  
Content-Type : application/json
```
- BODY
```
{
  "projCode" : "PROJ1",
  "projImage" : "proj1-1.png",
  "projName" : "Project1-1",
  "status" : "Y",
  "pkCode" : "ISSUE-PROJECT-PROJ1"
}
```

#### delete project
- DELETE http://train-api.pnpsw.com/api/v1/project/{{pkCode}}

### get project by key
- GET {{url}}/api/v1/project/findByID/{{pkCode}}

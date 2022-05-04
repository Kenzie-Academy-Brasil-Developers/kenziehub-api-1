 <h2 align ='center'> Cadastro de Usuario </h2>

`POST /users - FORMATO DA RESPOSTA - STATUS 201`
```json
{
	"name": "teste",
	"email": "teste@mail.com",
	"password": "1234"
}
```
Login

`POST /login - FORMATO DA RESPOSTA - STATUS 200`
```json
{
    "email":"teste@mail.com",
	"password":"1234"
}
```
 <h2 align ='center'> Cadastro de poder </h2>

`POST /magic - FORMATO DA RESPOSTA - STATUS 201`

necessario token de autenticação para criação
```json
{
    "magic":"Chute",
	"element":"ar",
	"userId":1
}
```

<h2 align ='center'> Consulta de poder </h2>

a consulta pode ser realizada sem a autenticação de usuario

`GET /magic - FORMATO DA RESPOSTA - STATUS 200`
```json
[
	{
		"magic": "Chute",
		"element": "ar",
		"userId": 1,
		"id": 1
	}
]
```





<h2 align ='center'> Cadastro de Overpoder</h2>

Cadastro/consulta somente com autenticação

`POST /overpower - FORMATO DA RESPOSTA - STATUS 201`
```json
{
	"name":"Mega Soco",
	"element" : "Fire"
}
```
consulta Overpower







`GET /overpower FORMATO DA RESPOSTA - STATUS 200`
```json
[
	{
		"name": "Mega Soco",
		"element": "Fire",
		"id": 1
	}
]
```
 <h2 align ='center'> Possiveis errros </h2>

Resposta de Error cadastro / consulta

`401 - Unauthorized `
```json
"Missing token"
"Missing authorization header"
```
verificar token

Cadastro

`400 - Bad Request`
```json
"Email format is invalid"
"Email and password are required"
```
# Xendit-Go

## Description
**Xendit-Go** is an example of using Xendit API in Golang

## Installation & Configuration
Ensure you have installed:
* [Golang](https://golang.org/doc/install)
* [Glide - Golang Package Management]  (https://github.com/Masterminds/glide)

## Examples
* Run `glide install` to install all your dependencies
* Go to examples folder

  `cd src/test/examples`
* Create Disbursement

  `go run create_disbursement.go`
* Disbursement Callback Server (Your server will run in port 3000)

  `go run disbursement_callback.go`
* Hit `localhost:3000/disbursement_callback_url` with
    * method: **POST**
    * header: `'Content-Type: application/json'`
    * body: 
    ```json
    {
      "user_id": "5785e6334d7b410667d355c4",
      "external_id": "12345",
      "amount": 1000,
      "bank_code": "BCA",
      "account_holder_name": "RAIDY WIJAYA",
      "disbursement_description": "Refunds for shoes",
      "status": "PENDING",
      "id": "57f1ce05bb1a631a65eee662"
    }
    ```
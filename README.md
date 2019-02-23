# ATP

Asia trade pay - ATP

# Create Wallet
    Request:/api/v1/wallet/create/{"password":"enter your password","public_key":"a09111a1-a557-5b69-a94c-b7b291abbcc0"}
```sh
Responce:

{
"status": "success",
"keystore": "{\"address\": \"b84ddbf0cf9d1470e63adc5861353e576a3ee561\", \"crypto\": {\"cipher\": \"aes-128-ctr\", \"cipherparams\": {\"iv\": \"34065716cb2c5b5cefc0e4b6b668bb1d\"}, \"ciphertext\": \"ca5971143079eebbd55439641851e93b537c7f63615f281193ba8fab8e3e54f3\", \"kdf\": \"pbkdf2\", \"kdfparams\": {\"c\": 1000000, \"dklen\": 32, \"prf\": \"hmac-sha256\", \"salt\": \"ad4516e578c6188b162ba6a64c8ecf77\"}, \"mac\": \"3516439a863354be365d1200f53db92fef0b26dbd0c13fedaf715443217ecd92\"}, \"id\": \"b0f49063-13f7-44f4-9456-9c12b225540f\", \"version\": 3}"
}
```
# Send ATP
    Request:api/v1/wallet/importPk/{"privateKey":"enter your privivate key","public_key":"a09111a1-a557-5b69-a94c-b7b291abbcc0"}
```sh
Responce:

{"status": "error", "message": "does not match"}
or
{"status": "success", "address": "publicKey"}
or
{"status": "error", "error": "public key fail"}
```

# Check Tx status
    Request: /api/v1/wallet/txHash/{"txHash":"0xbb915b9a5a2b3e3f75e9ba6633d4f3345692474ae49580416b2b4c4c748dbf39","public_key":"a09111a1-a557-5b69-a94c-b7b291abbcc0"}
```sh
Responce:

{
"status": "success",
"tx_hash": "0xbb915b9a5a2b3e3f75e9ba6633d4f3345692474ae49580416b2b4c4c748dbf39",
"from": "0x38C1E1204C10C8be90ecA671Da8Ea8a9AEb16031",
"to": "0x4615F4FD7DCe26C36F4d1c392E7FC81FC07f5234",
"nonce": "117",
"gas_limit": "57828",
"gas_price": "29000000000",
"value": "0"
}
```
# Send BET2R 
    Request: api/v1/wallet/sendBet/{"public_key":"a09111a1-a557-5b69-a94c-b7b291abbcc0", "deposit_money":"0.000485", "resoult":"true", "time":"2019-02-19T06:11:00.000Z", "multiply_bet":"2"}

```sh
Responce:

{
"betting_list": "["address": "b84ddbf0cf9d1470e63adc5861353e576a3ee561", "deposit_amount":"0.000485"]",
"winning_resoult": "["address": "b84ddbf0cf9d1470e63adc5861353e576a3ee561", "winning_amount":"0.000999"]"
}
```
# Check BET Tx status
   Request:

```sh
Responce:
```

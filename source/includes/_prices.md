# Simulação

## Realizar uma simulação

```shell
curl --request POST \
  --url http://<url>/v1/prices \
  --header 'Authorization: Bearer <TOKEN>' \
  --header 'Content-Type: application/json' \
  --data '{
	"product_id": "SKU_DIGITAL_PRODUCT_LEADERSHIP",
	"discount": 0
}'
```

> Resposta:

```json
[
	{
		"installments": 13,
		"extended_installments": 15,
		"total_extended_amount": 9035,
		"amounts": [
			{
				"amount_cents": 10000,
				"description": "course_price",
				"extended_amount_cents_without_discount": 9035,
				"extended_amount_cents": 9035,
				"extended_installments": 15,
				"installments": 13
			}
		]
	},
	{
		"installments": 13,
		"extended_installments": 18,
		"total_extended_amount": 8036,
		"amounts": [
			{
				"amount_cents": 10000,
				"description": "course_price",
				"extended_amount_cents_without_discount": 8036,
				"extended_amount_cents": 8036,
				"extended_installments": 18,
				"installments": 13
			}
		]
	},
	{
		"installments": 13,
		"extended_installments": 24,
		"total_extended_amount": 6253,
		"amounts": [
			{
				"amount_cents": 10000,
				"description": "course_price",
				"extended_amount_cents_without_discount": 6253,
				"extended_amount_cents": 6253,
				"extended_installments": 24,
				"installments": 13
			}
		]
	}
]
```

Esse endpoint vai realizar a simulação de acordo com as configurações e taxas informadas no seu cadastro junto a Lia.

### HTTP Request

`GET http://<url>/v1/prices`

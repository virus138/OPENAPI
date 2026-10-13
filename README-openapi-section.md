## OpenAPI specification

An OpenAPI 3.0 description of the Shoonya REST API (OAuth) is available in two formats:

| Format | Link |
|---|---|
| YAML | [`openapi/shoonya-openapi.yaml`](openapi/shoonya-openapi.yaml) |
| JSON | [`openapi/shoonya-openapi.json`](openapi/shoonya-openapi.json) |

Raw URL for tools:
`https://raw.githubusercontent.com/Shoonya-API-OAuth-Python/Shoonya_API_OAuth/main/openapi/shoonya-openapi.yaml`

### Use it

- **View it:** paste the raw URL into [editor.swagger.io](https://editor.swagger.io) (File → Import URL).
- **Postman:** Import → Link → paste the raw URL.
- **Generate a client:**
  `npx @openapitools/openapi-generator-cli generate -i openapi/shoonya-openapi.yaml -g python -o ./client`
- **Python models only:**
  `pip install datamodel-code-generator` then
  `datamodel-codegen --input openapi/shoonya-openapi.yaml --input-file-type openapi --output models.py`

### Request format

Every endpoint is a `POST` with `Authorization: Bearer <access_token>`. The body is a single form field,
`jData`, containing the request model as a compact JSON string. Each model is named `<Operation>Request`
in the spec (for example `PlaceOrderRequest`). Check `stat` in every response: `Ok` or `Not_Ok` (with `emsg`).

See [`openapi/CHANGELOG.md`](openapi/CHANGELOG.md) for versions. The official documentation is at
https://shoonya.com/api-documentation.

# Changelog

All notable changes to `shoonya-openapi.yaml` / `shoonya-openapi.json` are listed here.
Versioning follows `info.version` in the spec.

## 1.0.0

- Initial release, built from the `NorenRESTAPI_oAuth` Postman collection and the public Shoonya API documentation.
- 51 operations: the 50 requests from the Postman collection plus `Logout`.
- Gateway: `https://api.shoonya.com/NorenWClientAPI`.
- Typed request models (`<Operation>Request`) for every operation. 20 are fully documented; 31 are tagged
  `x-needs-review` and list only the fields shown in the Postman collection.
- Typed response models for orders, trades, positions, holdings, limits, quotes, security info, scrip search,
  SPAN calculator and option greeks.

# OFMAPI Postman collection

A Postman collection for the [OFMAPI](https://ofmapi.com) OnlyFans API,
generated from the public OpenAPI 3.1 spec at
[ofmapi.com/openapi.json](https://ofmapi.com/openapi.json). Every operation in
the spec is included, grouped into folders by tag.

## Files

| File | What it is |
|---|---|
| `collection.json` | The collection. Uses `{{baseUrl}}` and sends `{{apiKey}}` as a Bearer token on every request. |
| `ofmapi.postman_environment.json` | An environment with `baseUrl` preset to `https://api.ofmapi.com` and an empty `apiKey`. |

## Use it

1. In Postman choose **File → Import** and drop both files.
2. Create an API key at [app.ofmapi.com/api-keys](https://app.ofmapi.com/api-keys)
   (free during the public Beta, no card required).
3. Select the **OFMAPI Production** environment and paste the `ofmapi_...`
   value into `apiKey`.
4. Open **Accounts → List Accounts** and send.

Once the environment holds a real key, keep the file out of shared
workspaces and version control.

## Regenerate

```bash
npx openapi-to-postmanv2 -s https://ofmapi.com/openapi.json -o collection.json -p -O folderStrategy=Tags
```

The repository is regenerated when the spec changes.

## Documentation

- Postman guide: https://ofmapi.com/docs/integrations/postman
- Interactive API reference (no login): https://ofmapi.com/docs/api
- Quickstart: https://ofmapi.com/docs/quickstart
- Rate limits and Beta usage limits: https://ofmapi.com/docs/rate-limits
- Status: https://ofmapi.com/status

## License

MIT. See [LICENSE](LICENSE).

---

OFMAPI is an independent organisation, not affiliated with OnlyFans.com or
Fenix International Limited. "OnlyFans" is a registered trademark of Fenix
International Limited. Postman is a trademark of Postman, Inc.

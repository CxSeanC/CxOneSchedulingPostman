# Final Schedules API

This repository contains a Postman collection for interacting with the Final Schedules API. The collection supports authentication via OAuth 2.0 and requires environment variables to be set up for seamless use.

## Prerequisites

- [Postman](https://www.postman.com/) installed
- Client credentials (Client ID & Client Secret) for OAuth 2.0 authentication
- Access to the Final Schedules API

## Environment Variables

The following environment variables should be configured in Postman:

| Variable       | Description |
|---------------|-------------|
| `base_url`    | The base URL of the API (e.g., `https://api.example.com`) |
| `client_id`   | OAuth 2.0 Client ID |
| `client_secret` | OAuth 2.0 Client Secret |
| `access_token` | Auto-populated Bearer Token after authentication |
| `id`          | Project ID (used in API requests) |

Ensure these variables are set up in a Postman environment before executing the requests.

## Authentication Process

This API uses OAuth 2.0 for authentication. The access token is obtained via the "Get Bearer Token" request in the collection.

### Steps to Authenticate:
1. Run the **Get Bearer Token** request in Postman.
2. The `access_token` variable will be automatically populated.
3. Subsequent API requests will use the `access_token` in the `Authorization` header (`Bearer {{access_token}}`).

## Usage

1. Import the Postman collection (`Final Schedules API.postman_collection.json`) into Postman.
2. Configure the environment variables in Postman.
3. Authenticate by running the "Get Bearer Token" request.
4. Execute API requests using the populated access token.

## Notes

- No API key is required for authentication; OAuth 2.0 with Client ID and Client Secret is used.
- Ensure your credentials are securely stored and not shared.
- If the token expires, rerun the "Get Bearer Token" request to refresh it.

## Troubleshooting

- If requests fail with `401 Unauthorized`, verify that:
  - The `access_token` is populated in the environment.
  - The Client ID and Client Secret are correct.
  - The OAuth 2.0 authentication endpoint is reachable.
- If issues persist, regenerate client credentials or check API access permissions.

## Contribution

Feel free to contribute by submitting a pull request or reporting issues.

## License

This project is licensed under the MIT License.

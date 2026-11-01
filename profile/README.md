# Cadenya

Cadenya is an API-first agent runtime. It runs the agent loop for your app as a hosted service. Your agents call tools from an OpenAPI document, an MCP server or your own HTTP endpoints. A person approves the calls that need it, and every step streams to your app or to an embeddable chat widget.

## Start here

1. Create a free account at https://app.cadenya.com/signup. The Free plan needs no card.
2. Copy your API key from https://app.cadenya.com/account/apiKeys and set it as `CADENYA_API_KEY`.
3. Install the CLI, sign in and pick a workspace:

   ```sh
   brew install cadenya/tools/cadenya   # Windows: choco install cadenya
   cadenya auth login                   # approve the one-time code in your browser
   cadenya workspaces list              # set one as CADENYA_WORKSPACE_ID
   ```

4. Describe your agent, its tool sets and its variations as YAML files in `.cadenya/` next to a `cadenya.yaml`, then run `cadenya config apply`.

The docs are at https://cadenya.com/docs. To give your coding agent Cadenya's skills, run `npx skills add https://cadenya.com/docs`.

## SDKs

| Language | Install | Repository |
| --- | --- | --- |
| TypeScript | `npm install @cadenya/cadenya` | [cadenya-typescript](https://github.com/cadenya/cadenya-typescript) |
| Python | `pip install cadenya` | [cadenya-python](https://github.com/cadenya/cadenya-python) |
| Ruby | `gem install cadenya` | [cadenya-ruby](https://github.com/cadenya/cadenya-ruby) |
| Go | `go get go.cadenya.com/cadenya-go` | [cadenya-go](https://github.com/cadenya/cadenya-go) |

## CLI and configuration

- [cadenya-cli](https://github.com/cadenya/cadenya-cli) is the `cadenya` CLI. It signs you in with `cadenya auth login`, runs the API from your terminal, and applies your `.cadenya/` files with `cadenya config apply`.
- [cadenya-config-loader](https://github.com/cadenya/cadenya-config-loader) is a GitHub Action that validates, plans and applies the same files in CI.
- [cadenya-openapi](https://github.com/cadenya/cadenya-openapi) points to the OpenAPI spec, which is live at https://openapi.cadenya.com/api-spec.yml.

## Widgets

- [widgets-sdk](https://github.com/cadenya/widgets-sdk) is the TypeScript client for Cadenya Widgets, which put a Cadenya agent in your web app (`npm install @cadenya/widgets`).
- [widgets-ui-react](https://github.com/cadenya/widgets-ui-react) is the React UI kit for it, with conversations, streaming replies and tool approvals (`npm install @cadenya/widgets-ui-react`).

## Examples

- [examples-slacktacular](https://github.com/cadenya/examples-slacktacular) is a Slack app that runs Cadenya agents and shows tool approvals in the thread.
- [cadenyaception-widgets-sandbox](https://github.com/cadenya/cadenyaception-widgets-sandbox) holds three widget demos: a travel concierge, chess and a diagram builder. Try them at https://widgets-demo.cadenya.com.

## More open source

- [redwood](https://github.com/cadenya/redwood) generates the SDKs from the OpenAPI spec.
- [mcp-grpc-gateway](https://github.com/cadenya/mcp-grpc-gateway) exposes gRPC services as MCP tools.
- [prorate](https://github.com/cadenya/prorate) adds rate limits to gRPC services from proto annotations.
- [protoc-gen-go-dbtypes](https://github.com/cadenya/protoc-gen-go-dbtypes) generates Go types that store protobuf messages in a database.

## Learn more

- [Docs](https://cadenya.com/docs) and the [API reference](https://cadenya.com/docs/api-reference)
- [Pricing](https://cadenya.com/pricing) for the Free, Growth and Enterprise plans
- [Handwritten](https://cadenya.com/handwritten), Robert Ross's posts on how Cadenya is built
- [Articles](https://cadenya.com/other-content) on agent frameworks, durable execution and approvals

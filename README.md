# Release Information

- **Version**: 2.0.0

- **Certified**: Yes

- **Publisher**: Fortinet

- **Scope**: NA

- **Verified with Models**: Fortinet FortiAI (AI model Medium)

- [Release Notes](./release_notes.md)

# Chat Assistant

A cybersecurity conversational agent that interprets SOC analyst queries and provides accurate, context-driven responses.

## Installation

This agent installs along with the FortiAI solution pack.

## Configuration

The Chat Assistant Agent ships with a configuration that has access to all shipped MCP servers. For custom configuration, refer to the *Configuration* section of the [FortiAI](https://github.com/fortinet-fortisoar/solution-pack-fortinet-advisor) solution pack documentation.

> [!Note]
> Refer to [Configuring MCP Servers](https://docs.fortinet.com/document/fortisoar/8.0.0/administration-guide/823139/mcp-servers#Configure_MCP_Servers) on FortiSOAR platform documentation for information on configuring a custom MCP server.

### Prerequisites

The following prerequisites must be met before using this agent:

- The FortiAI solution pack must be installed and configured with the Fortinet FortiAI connector.

  - To configure the FortiAI solution pack, refer to the [FortiAI](https://github.com/fortinet-fortisoar/solution-pack-fortinet-advisor/) solution pack documentation.
  - To configure the Fortinet FortiAI connector, refer to the [Fortinet FortiAI](https://docs.fortinet.com/fortisoar/connectors/fortinet-fortiai) connector documentation.

> [!Note]
> The FortiAI solution pack and the Fortinet FortiAI connector are preconfigured out-of-the-box with FortiSOAR `v8.0.1` and later.

## Input Parameters

The input must be provided as a JSON object.

| Parameter              | Description                                                                                                                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message`              | The user input message to be processed by the conversation agent.                                                                                                                                                                            |
| `context`              | The user's page context. When the user is on a record page, set `context.record` to `{module, id}` so the agent preloads the record, its module schema, and the modules list, avoiding the `get_modules`, `get_module_schema`, and `query_records` discovery loop. |
| `previous_response_id` | The ID of the previous response (if applicable).                                                                                                                                                                                             |

## Response

The output is returned as a JSON object.

| Parameter | Description                                        |
|-----------|----------------------------------------------------|
| `status`  | Indicates if the request was successful or failed. |
| `data`    | The response returned by the agent.                |
| `message` | A message describing the result.                   |
# Release Information

- **Version**: 1.0.0

- **Certified**: Yes

- **Publisher**: Fortinet

- **Scope**: NA

- **Verified with Models**: Fortinet FortiAI (AI model Medium)

# Chat Assistant

A cybersecurity conversational agent that interprets SOC analyst queries and provides accurate, context-driven responses.

## Installation

This agent installs along with the FortiAI solution pack.

## Configuration

**Required MCP Servers**: NA

### Prerequisites

- The FortiAI solution pack must be installed and configured with the Fortinet FortiAI connector.

  - To configure the FortiAI solution pack, refer to the [FortiAI](https://github.com/fortinet-fortisoar/solution-pack-fortinet-advisor/) solution pack documentation.
  - To configure the Fortinet FortiAI connector, refer to the [Fortinet FortiAI](https://docs.fortinet.com/fortisoar/connectors/fortinet-fortiai) connector documentation.

> [!Note]
>
> FortiAI solution pack and Fortinet FortiAI connector are preconfigured out-of-the-box with FortiSOAR `v8.0.0`.
> 


## Input Parameters

The input must be provided as a JSON object.

| Parameter         | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| `messages`        | List of user input messages to be processed by the conversation agent.      |
| `insight_id`      | Insight id in whose context to answer the query.                            |
| `message_history` | Historical conversation messages providing context for the current request. |

## Response

The output is returned as a JSON object.

| Parameter | Description                                        |
|-----------|----------------------------------------------------|
| `status`  | Indicates if the request was successful or failed. |
| `data`    | The response returned by the agent.                |
| `message` | A message describing the result.                   |

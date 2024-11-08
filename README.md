🏈 Fantasy Football Agent is a production ready multi-agent collaboration framework that enables you to orchestrate many agents to work collaboratively at scale to automate your fantasy football activities. 

----

## Requirements
- `python3.10` or above!
- `$ pip install -U swarms` And, don't forget to install swarms!
- `.env` file with API keys from your providers like `OPENAI_API_KEY`, `ANTHROPIC_API_KEY`
-  Set an `.env` Variable with your desired workspace dir: `WORKSPACE_DIR="agent_workspace"` or do it in your terminal with `export WORKSPACE_DIR="agent_workspace"`
-  Finally, `swarms onboarding` to get you started.

## Onboarding
Refer to our documentation for production grade implementation details.


| Section              | Links                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------|
| Installation    | [Installation](https://docs.swarms.world/en/latest/swarms/install/install/)                                                            |
| Quickstart | [Get Started](https://docs.swarms.world/en/latest/swarms/install/quickstart/)                                                 |
| Agent Internal Mechanisms | [Agent Architecture](https://docs.swarms.world/en/latest/swarms/framework/agents_explained/)                                                 |
| Agent API | [Agent API](https://docs.swarms.world/en/latest/swarms/structs/agent/)                                                 |
| Integrating External Agents Griptape, Autogen, etc | [Integrating External APIs](https://docs.swarms.world/en/latest/swarms/agents/external_party_agents/)                                                 |
| Creating Agents from YAML | [Creating Agents from YAML](https://docs.swarms.world/en/latest/swarms/agents/create_agents_yaml/)                                                 |
| Why You Need Swarms | [Why MultiAgent Collaboration is Necessary](https://docs.swarms.world/en/latest/swarms/concept/why/)                                                 |
| Swarm Architectures Analysis | [Swarm Architectures](https://docs.swarms.world/en/latest/swarms/concept/swarm_architectures/)                                                 |
| Choosing the Right Swarm for Your Business Problem¶ | [CLICK HERE](https://docs.swarms.world/en/latest/swarms/concept/swarm_architectures/)                                                 |
| AgentRearrange Docs| [CLICK HERE](https://docs.swarms.world/en/latest/swarms/structs/agent_rearrange/)                                                 |


## Install 💻

```bash
$ pip3 install -U swarms
```


## Onboarding

Now that you have downloaded swarms with `pip3 install -U swarms`, we get access to the `CLI`. Get Onboarded with CLI Now with:

```bash
swarms onboarding
```

You can also run this command for help:

```bash
swarms help
```

For more documentation on the CLI [CLICK HERE](https://docs.swarms.world/en/latest/swarms/cli/main/)

---

## `Agent` Class
The `Agent` class is a fundamental component of the Swarms framework, designed to execute tasks autonomously. It fuses llms, tools and long-term memory capabilities to create a full stack agent. The `Agent` class is highly customizable, allowing for fine-grained control over its behavior and interactions.

### `run` Method
The `run` method is the primary entry point for executing tasks with an `Agent` instance. It accepts a task string as the main input task and processes it according to the agent's configuration. And, it can also accept an `img` parameter such as `img="image_filepath.png` to process images if you have a VLM


### Settings and Customization
The `Agent` class offers a range of settings to tailor its behavior to specific needs. Some key settings include:

| Setting | Description | Default Value |
| --- | --- | --- |
| `agent_name` | The name of the agent. | "DefaultAgent" |
| `system_prompt` | The system prompt to use for the agent. | "Default system prompt." |
| `llm` | The language model to use for processing tasks. | `OpenAIChat` instance |
| `max_loops` | The maximum number of loops to execute for a task. | 1 |
| `autosave` | Enables or disables autosaving of the agent's state. | False |
| `dashboard` | Enables or disables the dashboard for the agent. | False |
| `verbose` | Controls the verbosity of the agent's output. | False |
| `dynamic_temperature_enabled` | Enables or disables dynamic temperature adjustment for the language model. | False |
| `saved_state_path` | The path to save the agent's state. | "agent_state.json" |
| `user_name` | The username associated with the agent. | "default_user" |
| `retry_attempts` | The number of retry attempts for failed tasks. | 1 |
| `context_length` | The maximum length of the context to consider for tasks. | 200000 |
| `return_step_meta` | Controls whether to return step metadata in the output. | False |
| `output_type` | The type of output to return (e.g., "json", "string"). | "string" |


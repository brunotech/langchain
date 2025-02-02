# SerpAPI

This page covers how to use the SerpAPI search APIs within LangChain.
It is broken into two parts: installation and setup, and then references to the specific SerpAPI wrapper.

## Installation and Setup
- Install requirements with `pip install google-search-results`
- Get a SerpAPI api key and either set it as an environment variable (`SERPAPI_API_KEY`)
- Optional, if you are using a proxy, set environment variable (`SERPAPI_BASE_URL`) or pass it to the LLM constructor to your proxy url.

## Wrappers

### Utility

There exists a SerpAPI utility which wraps this API. To import this utility:

```python
from langchain.utilities import SerpAPIWrapper
```

For a more detailed walkthrough of this wrapper, see [this notebook](../modules/agents/tools/examples/serpapi.ipynb).

### Tool

You can also easily load this wrapper as a Tool (to use with an Agent).
You can do this with:
```python
from langchain.agents import load_tools
tools = load_tools(["serpapi"])
```

For more information on this, see [this page](../modules/agents/tools/getting_started.md)

<h1 align="center">
 </picture>
 </a>
 <br>
 Strait
</h1>
<p align="center">
:wrench: Test and experiment with prompts, LLMs, and vector databases for Project Strait. :hammer:
<p align="center">
</p>


Welcome to `Project Strait` created by Ben Ahmed & Morgan Swan. This repo offers a set of open-source, self-hostable tools for experimenting with, testing, and evaluating LLMs, vector databases, and prompts. The core idea is to leverage Multiple LLM based Models in assistance for Psychiatric Professionals too reach a wider audience and customer base. 

this id for ingternal provate testing only: --------
In just a few lines of codes, you can test your prompts and parameters across different models. You can even evaluate the retrieval accuracy of vector databases.

```python
prompts = ["Tell me a joke.", "Is 17077 a prime number?"]
models = ["gpt-3.5-turbo", "gpt-4"]
temperatures = [0.0]
openai_experiment = OpenAIChatExperiment(models, prompts, temperature=temperatures)
openai_experiment.run()
openai_experiment.visualize()
```


![image](img/demo.gif)


## Quickstart

To install `prompttools`, you can use `pip`:

```
pip install prompttools
```

You can run a simple example of a `prompttools` locally with the following

```
git clone https://github.com/hegelai/prompttools.git
cd prompttools && jupyter notebook examples/notebooks/OpenAIChatExperiment.ipynb
```

## Project Strait Testing Playground

<p align="center">
  <img src="img/playground.gif" width="1000" height="500">
</p>

If you want to interact with `prompttools` using our playground interface, you can launch it with the following commands.

First, install prompttools:

```
pip install prompttools
```

Then, clone the git repo and launch the streamlit app:

```
git clone https://github.com/hegelai/prompttools.git
cd prompttools && streamlit run prompttools/playground/playground.py
```

You can also access a hosted version of the playground on the [Streamlit Community Cloud](https://prompttools.streamlit.app/).

> Note: The hosted version does not support LlamaCpp

## Documentation

Our [documentation website](https://prompttools.readthedocs.io/en/latest/index.html) contains the full API reference
and more description of individual components. Check it out!

## Supported Integrations

Here is a list of APIs that we support with our experiments:

LLMs
- OpenAI (Completion, ChatCompletion, Fine-tuned models) - **Supported**
- LLaMA.Cpp (LLaMA 1, LLaMA 2) - **Supported**
- HuggingFace (Hub API, Inference Endpoints) - **Supported**
- Anthropic - **Supported**
- Google PaLM - **Supported**
- Google Vertex AI - **Supported**
- Azure OpenAI Service - **Supported**
- Replicate - **Supported**
- Ollama - _In Progress_

Vector Databases and Data Utility
- Chroma - **Supported**
- Weaviate - **Supported**
- Qdrant - **Supported**
- LanceDB - **Supported**
- Milvus - Exploratory
- Pinecone - **Supported**
- Epsilla - _In Progress_

Frameworks
- LangChain - **Supported**
- MindsDB - **Supported**
- LlamaIndex - Exploratory

## Frequently Asked Questions (FAQs)

1. Will this library forward my LLM calls to a server before sending it to OpenAI, Anthropic, and etc.?
    - No, the source code will be executed on your machine. Any call to LLM APIs will be directly executed from your machine without any forwarding.

2. Does `prompttools` store my API keys or LLM inputs and outputs to a server?
    - No, all of those data stay on your local machine. We do not collect any PII (personally identifiable information).

3. How do I persist my results?
   -  To persist the results of your tests and experiments, you can export your `Experiment` with the methods `to_csv`,
      `to_json`, `to_lora_json`, or `to_mongo_db`. We are building more persistence features and we will be happy to further discuss your use cases, pain points, and what export
      options may be useful for you.


We welcome PRs and suggestions! Don't hesitate to open a PR/issue or to reach out to us [via email](mailto:team@hegel-ai.com).
Please have a look at our [contribution guide](CONTRIBUTING.md) and
["Help Wanted" issues](https://github.com/hegelai/prompttools/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22) to get started!

## Usage and Feedback

We will be delighted to work with early adopters to shape our designs. Please reach out to us [via email](mailto:A.Ben.Ahmed@gmail.com) if you're
interested in using this tooling for your Practice or have any feedback.

## License

We will be gradually releasing more components to the open-source community. The current license can be found in the  [LICENSE](LICENSE) file. If there is any concern, please [contact us](mailto:eam@hegel-ai.com) and we will be happy to work with you.

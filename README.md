This is the [repository](https://github.com/jcheng5/SciPy-2025) for the SciPy 2025 talk "Keeping LLMs in Their Lane: Focused AI for Data Science and Research" by Joe Cheng.

## Helpful links

* Get started by watching ["Harnessing LLMs for Data Analysis"](https://www.youtube.com/watch?v=owDd1CJ17uQ) (YouTube)
* [Chatlas](https://posit-dev.github.io/chatlas/): Easily call LLMs from Python
* [Shiny](https://shiny.posit.co/py/): Web framework designed for Python data folks
* [Querychat](https://posit-dev.github.io/querychat/): Enhance Shiny data dashboards with LLMs that speak SQL

## Demo: Natural language filtering of eBird data dashboard

To run this demo, you will need an Anthropic API key; you can get one via the [Anthropic Console](https://console.anthropic.com/) (requires signup and credit card).

Create a file named `.env` in the root of this repository, and add your API key like this:

```bash
ANTHROPIC_API_KEY=your_api_key_here
```

Then, you can run the demo using the following command:

```bash
uv run shiny run --launch-browser
```

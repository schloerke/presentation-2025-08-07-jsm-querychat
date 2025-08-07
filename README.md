# `{querychat}`: Natural language interfaces for interactive data graphics in Shiny

## Helpful links

* [Slides](https://schloerke.com/presentation-2025-08-07-jsm-querychat/)
* Get started by watching ["Harnessing LLMs for Data Analysis"](https://www.youtube.com/watch?v=owDd1CJ17uQ) (YouTube)
* [Ellmer](https://ellmer.tidyverse.org/): Easily call LLMs from R
* [Chatlas](https://posit-dev.github.io/chatlas/): Easily call LLMs from Python
* [Shiny](https://shiny.posit.co/py/): Web framework designed for Python data folks
* [Querychat](https://posit-dev.github.io/querychat/): Enhance Shiny data dashboards with LLMs that speak SQL

## Demo: Natural language filtering of eBird data dashboard

To run this demo, you will need an Anthropic API key; you can get one via the [Anthropic Console](https://console.anthropic.com/) (requires signup and credit card).

Create a file named `.env` in the root of this repository, and add your API key like this:

```bash
ANTHROPIC_API_KEY=your_api_key_here
```

Then, you can install the dependencies and run the demo using the following command:

```bash
uv run shiny run --launch-browser
```


------------------------

## Abstract

Interactive data graphics have long empowered users to explore complex datasets through visual manipulation. However, there are barriers to entry for complex interactions. The Shiny Team presents `{querychat}`, a multilingual package that enables natural language interaction with data visualizations in both R and Python Shiny applications. Users can pose questions such as "Show only data from 2008 with highway MPG greater than 30" or "What's the average city MPG for SUVs vs compact cars?" and see immediate visual results.

`{querychat}` works by translating natural language into SQL queries that filter or transform data frames, making the resulting data available as reactive objects. This approach enhances reliability (LLMs excel at SQL generation), transparency (SQL queries can be displayed to users), and reproducibility (queries can be saved and reused). Shiny's reactive programming model allows for seamless propagation of LLM-generated transformations through its dashboard visualization pipelines. The same properties that make Shiny effective for rapid prototyping (event-driven architecture, reactive expressions, and component model) create a natural framework for embedding LLM capabilities that dynamically respond to a user's conversations.

## Introduction

Dr. Barret Schloerke is a Shiny Software Engineer at Posit who specializes in developing interactive web applications and data visualization tools. He has significantly contributed to many open-source R packages including {shiny}, {shinytest2}, {plumber}, and {reactlog}. In addition to his work in R, Barret also works on Shiny for Python, implementing its testing tools, bookmarking, and interactive data frame experience. Blending his extensive expertise in statistical computing, large data visualization, and automated testing systems, Barret has been able to speed up Shiny app development, allowing developers to focus on building robust and reproducible applications.

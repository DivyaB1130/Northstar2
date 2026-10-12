# NorthStar* (filter prototype)

An earlier, filter-based version of [NorthStar](https://github.com/DivyaB1130/NorthStar1), built during Kode With Klossy's 2026 AI & Machine Learning program.

Choose where you're eating and what you're in the mood for, and NorthStar returns up to ten matching restaurants:

- **Location:** a city, or a city and state (full state names like "New Jersey" are converted to "NJ").
- **Preferences:** meal, price range, cuisine and dining vibe.
- **Dietary needs:** vegetarian, vegan, halal and gluten-free.

Each restaurant is stored as a single text document combining its location, food types, Yelp rating, price tier and excerpts from customer reviews. Filters that would leave no results are relaxed instead of showing an empty page, and matches are shuffled so results stay fresh.

The deployed version became a chatbot that pulls live data: see [NorthStar1](https://github.com/DivyaB1130/NorthStar1) and [try it on Hugging Face](https://huggingface.co/spaces/kode-with-klossy/4.3-groupC4-capstone).

## Running it

```bash
pip install gradio pandas pyarrow
python app.py
```

The app expects `northstar_rag_dataset.parquet` next to `app.py`. It is built from the Yelp Open Dataset, which can't be redistributed, so it isn't included here.

Built with Python, pandas and Gradio.

# Bechdel Test Prediction

This project explores which types of films are more likely to pass the [Bechdel Test](https://bechdeltest.com/), a simple measure of female representation in film. By analyzing metadata from IMDb and user-curated Bechdel scores, the project builds a logistic regression model to identify factors associated with a film's likelihood of passing the test.

> **Bechdel Test Criteria**  
> 1. The movie must have at least two named women,  
> 2. who talk to each other,  
> 3. about something other than a man.  

## Data Sources

- [IMDb API](https://developer.imdb.com/documentation/api-documentation/)
- [BechdelTest.com API](https://bechdeltest.com/api/v1/doc)
- Data originally sourced via [TidyTuesday Week 11, 2021](https://github.com/rfordatascience/tidytuesday/tree/master/data/2021/2021-03-09)
- 1,794 films (up to 2020 Bechdel scores and 2013 IMDb metadata)

## Key Findings

- **Release year** is positively associated with passing the Bechdel test, suggesting slow but steady improvement in gender representation.
- A better **Metascore** (critic reviews) increases the odds of passing, while **IMDb rating** (user ratings) is negatively associated, highlighting a possible gap between critical and popular reception.
- Higher **budgets** and **IMDb vote counts** are linked to lower odds of passing, whereas **genre score**, **runtime**, and **international gross** correlate with better representation.
- The final logistic model achieves an **AUC of 0.707** and **67% accuracy**—modest but informative for inference purposes.

## Limitations

- **Selection bias**: The dataset relies on user submissions to BechdelTest.com, possibly skewing toward well-known or culturally salient films.
- **Focus on inference over prediction**: Logistic regression was chosen for interpretability; ensemble methods might offer stronger predictive performance.
- **Room for future work**: Incorporating unstructured metadata (e.g., plot summaries, director names) with NLP or LLMs could provide deeper insights into gender dynamics in film.

## Acknowledgements

This project was originally developed as an assignment for a graduate-level linear models course (STAT 230A) at UC Berkeley. Special thanks to the course staff for their guidance and feedback.

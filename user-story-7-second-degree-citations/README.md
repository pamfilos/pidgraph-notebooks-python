## [FREYA](https://www.project-freya.eu/en) WP2 [User Story 7]( https://www.pidforum.org/t/pid-graph-graphql-example-second-degree-citations/939): As a data center, I want to see the citations of publications that use my repository for the underlying data, so that I can demonstrate the impact of our repository. 
                   
### Jupyter Notebook:
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/datacite/pidgraph-notebooks-python/master?user-story-7-second-degree-citations%2Fpy-second-degree-citations-output.ipynb)

### Examples of GraphQL Queries Used:
* Retrieve citations of the dataset https://doi.org/10.5061/dryad.234 

```
{
  dataset(id: "https://doi.org/10.5061/dryad.234") {
    id
    titles {
      title
    }
    citationCount
    citations {
      nodes {
        id
        publisher
        titles {
          title
        }
        citationCount
      }
    }
  }
}
```
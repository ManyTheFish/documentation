# Stats

`Stats` gives extended information and metrics about indexes and the MeiliSearch database.

## Get stat of an index

<RouteHighlighter method="GET" route="/indexes/:index_uid/stats"/>

Get stats of an index.

#### Path variables

| Variable      | Description   |
| ------------- | ------------- |
| **index_uid** | The index UID |

### Example

<CodeSamples id="get_index_stats_1" />

#### Response: `200 Ok`

```json
{
  "numberOfDocuments": 19654,
  "isIndexing": false,
  "fieldDistribution": {
    "poster": 19654,
    "release_date": 19654,
    "title": 19654,
    "id": 19654,
    "overview": 19654
  }
}
```

## Get stats of all indexes

<RouteHighlighter method="GET" route="/stats"/>

Get stats of all indexes.

::: note
`databaseSize` is expressed in **bytes**.
:::

### Example

<CodeSamples id="get_indexes_stats_1" />

#### Response: `200 Ok`

```json
{
  "databaseSize": 447819776,
  "lastUpdate": "2019-11-15T11:15:22.092896Z",
  "indexes": {
    "movies": {
      "numberOfDocuments": 19654,
      "isIndexing": false,
      "fieldDistribution": {
        "poster": 19654,
        "overview": 19654,
        "title": 19654,
        "id": 19654,
        "release_date": 19654
      }
    },
    "rangemovies": {
      "numberOfDocuments": 19654,
      "isIndexing": false,
      "fieldDistribution": {
        "overview": 19654,
        "id": 19654,
        "title": 19654
      }
    }
  }
}
```

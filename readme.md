<h2 style="text-align:center;"> 2019 Covid-19 California County Data API</h2>

<hr>

### COVID-19 California County Cases API
This API collects California counties' data with confirmed cases and deaths number since March 16th.

Using axios
```js
import axios from 'axios';
axios.get('https://amazingshellyyy.com/covid19-CA/countyTimeseries.json')
      .then(res => {
        console.log('covid CA County data',res.data)
      })
      .catch(err => {
        console.log(err)
      })
```

The JSON contains timeStamp (stored in milliseconds) and Array of counties'case with an object of each county and its name, cases, and deaths.

```
[
  {
    "timeStamp": 1584367447000,
    "data": [
      {
        "county": "Santa Clara",
        "case": 114,
        "death": 2
      },
      {
        "county": "Los Angeles",
        "case": 69,
        "death": 1
      },
      {
        "county": "San Francisco",
        "case": 37,
        "death": 0
      },
      ...
    ]
  }
  ...
}
```

*Data is updated four times daily at 00:30, 07:30, 13:30 and 23:30

#### resource
 https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_California

# business-hours.js
Business hours javascript lib

[![Travis](https://img.shields.io/travis/littletower/business-hours.js.svg?style=flat-square)]()
[![Codecov](https://img.shields.io/codecov/c/github/littletower/business-hours.js.svg?style=flat-square)]()
[![npm](https://img.shields.io/npm/v/business-hours.js.svg?style=flat-square)]()

## Installation

Add the latest version of `business-hours.js` to your package.json:
```
npm install business-hours.js --save
```
or
```
yarn add business-hours.js
```

# Configuration

To get started, setup a JSON file where you define the business hours.

`0` stands for `Sunday`

`1` stands for `Monday` and so on.

You can have 1 to N `from/to` pairs per weekday. If on a given day you are closed, instead of a `from/to` pair, just put `closed`.

```json
{
  "0": [
    {
      "from": "10:00",
      "to": "13:30"
    },
    {
      "from": "17:00",
      "to": "20:00"
    },
    {
      "from": "21:00",
      "to": "24:00"
    }
  ],
  "1": [
    {
      "from": "10:00",
      "to": "13:30"
    },
    {
      "from": "18:00",
      "to": "22:00"
    }
  ],
  "2": "closed",
  "3": [
    {
      "from": "10:00",
      "to": "13:30"
    },
    {
      "from": "18:00",
      "to": "22:00"
    }
  ],
  "4": [
    {
      "from": "10:00",
      "to": "13:30"
    },
    {
      "from": "18:00",
      "to": "22:00"
    }
  ],
  "5": [
    {
      "from": "10:00",
      "to": "13:30"
    },
    {
      "from": "18:00",
      "to": "22:00"
    }
  ],
  "6": [
    {
      "from": "10:00",
      "to": "13:30"
    },
    {
      "from": "18:00",
      "to": "22:00"
    }
  ]
}
```

# Usage

First import the lib
```
import businessHours from "business-hours.js";
```
Then you have to initalize the lib with your business hours
```
businessHours.init(hoursJson);
```
`hoursJson` must be in JSON format. It could come from an external file
```
import hoursJson from "./hours.json";
```
or it could come from any other endpoind, as long as it's JSON.

# Example
Find an whole example in React here [here](example/)

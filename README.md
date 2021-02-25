Forked from https://github.com/Yevgenium/lovelace-weather-card-chart, with tweaks based on personal preferences:

![screenshot](https://i.imgur.com/vk98lqL.png)

## Configuration

Copy `weather-card-chart.js` from this repository into your `config/www` directory first (or add this repo as a custom HACS repository).

Add a reference to the copied file:
```yaml
# Example Lovelace UI config entry
resources:
- type: module
  url: /local/weather-card-chart.js
```
Then you can add the card to the view:
```yaml
# Example Lovelace UI config entry
  - type: 'custom:weather-card-chart'
    title: Weather
    weather: weather.openweathermap
```

#### Configuration variables:

| Name    | Optional | Description                                                                                        |
| ------- | -------- | -------------------------------------------------------------------------------------------------- |
| type    | **No**   | Should be `'custom:weather-card-chart'`                                                            |
| title   | **No**   | Card title                                                                                         |
| weather | **No**   | An entity_id with the `weather` domain                                                             |
| wind    | Yes      | Entity_id of the wind sensor. Show wind value from sensor instead                                  |
| temp    | Yes      | Entity_id of the temperature sensor. Show temperature value from sensor instead                    |
| mode    | Yes      | Default value: `daily`. Set mode to `hourly` to display hours instead weekdays on the chart        |

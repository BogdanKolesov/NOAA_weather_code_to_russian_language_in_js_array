# NOAA weather code

Источник: https://docs.synopticdata.com/services/weather-condition-codes

## На выходе

Сопоставленно в массив, объектов javascript, переведено на русский язык

### Пример использования в React

import { weatherCodeData } from '../../../data/weatherCodeData';

const [currentWeather, setCurrentWeather] = useState({});

    const findWeatherByCode = (code) => {
    	let result = weatherCodeData.find((weather) => Number(weather.code) === Number(code));
    	setCurrentWeather(result);
    };

return(
<NewsWeatherItem>
Явления: {currentWeather.description}
{currentWeather.note ? ` ${currentWeather.note}` : `}
{currentWeather.change ? currentWeather.change : `};
</NewsWeatherItem>
)

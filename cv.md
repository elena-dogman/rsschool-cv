# Elena Dogman 
## Junior Frontend Developer
---
### Contact information:
**E-mail:** elenadogman.gmail.com 

**Telegram:** @elenadogman

---
### Summary 
As a professional in the field of English education, I have dedicated my career to teaching English with a special focus on English for IT. My journey through the realm of language and technology sparked a profound interest in Frontend Development, igniting a passion for the craft. My desire to transition into the world of Frontend Development stems from the realization that it seamlessly combines my love for language and my enthusiasm for technology.

My background in education has equipped me with advanced studying skills, enabling me to quickly grasp and adapt to new concepts and technologies. This foundation, coupled with my innate interest in Frontend Development, positions me as a dedicated and capable person eager to contribute to the ever-evolving world of web design and user experience.

---
### Skills
* HTML5, CSS3
* JavaScript Basics
* Git, GitHub
* VS Code

---
### Code example
*Weather widget (API)*
```
const param = {
    "url": "https://api.openweathermap.org/data/2.5/",
    "appid": "******" // API key
}

function createCitySelect() {
    const cities = [
        { id: '2834282', name: 'Schwerin' },
        { id: '1508291', name: 'Chelyabinsk' },
        { id: '1835847', name: 'Seoul' },
        { id: '491422', name: 'Sochi' },
    ];

    const select = document.createElement('select');
    select.id = 'city';

    cities.forEach(city => {
        const option = document.createElement('option');
        option.value = city.id;
        option.innerText = city.name;
        select.appendChild(option);
    });

    document.querySelector('.select').appendChild(select);
}

function getWeather() {
    const cityId = document.querySelector('#city').value;
    fetch(`${param.url}weather?id=${cityId}&units=metric&APPID=${param.appid}`)
        .then(weather => {
            return weather.json();
        }).then(showWeather);
}

function showWeather(data) {
    console.log(data);
    document.querySelector('.city-name').innerHTML = data.name;
    document.querySelector('.temp').innerHTML = Math.round(data.main.temp) + '&deg;';
    document.querySelector('.description').innerHTML = data.weather[0].description;
    document.querySelector('.icon').innerHTML = '<img src="https://openweathermap.org/img/wn/' + data.weather[0].icon + '@2x.png">';
    document.querySelector('.deg').innerHTML = 'Wind' + ' ' + data.wind.deg + '&deg;' + ' ' + data.wind.speed + ' ' + 'm/s';
    document.querySelector('.pressure').innerHTML = 'Pressure' + ' ' + data.main.pressure + ' ' + 'hpa';
}

createCitySelect();
getWeather();
document.querySelector('#city').onchange = getWeather;

```
---
### Courses:
* Responsive Web Design on [freeCodeCamp](https://www.freecodecamp.org/)
![certificate](/img/ffc.jpg) 
* Java Script course on [ITGid](https://itgid.info/)
* RS School "JavaScript/Front-end" (in progress)
---
### Languages:
* English - Advanced
* Russian - Native 
* German - Intermediate 
* Korean - Basic 
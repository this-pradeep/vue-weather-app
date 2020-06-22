<template>
  <div id="app" class="bg-brand-100">
    <div class="pt-20 pb-56 hero rounded-b-xxl">
      <div class="container mx-auto px-auto">
        <img class="mx-auto md:h-32" :src="logo" alt="Hello" />
        <h1 class="text-xl text-center text-white my-2">
          Find the latest weather upadates on your mobile
        </h1>
        <div class="mx-auto my-5 w-5/6 flex items-center relative sm:w-1/2">
          <input
            type="search"
            id="address"
            name="search"
            class="h-10 px-4 w-full mx-auto shadow-md appearance-none border-2 border-blue-600 rounded-xl focus:outline-none focus:border-2 focus:border-blue-700"
            placeholder="Search City"
          />
        </div>
        <p class="text-blue-200 text-center mt-3">
          Selected: <strong id="address-value">none</strong>
        </p>
      </div>
    </div>
    <br />
    <div
      class="bg-blue-500 w-11/12 mx-auto -mt-56 px-2 py-5 gradient rounded-xxl shadow-xl md:px-20 py-5 md:w-9/12"
    >
      <div
        class="flex flex-col px-5 divide-y sm:divide-y-0 sm:divide-x sm:flex-row sm:justify-between sm:items-center"
      >
        <div class="w-full flex flex-col mb-8 sm:w-1/2">
          <div>
            <h1 class="text-xl text-white md:text-3xl">{{ location.city }}</h1>
            <h2 class="text-base text-white">
              {{ today.day }}, {{ today.date }} {{ today.month }}
            </h2>
          </div>
          <div class="flex justify-start items-top mt-5 md:mt-8">
            <div>
              <img :src="current.icon" class="w-full md:w-40" alt="">
            </div>
            <div class="mx-8">
              <h1 class="text-5xl font-bold text-white md:text-6xl">
                {{ current.actual }}<sup>o</sup>C
              </h1>
              <p class="text-base text-white">{{ current.summary }}</p>
            </div>
          </div>
        </div>
        <div class="sm:w-1/2 sm:mx-5">
          <div class="pt-5 flex flex-row justify-around itmes-center">
            <div class="text-center">
              <h3 class="text-xl font-semibold text-white">
                {{ current.presure }} hPa
              </h3>
              <p class="text-base text-white">Presure</p>
            </div>
            <div class="text-center">
              <h3 class="text-xl font-semibold text-white">
                {{ current.wind_speed }} m/s
              </h3>
              <p class="text-base text-white">Wind Speed</p>
            </div>
            <div class="text-center">
              <h3 class="text-xl font-semibold text-white">
                {{ newTime(today.sunrise) }}
              </h3>
              <p class="text-base text-white">Sunrise</p>
            </div>
          </div>
          <div class="pt-5 flex flex-row justify-around itmes-center">
            <div class="text-center">
              <h3 class="text-xl font-semibold text-white">
                {{ current.humidity }}%
              </h3>
              <p class="text-base text-white">Humidity</p>
            </div>
            <div class="text-center">
              <h3 class="text-xl font-semibold text-white">
                {{ Math.round(current.feels_like) }}<sup>o</sup>C
              </h3>
              <p class="text-base text-white">Feels Like</p>
            </div>
            <div class="text-center">
              <h3 class="text-xl font-semibold text-white">
                {{ newTime(today.sunset) }}
              </h3>
              <p class="text-base text-white">Sunset</p>
            </div>
          </div>
        </div>
      </div>
      <div class="px-5 mt-5">
        <h1 class="text-base font-bold text-white mb-3">
          Next 5 Hours Forecast
        </h1>
        <div
          class="flex flex-row pb-5 justify-start overflow-x-auto md:justify-between"
        >
          <div
            v-for="hour in hours"
            :key="hour.dt"
            class="w-1/3 bg-blue-200 py-2 px-2 rounded-xl mr-4 shadow-lg sm:rounded-xxl md:w-1/6"
          >
            <p class="text-sm font-semibold text-center my-2">
              {{ newTime(hour.dt) }}
            </p>
            <div class="w-10/12 mx-auto my-1 sm:w-9/12 sm:mx-auto">
              <img :src="hourlyIcon + hour.weather[0].icon +'@2x.png'" alt="">
            </div>
            <p class="text-2xl text-center font-bold my-2 sm:text-3xl">
              {{ Math.round(hour.temp) }}<sup>o</sup>C
            </p>
          </div>
        </div>
      </div>
      <div class="px-3 mt-5">
        <h1 class="text-base font-bold text-white mb-3">8 days' forecast</h1>
        <div
          v-for="day in days"
          :key="day.dt"
          class="flex flex-row items-center py-3 justify-between bg-blue-200 shadow-lg mb-8 rounded-xl overflow-x-auto"
        >
          <div class="text-2xl font-bold mx-5 md:w-1/12">
            {{ newDay(day.dt) }}
          </div>
          <div class="w-1/12 md:w-1/12">
            <img class="w-full object-cover" :src="hourlyIcon + day.weather[0].icon +'@2x.png'" alt="">
          </div>
          <div
            class="mr-5 w-10/12 flex flex-row justify-between itmes-center md:w-5/6"
          >
            <div class="text-center mx-5">
              <h3 class="text-lg font-semibold">
                {{ Math.round(day.temp.day) }}<sup>o</sup>C
              </h3>
              <p class="text-sm">Temp</p>
            </div>
            <div class="text-center mx-5">
              <h3 class="text-lg font-semibold">{{ day.pressure }}hPa</h3>
              <p class="text-sm">Pressure</p>
            </div>
            <div class="text-center mx-5">
              <h3 class="text-lg font-semibold">{{ day.wind_speed }}m/s</h3>
              <p class="text-sm">Wind_Speed</p>
            </div>
            <div class="text-center mx-5">
              <h3 class="text-lg font-semibold">{{ day.humidity }}%</h3>
              <p class="text-sm">Humidity</p>
            </div>
            <div class="text-center mx-5">
              <h3 class="text-lg font-semibold">{{ newTime(day.sunrise) }}</h3>
              <p class="text-sm">Sunrise</p>
            </div>
            <div class="text-center mx-5">
              <h3 class="text-lg font-semibold">{{ newTime(day.sunset) }}</h3>
              <p class="text-sm">Sunset</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <br />
    <div class="my-3">
      <p class="text-blue-700 text-center text-sm">
        &copy; 2020 <br />Designed &amp; Developed with love by Pradeep Nayak
      </p>
    </div>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {},
  mounted() {
    //current date & month
    let date = new Date();
    var days = [
      "Sunday",
      "Monday",
      "Tuesday",
      "Wednesday",
      "Thursday",
      "Friday",
      "Saturday"
    ];
    var months = [
      "January",
      "February",
      "March",
      "April",
      "May",
      "June",
      "July",
      "August",
      "September",
      "October",
      "November",
      "December"
    ];
    this.today.day = days[date.getDay()].toString();
    this.today.month = months[date.getMonth()].toString();
    this.today.date = date.getDate().toString();

    this.fetchData();

    var places = require("places.js");
    var placesAutocomplete = places({
      appId: "pl8P9HXEV66M",
      apiKey: "4bc2d7cb8e625b6f31e2673c457c04cd",
      container: document.querySelector("#address")
    }).configure({
      type: "city",
      aroundLatLngViaIP: false
    });

    var $address = document.querySelector("#address-value");
    placesAutocomplete.on("change", e => {
      $address.textContent = e.suggestion.value;
      this.location.city = `${e.suggestion.name}, ${e.suggestion.country}`;
      this.location.lat = e.suggestion.latlng.lat;
      this.location.lon = e.suggestion.latlng.lng;
    });

    placesAutocomplete.on("clear", function() {
      $address.textContent = "none";
    });
  },
  watch: {
    location: {
      handler() {
        this.fetchData();
      },
      deep: true
    }
  },
  data() {
    return {
      logo: require("./assets/img/logo.svg"),
      background: require("./assets/img/clouds.jpeg"),
      location: {
        city: "Indore, India",
        lat: "22.7196",
        lon: "75.8577"
      },
      today: {
        sunrise: "",
        sunset: "",
        date: "",
        month: "",
        day: ""
      },
      hourlyIcon: 'http://openweathermap.org/img/wn/',
      hours: [],
      days: [],
      current: {
        actual: "",
        feels_like: "",
        summary: "",
        wind_speed: "",
        presure: "",
        humidity: "",
        visibility: "",
        icon: ""
      }
    };
  },
  methods: {
    fetchData() {
      fetch(
        `https://api.openweathermap.org/data/2.5/onecall?lat=${this.location.lat}&lon=${this.location.lon}&units=metric&exclude=minutely&appid=550f13cf30a000e80a7df1e0c32add8b`
      )
        .then(response => response.json())
        .then(data => {
          this.current.actual = Math.round(data.current.temp);
          this.current.feels = Math.round(data.current.feels_like);
          this.current.summary = data.current.weather[0].description;
          this.current.wind_speed = data.current.wind_speed;
          this.current.presure = data.current.pressure;
          this.current.humidity = data.current.humidity;
          this.current.feels_like = data.current.feels_like;
          this.today.sunrise = data.current.sunrise;
          this.today.sunset = data.current.sunset;
          let icons = data.current.weather[0].icon;
          this.current.icon = `http://openweathermap.org/img/wn/${icons}@2x.png`;
          //5 hours forecast
          this.hours = data.hourly.slice(0, -43);
          this.days = data.daily;
        });
    },
    newTime(timestamp) {
      const time = new Date(timestamp * 1000);
      time.getHours();
      time.getMinutes();
      return `${time.getHours()}:${time.getMinutes()}`;
    },
    newDay(timestamp) {
      const date = new Date(timestamp * 1000);
      var days = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"];
      return days[date.getDay()];
    }
  }
};
</script>

<style lang="scss">
html {
  scroll-behavior: smooth;
}
::-moz-selection {
  /* Code for Firefox */
  color: #65d7e4;
  background: black;
}
::selection {
  color: #65d7e4;
  background: black;
}

.hero {
  background-attachment: local;
  background: url("./assets/img/clouds.jpeg") rgba(0, 77, 122, 1);
  background-blend-mode: multiply;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
.gradient {
  background: linear-gradient(
    to top right,
    rgb(62, 215, 255),
    rgb(0, 118, 151)
  );
}
</style>

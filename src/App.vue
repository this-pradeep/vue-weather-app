<template>
  <div id="app">
    <div class="pt-20 pb-56 hero rounded-b-xxl">
      <div class="container mx-auto px-auto">
        <img class="mx-auto" :src="logo" alt="Hello">
        <h1 class="text-xl text-center text-white my-2">Find the latests weather upadates on your mobile</h1>
        <div class="mx-auto my-5 w-5/6 flex items-center relative sm:w-1/2">
          <input type="search" name="search" class="h-10 px-4 w-full mx-auto shadow-md appearance-none border-2 border-blue-600 rounded-xl focus:outline-none focus:border-2 focus:border-blue-700" placeholder="Search City">
          <svg class="h-5 w-5 absolute right-0 mr-6" viewBox="0 0 24 23.988">
            <path id="search" d="M15.743,17.474a9.762,9.762,0,1,1,1.721-1.721l6.528,6.5L22.259,23.99l-6.5-6.516Zm-5.979-.39A7.322,7.322,0,1,0,2.442,9.762a7.322,7.322,0,0,0,7.322,7.322Z" transform="translate(0.008 -0.002)" fill="#037a9c"/>
          </svg>
        </div>
      </div>
    </div><br>
    <div class="bg-blue-500 w-11/12 mx-auto -mt-56 px-2 py-5 gradient rounded-xxl shadow-xl md:px-20 py-5 md:w-9/12">
      <div class="flex flex-col px-5 divide-y sm:divide-y-0 sm:divide-x sm:flex-row sm:justify-between sm:items-center">
        <div class="w-full flex flex-col mb-8 sm:w-1/2">
          <div>
            <h1 class="text-xl text-white md:text-3xl">Indore,IN</h1>
            <h2 class="text-base text-white">Monday, 29 June</h2>
          </div>
          <div class="flex justify-start items-top mt-5 md:mt-8">
            <div>
              <svg class="h-20"  viewBox="0 0 108.989 86.73">
                <g id="Group_2" data-name="Group 2" transform="translate(2.284 2.797)">
                  <ellipse id="Ellipse_1" data-name="Ellipse 1" cx="23.511" cy="23.059" rx="23.511" ry="23.059" transform="translate(27.129 37.814)" fill="#fff"/>
                  <circle id="Ellipse_2" data-name="Ellipse 2" cx="23.059" cy="23.059" r="23.059" transform="translate(60.587 37.814)" fill="#fff"/>
                  <circle id="Ellipse_3" data-name="Ellipse 3" cx="23.511" cy="23.511" r="23.511" transform="translate(40.693 17.92)" fill="#fff"/>
                  <g id="Ellipse_4" data-name="Ellipse 4" transform="translate(15.373 14.303)" fill="none" stroke="#fff" stroke-width="4">
                    <circle cx="20.799" cy="20.799" r="20.799" stroke="none"/>
                    <circle cx="20.799" cy="20.799" r="18.799" fill="none"/>
                  </g>
                  <line id="Line_1" data-name="Line 1" y1="9.043" x2="9.043" transform="translate(50.188 7.521)" fill="none" stroke="#fff" stroke-linecap="round" stroke-width="4"/>
                  <line id="Line_2" data-name="Line 2" y1="9.043" x2="9.043" transform="translate(11.304 52.735)" fill="none" stroke="#fff" stroke-linecap="round" stroke-width="4"/>
                  <line id="Line_3" data-name="Line 3" y1="9.043" x2="9.043" transform="matrix(0.174, 0.985, -0.985, 0.174, 14.971, 12.23)" fill="none" stroke="#fff" stroke-linecap="round" stroke-width="4"/>
                  <line id="Line_5" data-name="Line 5" y1="1.758" x2="11.304" transform="translate(0 39.171)" fill="none" stroke="#fff" stroke-linecap="round" stroke-width="4"/>
                  <line id="Line_6" data-name="Line 6" x2="11.304" y2="1.758" transform="matrix(0.259, 0.966, -0.966, 0.259, 31.262, 0)" fill="none" stroke="#fff" stroke-linecap="round" stroke-width="4"/>
                </g>
              </svg>
            </div>
            <div class="mx-8">
              <h1 class="text-5xl font-bold text-white md:text-6xl">23<sup>o</sup>C</h1>
              <p class="text-base text-white">Sunny Weather</p>
            </div>
          </div>
        </div>
        <div class="sm:w-1/2 sm:mx-5">
          <div class="pt-5 flex flex-row justify-around itmes-center">
          <div class="text-center">
            <h3 class="text-xl font-semibold text-white">32 <sup>o</sup>C</h3>
            <p class="text-base text-white">High</p>
          </div>
          <div class="text-center">
            <h3 class="text-xl font-semibold text-white">32 <sup>o</sup>C</h3>
            <p class="text-base text-white">High</p>
          </div>
          <div class="text-center">
            <h3 class="text-xl font-semibold text-white">32 <sup>o</sup>C</h3>
            <p class="text-base text-white">High</p>
          </div>
        </div>
        <div class="pt-5 flex flex-row justify-around itmes-center">
          <div class="text-center">
            <h3 class="text-xl font-semibold text-white">32 <sup>o</sup>C</h3>
            <p class="text-base text-white">High</p>
          </div>
          <div class="text-center">
            <h3 class="text-xl font-semibold text-white">32 <sup>o</sup>C</h3>
            <p class="text-base text-white">High</p>
          </div>
          <div class="text-center">
            <h3 class="text-xl font-semibold text-white">32 <sup>o</sup>C</h3>
            <p class="text-base text-white">High</p>
          </div>
        </div>
        </div>
      </div>
      <div class="px-5 mt-5">
        <h1 class="text-base font-bold text-white mb-3">Today's Weather</h1>
        <div class="flex flex-row pb-5 justify-start overflow-x-auto md:justify-between">
          <div class="w-1/3 justify-between bg-white py-2 px-2 rounded-xl mr-4 shadow-lg sm:rounded-xxl md:w-1/6">
            <p class="text-sm font-semibold text-center my-2">8:00 AM</p>
            <div class="w-10/12 mx-auto my-1 sm:w-9/12 sm:mx-auto">
              <svg viewBox="0 0 67.142 53.214">
                <g id="Group_52" data-name="Group 52" transform="translate(-302.858 -684.786)">
                  <ellipse id="Ellipse_1" data-name="Ellipse 1" cx="14.5" cy="14" rx="14.5" ry="14" transform="translate(321 710)" fill="#037b9d"/>
                  <ellipse id="Ellipse_2" data-name="Ellipse 2" cx="14.5" cy="14" rx="14.5" ry="14" transform="translate(341 710)" fill="#037b9d"/>
                  <circle id="Ellipse_3" data-name="Ellipse 3" cx="14.5" cy="14.5" r="14.5" transform="translate(329 697)" fill="#037b9d"/>
                  <g id="Ellipse_4" data-name="Ellipse 4" transform="translate(313 695)" fill="none" stroke="#037b9d" stroke-width="2">
                    <circle cx="13" cy="13" r="13" stroke="none"/>
                    <circle cx="13" cy="13" r="12" fill="none"/>
                  </g>
                  <line id="Line_1" data-name="Line 1" y1="5.583" x2="5.583" transform="translate(334.983 690.828)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_2" data-name="Line 2" y1="5.583" x2="5.583" transform="translate(310.978 718.74)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_3" data-name="Line 3" y1="5.583" x2="5.583" transform="matrix(0.174, 0.985, -0.985, 0.174, 313.242, 693.735)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_5" data-name="Line 5" y1="1.085" x2="6.978" transform="translate(304 710.366)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_6" data-name="Line 6" x2="6.978" y2="1.085" transform="matrix(0.259, 0.966, -0.966, 0.259, 323.3, 686.185)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                </g>
              </svg>
            </div>
            <p class="text-2xl text-center font-bold my-2 sm:text-3xl">32<sup>o</sup>C</p>
          </div>
          <div class="w-1/3 justify-between bg-white py-2 px-2 mr-4 rounded-xl shadow-xl sm:rounded-xxl md:w-1/6">
            <p class="text-sm font-semibold text-center my-2">8:00 AM</p>
            <div class="w-10/12 mx-auto my-1 sm:w-9/12 sm:mx-auto">
              <svg viewBox="0 0 67.142 53.214">
                <g id="Group_52" data-name="Group 52" transform="translate(-302.858 -684.786)">
                  <ellipse id="Ellipse_1" data-name="Ellipse 1" cx="14.5" cy="14" rx="14.5" ry="14" transform="translate(321 710)" fill="#037b9d"/>
                  <ellipse id="Ellipse_2" data-name="Ellipse 2" cx="14.5" cy="14" rx="14.5" ry="14" transform="translate(341 710)" fill="#037b9d"/>
                  <circle id="Ellipse_3" data-name="Ellipse 3" cx="14.5" cy="14.5" r="14.5" transform="translate(329 697)" fill="#037b9d"/>
                  <g id="Ellipse_4" data-name="Ellipse 4" transform="translate(313 695)" fill="none" stroke="#037b9d" stroke-width="2">
                    <circle cx="13" cy="13" r="13" stroke="none"/>
                    <circle cx="13" cy="13" r="12" fill="none"/>
                  </g>
                  <line id="Line_1" data-name="Line 1" y1="5.583" x2="5.583" transform="translate(334.983 690.828)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_2" data-name="Line 2" y1="5.583" x2="5.583" transform="translate(310.978 718.74)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_3" data-name="Line 3" y1="5.583" x2="5.583" transform="matrix(0.174, 0.985, -0.985, 0.174, 313.242, 693.735)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_5" data-name="Line 5" y1="1.085" x2="6.978" transform="translate(304 710.366)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_6" data-name="Line 6" x2="6.978" y2="1.085" transform="matrix(0.259, 0.966, -0.966, 0.259, 323.3, 686.185)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                </g>
              </svg>
            </div>
            <p class="text-2xl text-center font-bold my-2 sm:text-3xl">32<sup>o</sup>C</p>
          </div>
          <div class="w-2/5 justify-between bg-white py-2 px-2 mr-4 rounded-xl shadow-xl sm:rounded-xxl md:w-1/6">
            <p class="text-sm font-semibold text-center my-2">8:00 AM</p>
            <div class="w-10/12 mx-auto my-1 sm:w-9/12 sm:mx-auto">
              <svg viewBox="0 0 67.142 53.214">
                <g id="Group_52" data-name="Group 52" transform="translate(-302.858 -684.786)">
                  <ellipse id="Ellipse_1" data-name="Ellipse 1" cx="14.5" cy="14" rx="14.5" ry="14" transform="translate(321 710)" fill="#037b9d"/>
                  <ellipse id="Ellipse_2" data-name="Ellipse 2" cx="14.5" cy="14" rx="14.5" ry="14" transform="translate(341 710)" fill="#037b9d"/>
                  <circle id="Ellipse_3" data-name="Ellipse 3" cx="14.5" cy="14.5" r="14.5" transform="translate(329 697)" fill="#037b9d"/>
                  <g id="Ellipse_4" data-name="Ellipse 4" transform="translate(313 695)" fill="none" stroke="#037b9d" stroke-width="2">
                    <circle cx="13" cy="13" r="13" stroke="none"/>
                    <circle cx="13" cy="13" r="12" fill="none"/>
                  </g>
                  <line id="Line_1" data-name="Line 1" y1="5.583" x2="5.583" transform="translate(334.983 690.828)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_2" data-name="Line 2" y1="5.583" x2="5.583" transform="translate(310.978 718.74)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_3" data-name="Line 3" y1="5.583" x2="5.583" transform="matrix(0.174, 0.985, -0.985, 0.174, 313.242, 693.735)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_5" data-name="Line 5" y1="1.085" x2="6.978" transform="translate(304 710.366)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_6" data-name="Line 6" x2="6.978" y2="1.085" transform="matrix(0.259, 0.966, -0.966, 0.259, 323.3, 686.185)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                </g>
              </svg>
            </div>
            <p class="text-2xl text-center font-bold my-2 sm:text-3xl">32<sup>o</sup>C</p>
          </div>
          <div class="w-2/5 justify-between bg-white py-2 px-2 mr-4 rounded-xl shadow-xl sm:rounded-xxl md:w-1/6">
            <p class="text-sm font-semibold text-center my-2">8:00 AM</p>
            <div class="w-10/12 mx-auto my-1 sm:w-9/12 sm:mx-auto">
              <svg viewBox="0 0 67.142 53.214">
                <g id="Group_52" data-name="Group 52" transform="translate(-302.858 -684.786)">
                  <ellipse id="Ellipse_1" data-name="Ellipse 1" cx="14.5" cy="14" rx="14.5" ry="14" transform="translate(321 710)" fill="#037b9d"/>
                  <ellipse id="Ellipse_2" data-name="Ellipse 2" cx="14.5" cy="14" rx="14.5" ry="14" transform="translate(341 710)" fill="#037b9d"/>
                  <circle id="Ellipse_3" data-name="Ellipse 3" cx="14.5" cy="14.5" r="14.5" transform="translate(329 697)" fill="#037b9d"/>
                  <g id="Ellipse_4" data-name="Ellipse 4" transform="translate(313 695)" fill="none" stroke="#037b9d" stroke-width="2">
                    <circle cx="13" cy="13" r="13" stroke="none"/>
                    <circle cx="13" cy="13" r="12" fill="none"/>
                  </g>
                  <line id="Line_1" data-name="Line 1" y1="5.583" x2="5.583" transform="translate(334.983 690.828)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_2" data-name="Line 2" y1="5.583" x2="5.583" transform="translate(310.978 718.74)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_3" data-name="Line 3" y1="5.583" x2="5.583" transform="matrix(0.174, 0.985, -0.985, 0.174, 313.242, 693.735)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_5" data-name="Line 5" y1="1.085" x2="6.978" transform="translate(304 710.366)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_6" data-name="Line 6" x2="6.978" y2="1.085" transform="matrix(0.259, 0.966, -0.966, 0.259, 323.3, 686.185)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                </g>
              </svg>
            </div>
            <p class="text-2xl text-center font-bold my-2 sm:text-3xl">32<sup>o</sup>C</p>
          </div>
          <div class="w-2/5 justify-between bg-white py-2 px-2 mr-4 rounded-xl shadow-xl sm:rounded-xxl md:w-1/6">
            <p class="text-sm font-semibold text-center my-2">8:00 AM</p>
            <div class="w-10/12 mx-auto my-1 sm:w-9/12 sm:mx-auto">
              <svg viewBox="0 0 67.142 53.214">
                <g id="Group_52" data-name="Group 52" transform="translate(-302.858 -684.786)">
                  <ellipse id="Ellipse_1" data-name="Ellipse 1" cx="14.5" cy="14" rx="14.5" ry="14" transform="translate(321 710)" fill="#037b9d"/>
                  <ellipse id="Ellipse_2" data-name="Ellipse 2" cx="14.5" cy="14" rx="14.5" ry="14" transform="translate(341 710)" fill="#037b9d"/>
                  <circle id="Ellipse_3" data-name="Ellipse 3" cx="14.5" cy="14.5" r="14.5" transform="translate(329 697)" fill="#037b9d"/>
                  <g id="Ellipse_4" data-name="Ellipse 4" transform="translate(313 695)" fill="none" stroke="#037b9d" stroke-width="2">
                    <circle cx="13" cy="13" r="13" stroke="none"/>
                    <circle cx="13" cy="13" r="12" fill="none"/>
                  </g>
                  <line id="Line_1" data-name="Line 1" y1="5.583" x2="5.583" transform="translate(334.983 690.828)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_2" data-name="Line 2" y1="5.583" x2="5.583" transform="translate(310.978 718.74)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_3" data-name="Line 3" y1="5.583" x2="5.583" transform="matrix(0.174, 0.985, -0.985, 0.174, 313.242, 693.735)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_5" data-name="Line 5" y1="1.085" x2="6.978" transform="translate(304 710.366)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  <line id="Line_6" data-name="Line 6" x2="6.978" y2="1.085" transform="matrix(0.259, 0.966, -0.966, 0.259, 323.3, 686.185)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                </g>
              </svg>
            </div>
            <p class="text-2xl text-center font-bold my-2 sm:text-3xl">32<sup>o</sup>C</p>
          </div>
        </div>
      </div>
      <div class="px-5 mt-5">
        <h1 class="text-base font-bold text-white mb-3">5 days' forecast</h1>
        <div class="flex items-center py-3 justify-between bg-white shadow-lg mb-8 rounded-xl overflow-x-auto">
          <div class="text-2xl font-bold mx-5 md:w-1/12">Mon</div>
            <div class="md:w-1/12">
              <svg class="h-10" viewBox="0 0 67.142 53.214">
                  <g id="Group_52" data-name="Group 52" transform="translate(-302.858 -684.786)">
                    <ellipse id="Ellipse_1" data-name="Ellipse 1" cx="14.5" cy="14" rx="14.5" ry="14" transform="translate(321 710)" fill="#037b9d"/>
                    <ellipse id="Ellipse_2" data-name="Ellipse 2" cx="14.5" cy="14" rx="14.5" ry="14" transform="translate(341 710)" fill="#037b9d"/>
                    <circle id="Ellipse_3" data-name="Ellipse 3" cx="14.5" cy="14.5" r="14.5" transform="translate(329 697)" fill="#037b9d"/>
                    <g id="Ellipse_4" data-name="Ellipse 4" transform="translate(313 695)" fill="none" stroke="#037b9d" stroke-width="2">
                      <circle cx="13" cy="13" r="13" stroke="none"/>
                      <circle cx="13" cy="13" r="12" fill="none"/>
                    </g>
                    <line id="Line_1" data-name="Line 1" y1="5.583" x2="5.583" transform="translate(334.983 690.828)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                    <line id="Line_2" data-name="Line 2" y1="5.583" x2="5.583" transform="translate(310.978 718.74)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                    <line id="Line_3" data-name="Line 3" y1="5.583" x2="5.583" transform="matrix(0.174, 0.985, -0.985, 0.174, 313.242, 693.735)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                    <line id="Line_5" data-name="Line 5" y1="1.085" x2="6.978" transform="translate(304 710.366)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                    <line id="Line_6" data-name="Line 6" x2="6.978" y2="1.085" transform="matrix(0.259, 0.966, -0.966, 0.259, 323.3, 686.185)" fill="none" stroke="#037b9d" stroke-linecap="round" stroke-width="2"/>
                  </g>
                </svg>
            </div>
            <div class="mr-5 w-10/12 flex flex-row justify-between itmes-center md:w-4/6">
              <div class="text-center mx-5">
                <h3 class="text-xl font-semibold">32 <sup>o</sup>C</h3>
                <p class="text-base">High</p>
              </div>
              <div class="text-center mx-5">
                <h3 class="text-xl font-semibold">32 <sup>o</sup>C</h3>
                <p class="text-base">High</p>
              </div>
              <div class="text-center mx-5">
                <h3 class="text-xl font-semibold">32 <sup>o</sup>C</h3>
                <p class="text-base">High</p>
              </div>
              <div class="text-center mx-5">
                <h3 class="text-xl font-semibold">32 <sup>o</sup>C</h3>
                <p class="text-base">High</p>
              </div>
              <div class="text-center mx-5">
                <h3 class="text-xl font-semibold">32 <sup>o</sup>C</h3>
                <p class="text-base">High</p>
              </div>
              <div class="text-center mx-5">
                <h3 class="text-xl font-semibold">32 <sup>o</sup>C</h3>
                <p class="text-base">High</p>
              </div>
          </div>
        </div>
      </div>
    </div><br>
    <div class="my-3">
      <p class="text-blue-700 text-center text-sm">&copy; 2020 <br>Designed &amp; Developed with love by Pradeep Nayak</p>
    </div>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
  },
  data() {
    return{
      logo: require('./assets/img/logo.svg'),
      background: require('./assets/img/clouds.jpeg')
    }
  },
};
</script>

<style lang="scss" scoped>
  .hero {
    // background-image: url('./assets/img/clouds.jpeg');
    background-attachment:local;
    background: url('./assets/img/clouds.jpeg') rgba(0, 77, 122, 1);
    background-blend-mode: multiply;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
  }
  .gradient{
    background: linear-gradient( to top right, rgb(62, 215, 255), rgb(0, 118,151));
  }
</style>
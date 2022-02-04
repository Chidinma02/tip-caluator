<template>
  <div class="hello">
    <!-- <h1>{{ msg }}</h1> -->
    <!-- <p>jjjjjjj</p> -->

    <div class="main backgroundColor">
      <div class="container">
        <div class="row container">
          <div class="col-12">
            <h1 class="ft mt-4 mb-4">Header</h1>
          </div>
        </div>

        <div class="row ro pt-5">
          <div class="col-lg-6 col-sm-12">
            <div class="ot">
              <p>Bill</p>
              <!-- <p v-if="error.length"> -->
              <!-- <b>Please correct the following errors</b> -->
              <!-- <ul> -->
              <!-- <li v-for="e in error" v-bind:key="e.id">{{e}}</li> -->
              <!-- </ul> -->
              <!-- </p> -->
              <p v-if="message.length === 0">add amount</p>
              <b-form-input
                id=""
                type="number"
                placeholder="$"
                required
                width="80px"
                class="ml-5 mr-5 pl-5 pr-5 mt-4"
                v-model="message"
              ></b-form-input>
              <!-- <input v-model="message" placeholder="edit me" /> -->
              <!-- <p>Message is: {{ message }}</p> -->

              <p class="mt-4">Select Tip %</p>
              <div class="row">
                <div class="col-6">
                  <button
                    class="btn btn-lg butt mt-4"
                    @click="fiveButton"
                    :disabled="message === ''"
                  >
                    5%
                  </button>
                </div>
                <div class="col-6">
                  <button
                    class="btn btn-lg butt mt-4"
                    :disabled="message === ''"
                    @click="tenButton"
                  >
                    10%
                  </button>
                </div>
                <div class="col-6">
                  <button
                    class="btn btn-lg but mt-4"
                    :disabled="message === ''"
                    @click="fifButton"
                  >
                    15%
                  </button>
                </div>
                <div class="col-6">
                  <button
                    class="btn btn-lg mt-4 butt"
                    :disabled="message === ''"
                    @click="twenButton"
                  >
                    25%
                  </button>
                </div>
                <div class="col-6">
                  <button
                    class="btn btn-lg butt mt-4"
                    :disabled="message === ''"
                    @click="fifty"
                  >
                    50%
                  </button>
                </div>
                <div class="col-6 mb-5">
                  <!-- <button class="btn btn-lg bu mt-4">Custom</button> -->
                  <!--  <b-form-input
                    id="fo"
                    type="email"
                    placeholder="Custom"
                    required
                    class="mt-4 ml-5"
                  ></b-form-input> -->
                  <input
                    type="email"
                    class="form-control mt-4 bu by"
                    id="exampleFormControlInput1"
                    placeholder="custom"
                    v-model="custom"
                    v-on:keyup.enter="cus"
                  />
                </div>
                <div class="row">
                  <div class="col-12">
                    <p v-if="num_of_people.length === 0">
                      add number of people
                    </p>
                    <h5 class="nu">Number of people</h5>
                    <div></div>
                    <input
                      type=""
                      class="form-control mt-2 mb-4"
                      id="exampleFormControlInput1"
                      placeholder="0"
                      v-model="num_of_people"
                    />
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="col-lg-6 col-sm-12 container">
            <div class="sec">
              <div class="row">
                <div class="col mt-5">
                  <div class="">
                    <h4>Tip Amount</h4>
                    <p class="">/person</p>
                  </div>
                  <div>
                    <h4 class="m">Total</h4>
                    <p>/person</p>
                  </div>
                </div>
                <div class="col mt-5">
                  <h2>{{ result }}</h2>
                  <h2 class="m l">{{ re }}</h2>
                </div>
              </div>
              <div class="row mb-5">
                <div class="col-12 mb-5">
                  <button class="n btn btn-lg" @click="Reset">RESET</button>
                </div>
              </div>
            </div>
          </div>
          <!-- <div class="col"></div> -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      error: [],
      message: "",
      val: "",
      result: "",
      num_of_people: "",
      res: "",
      re: "",
      custom: "",
    };
  },
  watch: {
    re: function () {
      // console.log(this.message);
      console.log(this.re);
    },
  },
  methods: {
    people() {
      // this.res = this.val - this.result;
      // this.re = this.res / this.num_of_people;
      // this.re = (this.val - this.result) / this.num_of_people;
      // this.re = this.val
    },
    fiveButton() {
      this.val = parseInt(this.message);
      this.re = this.val;
      this.val = (this.val * 5) / 100;
      // this.people();
      // this.re
      this.re = this.re / this.num_of_people;
      this.result = this.val;
      this.re = this.re - this.result;
    },
    tenButton() {
      this.val = parseInt(this.message);
      this.re = this.val;
      this.val = (this.val * 10) / 100;
      // this.people();
      // this.re
      this.re = this.re / this.num_of_people;
      this.result = this.val;
      this.re = this.re - this.result;
    },
    fifButton() {
      this.val = parseInt(this.message);
      this.re = this.val;
      this.val = (this.val * 15) / 100;
      // this.people();
      // this.re
      this.re = this.re / this.num_of_people;
      this.result = this.val;
      this.re = this.re - this.result;
    },
    twenButton() {
      this.val = parseInt(this.message);
      this.re = this.val;
      this.val = (this.val * 25) / 100;
      // this.people();
      // this.re
      this.re = this.re / this.num_of_people;
      this.result = this.val;
      this.re = this.re - this.result;
    },
    fifty() {
      this.val = parseInt(this.message);
      this.re = this.val;
      this.val = (this.val * 25) / 100;
      // this.people();
      // this.re
      this.re = this.re / this.num_of_people;
      this.result = this.val;
      this.re = this.re - this.result;
    },
    cus() {
      this.val = parseInt(this.message);
      this.re = this.val;
      this.val = (this.val * this.custom) / 100;
      // this.people();
      // this.re
      this.re = this.re / this.num_of_people;
      this.result = this.val;
      this.re = this.re - this.result;
    },
    Reset() {
      this.message = "";
      this.num_of_people = "";
      this.re = "";
      this.result = "";
    },
  },
};
</script>

<style scoped>
* {
  margin: 0px;
  padding: 0px;
}
.hello {
  background-color: hsl(185, 41%, 84%);
}
.ft {
}
.butt {
  color: white;
  width: 80px;

  background-color: hsl(183, 100%, 15%);
}
.sec {
  background-color: hsl(183, 100%, 15%);
  color: white;
  border-radius: 20px;
}

.bu {
  width: 100px;
  margin-left: 20px;
}
#fo {
  width: 100px !important;
}
.ot {
}
.ro {
  background-color: hsl(0, 0%, 100%);
  margin-bottom: 20px;
  border-radius: 20px;
}
.n {
  background-color: hsl(172, 67%, 45%) !important;
  margin-top: 130px !important;
}
.m {
  margin-top: 70px;
}
.l {
  margin-top: 100px;
}
* {
  font-family: "Space Mono", monospace !important;
}
.nu {
  margin-right: 300px;
}
a.button2 {
  display: inline-block;
  padding: 0.5em 3em;
  border: 0.16em solid #ffffff;
  margin: 0 0.3em 0.3em 0;
  box-sizing: border-box;
  text-decoration: none;
  text-transform: uppercase;
  font-family: "Roboto", sans-serif;
  font-weight: 400;
  color: #ffffff;
  text-align: center;
  transition: all 0.15s;
}
a.button2:hover {
  color: #dddddd;
  border-color: #dddddd;
}
a.button2:active {
  color: #bbbbbb;
  border-color: #bbbbbb;
}
@media all and (max-width: 30em) {
  a.button2 {
    display: block;
    margin: 0.4em auto;
  }
}

@media only screen and (max-width: 600px) {
  n {
    width: 500px !important;
  }
}
</style>
<template>
  <div class="hello">
    <div class="main backgroundColor">
      <div class="container">
        <div class="row container">
          <div class="col-12"><h1 class="ft">Header</h1></div>
        </div>
        <div class="row">
          <div class="col-lg-6 col-sm-12">
            <div class="ro pt-5">
              <p>Bill</p>
              <b-form-input
                id=""
                type="email"
                placeholder="$"
                required
                width="80px"
                class="ml-5 mr-5 pl-5 pr-5"
              ></b-form-input>
              <p class="mt-4">Select Tip %</p>
              <div class="row">
                <div class="col-6">
                  <button class="btn btn-lg butt mt-4">5%</button>
                </div>
                <div class="col-6">
                  <button class="btn btn-lg butt mt-4">10%</button>
                </div>
                <div class="col-6">
                  <button class="btn btn-lg but mt-4">15%</button>
                </div>
                <div class="col-6">
                  <button class="btn btn-lg mt-4 butt">25%</button>
                </div>
                <div class="col-6">
                  <button class="btn btn-lg butt mt-4">50%</button>
                </div>
                <div class="col-6 mb-5">
                  <input
                    type="email"
                    class="form-control mt-4 bu"
                    id="exampleFormControlInput1"
                    placeholder="custom"
                  />
                </div>
              </div>
            </div>
          </div>
          <div class="col-lg-6 col-sm-12"></div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default { name: "HelloWorld", props: { msg: String } };
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
  padding-top: 50px;
}
.butt {
  color: white;
  width: 80px;
  background-color: hsl(183, 100%, 15%);
}
.bu {
  width: 100px;
  margin-left: 80px;
}
#fo {
  width: 100px !important;
}
.ro {
  background-color: hsl(0, 0%, 100%);
  margin-top: 20px;
  margin-bottom: 20px;
  border-radius: 20px;
}
</style>
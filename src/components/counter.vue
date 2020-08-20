<template>
  <div id="example-1">
    <div class="container">
      <div class="row">
        <div class="col-sm">
           <button v-on:click="$like" class="btn btn-primary btn-lg" >
      <i class="far fa-thumbs-up"></i>LIKE
    </button>
        </div>
        <div class="col-sm">
          <button v-on:click="$love" class="btn btn-danger btn-lg" >
      <i class="far fa-thumbs-up"></i>LOVE
    </button>
        </div>
        <div class="col-sm">
           <button v-on:click="$lol" class="btn btn-warning btn-lg" >
      <i class="far fa-thumbs-up"></i>LOL
    </button>
        </div>
      </div>
    </div>
  
    <div class="container">
      <div class="row">
        <div class="col-sm">
          <h4>LIKE : {{ like }}</h4>
        </div>
        <div class="col-sm">
          <h4>LOVE : {{ love }}</h4>
        </div>
        <div class="col-sm">
          <h4>LOL : {{ lol }}</h4><br>
        </div>
  </div>
</div>
<h2>Total Score : {{ counter }}</h2>
<br>

  </div>
</template>


<script>
export default {
  data: function() {
    return {
      like: 0,
      love: 0,
      lol: 0,
      counter: 0,
      
    };
  },

  methods: {
    $like: function() {
      this.counter += 1;
      this.like += 1;
      this.$emit("cc", this.counter);
    },
    $love: function() {
      this.counter += 5;
      this.love += 1;
      this.$emit("cc", this.counter);
    },
    $lol: function() {
      this.counter += 10;
      this.lol += 1;
      this.$emit("cc", this.counter);
    },
  },
};
</script>

<style></style>

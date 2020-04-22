<template>
    <div class="row">
          <h1> XDD </h1>
      </div>
</template>

<script>
export default {
  data () {
    return {
      countries: []
    };
  },
    created: function() {
      fetch("https://api.covid19api.com/summary")
      .then(response => response.json())
      .then((data) =>{
        this.countries = data;
      })
    }
  }
</script>

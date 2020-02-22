<template>
  <div class="row">
    <form>
      <div class="col-sm-6 col-sm-offset-6">
        <label>Add Quote</label>
        <textarea rows="3" class="form-control" v-model="quote"></textarea>
      </div>
      <div class="col-sm-6 col-sm-offset-6">
        <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      quote: ""
    };
  },
  methods: {
    createNew() {
      this.$emit("quoteAdded", this.quote);
      this.quote = "";
    }
  }
};
</script>

<template>
  <div>
    <div class="card-style">
      <b-progress :value="progress" variant="success"></b-progress>
    </div>
    <b-card v-if="current_step==1" class="card-style" title="STEP1">
      <b-card-text>Something for first step.</b-card-text>
      <b-button class="float-right" variant="primary" @click="onClickNext">Next</b-button>
    </b-card>
    <b-card v-if="current_step==2" class="card-style" title="STEP2">
      <b-card-text>Do something for second step.</b-card-text>
      <b-button class="float-left" variant="secondary" @click="onClickBack">Back</b-button>
      <b-button class="float-right" variant="primary" @click="onClickNext">Next</b-button>
    </b-card>
    <b-card v-if="current_step==3" class="card-style" title="STEP3">
      <b-card-text>For furthermore in 3rd step.</b-card-text>
      <b-button class="float-left" variant="secondary" @click="onClickBack">Back</b-button>
      <b-button class="float-right" variant="primary" @click="onClickNext">Next</b-button>
    </b-card>
    <b-card v-if="current_step==4" class="card-style" title="STEP4">
      <b-card-text>Will soon finish.</b-card-text>
      <b-button class="float-left" variant="secondary" @click="onClickBack">Back</b-button>
      <b-button class="float-right" variant="primary" @click="onClickNext">Next</b-button>
    </b-card>
    <b-card v-if="current_step==5" class="card-style" title="STEP5">
      <b-card-text>Finished!</b-card-text>
      <b-button class="float-left" variant="secondary" @click="onClickBack">Back</b-button>
      <b-button class="float-center" variant="success" @click="onClickFirst">Back to first</b-button>
    </b-card>
  </div>
</template>
<script>
export default {
  name: "SimpleStepper",
  data() {
    return {
      current_step: 1,
      max_step: 5
    };
  },
  computed: {
    progress: function() {
      return Math.round(100 / this.max_step) * this.current_step;
    }
  },
  methods: {
    onClickNext: function() {
      this.current_step++;
    },
    onClickBack: function() {
      this.current_step--;
    },
    onClickFirst: function() {
      this.current_step = 1;
    }
  }
};
</script>

<style>
.card-style {
  width: 90%;
  margin: 0 auto;
}
</style>

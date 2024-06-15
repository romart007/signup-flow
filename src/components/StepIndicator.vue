<template>
    <div class="step-indicator">
      <div 
        v-for="(step, index) in steps" 
        :key="index" 
        :class="['step', { active: currentStep >= step.number }]">
        <div class="step-number step-circle">{{ step.number }}</div>
        <div class="step-label">{{ step.label }}</div>
      </div>
      <div class="step-line"></div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'StepIndicator',
    props: {
      currentStep: {
        type: Number,
        required: true
      },
      steps: {
        type: Array,
        required: true
      }
    }
  };
  </script>
  
  <style scoped></style>
  
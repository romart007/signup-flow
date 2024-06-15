<template>
  <div id="app">
    <main class="flex items-center justify-center h-100">
      <div class="container w-100">
        <StepIndicator :currentStep="currentStep" :steps="steps" />
        <div class="content">
          <FormContainer />
          <MarketingContainer class="marketing" />
        </div>
          <PhoneNumberComponent />
      </div>
    </main>
  </div>
</template>

<script>
import FormContainer from './components/FormContainer.vue';
import MarketingContainer from './components/MarketingContainer.vue';
import PhoneNumberComponent from './components/PhoneNumberComponent.vue';
import StepIndicator from './components/StepIndicator.vue';

export default {
  name: 'App',
  components: {
    FormContainer,
    MarketingContainer,
    PhoneNumberComponent,
    StepIndicator
  },
  data() {
    return {
      currentStep: 1,
      steps: [
        { number: 1, label: 'Setup An Account' },
        { number: 2, label: 'Done!' }
      ]
    };
  }
};
</script>

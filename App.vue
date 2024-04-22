<script setup>
import { ref } from 'vue';

const formula = ref('');

/*
 * FUNCTION: evaluate()
 * PARAMETERS: none
 * FUNCTIONALITY: evaluate() was already written by instructors.
 */
function evaluate() {
  try {
    /* WARNING! Never use eval in production code. */
    // eslint-disable-next-line no-eval
    formula.value = eval(formula.value)
  } catch (exception) {
    console.log("warning: invalid formula", exception);
    formula.value='Error'
  }
}

/*
 * FUNCTION: append()
 * PARAMETERS: value: Value to be appended to end of string.
 * FUNCTIONALITY: append() first checks to see if this.formula has been set.
 * If not, then it just replaces the value. If it has been set, it adds the
 * user input string (the button pressed) to the end of this.formula.
 */
function append(value) {
  if (this.formula === undefined || this.formula === null) {
    this.formula = value;
  } else {
    this.formula += value;
  }
}

/*
 * FUNCTION: backspace()
 * PARAMETERS: none
 * FUNCTIONALITY: backspace() uses slice() to cut the last character off from
 * the string. It uses toString() to ensure that this.formula is a string
 * (otherwise this function would not work when deleting the last character
 * from a result).
 */
function backspace() {
  let str = formula.value.toString()
  formula.value = str.slice(0, -1)
}
/*
 * FUNCTION: clear()
 * PARAMETERS: none
 * FUNCTIONALITY: clear() sets the value of the formula string to empty to clear the input field.
 */
function clear() {
  formula.value = '';
}
</script>

<template>
<BContainer>
  <BRow>
    <BCol cols="12">
        <BFormInput v-model="formula"></BFormInput>
    </BCol>
  </BRow>
  <BRow class="mt-3">
    <BCol><BButton size="lg" class="w-100" variant="primary" v-on:click="clear()">Clear</BButton></BCol>
    <BCol><BButton size="lg" class="w-100" variant="primary" v-on:click="append('%')">%</BButton></BCol>
    <BCol><BButton size="lg" class="w-100" variant="primary" v-on:click="append('/')">/</BButton></BCol>
    <BCol><BButton size="lg" class="w-100" variant="primary" v-on:click="append('*')">*</BButton></BCol>
  </BRow>
  <BRow class="mt-3">
    <BCol><BButton size="lg" class="w-100" variant="outline-primary" v-on:click="append('7')">7</BButton></BCol>
    <BCol><BButton size="lg" class="w-100" variant="outline-primary" v-on:click="append('8')">8</BButton></BCol>
    <BCol><BButton size="lg" class="w-100" variant="outline-primary" v-on:click="append('9')">9</BButton></BCol>
    <BCol><BButton size="lg" class="w-100" variant="primary" v-on:click="append('-')">-</BButton></BCol>
  </BRow>
  <BRow class="mt-3">
    <BCol><BButton size="lg" class="w-100" variant="outline-primary" v-on:click="append('4')">4</BButton></BCol>
    <BCol><BButton size="lg" class="w-100" variant="outline-primary" v-on:click="append('5')">5</BButton></BCol>
    <BCol><BButton size="lg" class="w-100" variant="outline-primary" v-on:click="append('6')">6</BButton></BCol>
    <BCol><BButton size="lg" class="w-100" variant="primary" v-on:click="append('+')">+</BButton></BCol>
  </BRow>
  <BRow class="mt-3">
    <BCol cols="9">
      <BRow>
        <BCol><BButton size="lg" class="w-100" variant="outline-primary" v-on:click="append('1')">1</BButton></BCol>
        <BCol><BButton size="lg" class="w-100" variant="outline-primary" v-on:click="append('2')">2</BButton></BCol>
        <BCol><BButton size="lg" class="w-100" variant="outline-primary" v-on:click="append('3')">3</BButton></BCol>
      </BRow>
      <BRow class="mt-3">
        <BCol><BButton size="lg" class="w-100" variant="outline-primary" v-on:click="append('0')">0</BButton></BCol>
        <BCol><BButton size="lg" class="w-100" variant="outline-primary" v-on:click="append('00')">00</BButton></BCol>
        <BCol><BButton size="lg" class="w-100" variant="outline-primary" v-on:click="append('.')">.</BButton></BCol>
      </BRow>
    </BCol>
    <BCol cols="3"><BButton size="lg" class="w-100 h-100" variant="primary" v-on:click="evaluate()">=</BButton></BCol>
  </BRow>
</BContainer>
</template>

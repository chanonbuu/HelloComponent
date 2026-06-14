<script setup>
var msg = 'Hello Message'
var rawHtml = '<h1>Hello</h1>'
var myTd = 'myId1'
var color = 'green'
var isDisabled = true
const objectOfAttrs = {
  id: 'container',
  class: 'wrapper',
  style: 'background-color:green',
}
var number = 1
var ok = true
</script>

<template>
  <div>{{ msg }}</div>
  <div v-html="rawHtml"></div>
  <div :id="myTd"></div>
  <font :color="color">งง</font>
  <button :disabled="isDisabled">isEnabled</button>
  <div v-bind="objectOfAttrs">สีเขียวนะอันนี้</div>
  <div>{{ number + 1 }}</div>
  <div>{{ ok ? 'Yes' : 'No' }}</div>
</template>

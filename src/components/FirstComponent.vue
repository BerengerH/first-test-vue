<template>
  <div class="test-div">
    <h1>This is a test - Hello World</h1>
    <p>Just to see, "{{testMessage}}"</p>
    <a :href="ironhackLink" target="_blank">{{testLinkMessage}}</a>
    <input type="text" v-model="textInput"> <span>Here is your text input: "{{textInput}}"</span>
    <button @click="btnClicked(); helloWorld();">Test btn for v-on</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
        testMessage: "let's try out some string templates!",
        testLinkMessage: "Here is some text to try dynamic links with v-bind.",
        ironhackLink: "https://www.ironhack.com",
        textInput: "",
    };
  },
  methods: {
    btnClicked(){
        alert("The button was correctly clicked");
    },
    helloWorld(){
        console.log("Hello World");
    },
  },
}
</script>

<style scoped>
.test-div{
    background-color: #edede9;
    margin: 80px auto;
}

.test-div *{
    display: block;
    margin: 20px auto;
}
</style>
<template>
    <div class="test">
      <input type="text" v-model="title"><br/>
      <h1>{{title}}</h1>
      <p v-if="showName">{{user.firstName}}</p>
      <p v-else>Nobody</p>

      <ul>
        <li v-for="item in items">{{item.title}}</li>
      </ul>

      <button v-on:click="greet">Say Greeting</button>

    </div>
</template>

<script>
    export default {
        name: "test",
      data() {
          return {
            title: 'Hello World',
            user: {
              firstName: 'John',
              lastName: 'Doe'
            },
            showName: true,
            items: [
              {title: 'Item One'},
              {title: 'Item Two'},
              {title: 'Item Three'}
            ]
          }
      },
      methods: {
        greet: function () {
          alert('hello');
        }
      }
    }
</script>

<style scoped>

</style>

<template>
<div class="first">
    <h1>
        {{Title}}
    </h1>
    <input type="text" v-model="Title"><br>
    <p v-if="showName">
        {{user.fs_name}}
    </p>
    <p v-else>Nobody</p>
    <ul>
        <li v-for="item in items">{{item.title}}</li>
    </ul>
    <button v-on:click="greet('Heloooo')">greating!</button>
    <br />
    <input type="text" v-on:keyup="pressKey" v-on:keyup.enter="enterHit" >

    <hr />
    <label>first Name :</label><input type="text" v-model="user.fs_name">
    <label>last Name :</label><input type="text" v-model="user.ls_name">
    <h3>
        {{fullName}}
    </h3>
    <h2>
        {{msg}}
    </h2>
</div>
</template>

<script>
export default {
  name:'first',
  props:{
      msg:{
          type: String,
          default: 'Foobar'
      }
  } ,
  data(){
      return {
          Title: 'Kacang Goreng',
          user:{
              fs_name:'Toto',
              ls_name:'Kicep'
          },
          showName: true,
          items: [
               {title: 'Kacang Goreng'},
               {title: 'Kacang Goreng'},
               {title: 'Kacang Goreng'}
          ]
      }
  },
  methods:{
      greet: function (greeting) {
          alert(greeting);
      },
      pressKey: function (e) {
          console.log(e.target.value);          
      },
      enterHit: function () {
          console.log('you hit enter')
      }
  },
  computed:{
      fullName: function () {
          return this.user.fs_name+ ' '+this.user.ls_name;
      }
  }

}
</script>

<<style scoped>

</style>

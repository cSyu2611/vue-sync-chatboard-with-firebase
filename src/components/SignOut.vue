<template>
  <div class="signout">
    <button @click="signOut">ログアウト</button>
  </div>
</template>

<script>
import firebase from "firebase";
export default {
  name: "SignOut",
  data() {
    return {
    };
  },
  methods: {
    signOut: function(){
      firebase.auth().signOut()
      this.$router.push("/signIn");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.signin {
  margin-top: 20px;

  display: flex;
  flex-flow: column nowrap;
  justify-content: center;
  align-items: center;
}
input {
  margin: 10px 0;
  padding: 10px;
}
</style>
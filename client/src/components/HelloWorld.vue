<template>
  <div class="login">
    <head>
      <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css" integrity="sha384-PsH8R72JQ3SOdhVi3uxftmaW6Vc51MKb0q5P2rRUpPvrszuE4W1povHYgTpBfshb" crossorigin="anonymous">
      <link rel="stylesheet" href="../assets/css/login.css">
      <title>Project Manager X</title>
    </head>
    <body>
      <div class="container">
        <header class="row">
        <p class="text-center">xXx</p>
        <!-- <img src=""> -->
        </header>
        <section class="row">
          <div class="col-md-6">
            <h1 id="title">Project Manager xXx</h1>
            <p id="description">It's a funny thing to sit down to write your next adventure in a campaign and realize that somewhere along the line it went from "campaign" to "long-running campaign".

            That's what happened with Obsidian Frontier, a sandbox-style campaign set in the World of Greyhawk. We launched it as a playtest campaign for D&D 5th Edition in October 2014. Two years and thirty-four sessions later, the playtest is still running, and the campaign's still going.</p>
          </div>
          <div class="col-md-6">
          
          </div>
        </section>
      </div>
    </body>
  </div>
</template>

<script >
import LoginServices from '@/services/LoginServices'

export default {
  name: 'login',
  data () {
    return {
      user: {
        username: '',
        password: ''
      }
    }
  },
  methods: {
    async login () {
      await LoginServices.doLogin({
        user: {
          username: this.username,
          password: this.password
        }
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
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
</style>

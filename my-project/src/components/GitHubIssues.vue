<template>
  <div class="container">
        <h1>Vue.js + Github</h1>
        <p class="lead">
            Página que lista issues de um repositório do Github, usando Vue.js.
        </p>

        <div v-if="response.status === 'error'" class="alert alert-danger">
            {{ response.message }}
        </div>

        <div class="row">
            <div class="col">
                <div class="form-group">
                    <input v-model="username"
                           type="text" class="form-control" placeholder="github username">
                </div>
            </div>

            <div class="col">
                <div class="form-group">
                    <input v-model="repository"
                           type="text" class="form-control" placeholder="github repositório">
                </div>
            </div>

            <div class="col-3">
                <div class="form-group">
                    <button @click.prevent.stop="getIssues()"
                            class="btn btn-success">GO</button>
                    <button @click.prevent.stop="reset()"
                            class="btn btn-danger">LIMPAR</button>
                </div>
            </div>
        </div>
  </div>
</template>

<script>
export default {
  name: "'GitHubIssues'",
  data() {
    return {};
  },

  methods: {},
};
</script>

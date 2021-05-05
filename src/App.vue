<template>
  <div class="container mt-5">
    <div class="row">
      <div class="col form-inline">
          <b-form-input v-model="newTask" placeholder="Enter task" @keyup.enter="add"></b-form-input>
      </div>
    </div>
  </div>
</template>

<script>
import draggable from 'vuedraggable'

export default {
  name: 'App',
  components: {
    draggable
  },
  data() {
    return {
      newTask: "",
      arrBacklog: [
        {name: "test"},
        {name: "tes1"},
        {name: "test2"},
        {name: "test3"},
      ],
      arrInProgress: [],
      arrTestes: [],
      arrDone: []
    }
  },
  methods: {
    add() {
      if (this.newTask){
        this.arrBacklog.push({name: this.newTask});
        this.newTask="";
      }
    }
  }
}
</script>

<style>
</style>

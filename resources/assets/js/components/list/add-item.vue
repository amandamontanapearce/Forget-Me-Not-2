<template>
<div class="container">
  <div class="row">
    <div class="col-12">
      <div class="card card-body bg-light">
        <div class="card-title">Add a task...</div>
        <div class="card-body">
          <div class="form-group">
            <label for="title" class="form-group-label">Task</label>
            <input type="text" name="title" v-model="task.title">
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>
<script>
export default {
  props: [],
  data() {
    return {
      task: {
        title: '',
      },
    }
  },


}
<script>

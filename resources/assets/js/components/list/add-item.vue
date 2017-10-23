<template>
<div class="container">
  <div class="row">
    <div class="col-12">
      <div class="card card-body bg-light">
        <div class="card-title">Add a task...</div>
        <div class="card-body">
          <form>
            <div class="input-group input-group-lg">
              <input type="text" name="title" v-model="task.title" class="form-control">
              <span class="input-group-btn">
                <button class="btn btn-secondary" type="button">Add</button>
                <button type="button" class="btn btn-secondary dropdown-toggle dropdown-toggle-split" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                  <span class="sr-only">Toggle Dropdown</span>
                </button>
                <div class="dropdown-menu">
                  <a class="dropdown-item" href="#">Add Due Date</a>
                  <a class="dropdown-item" href="#">Add Tags</a>
                  <a class="dropdown-item" href="#" :click="showDescriptionField = true">Add Description</a>
                  <div role="separator" class="dropdown-divider"></div>
                    <a class="dropdown-item" href="#">Add Priority Level</a>
                  </div>
              </span>
            </div>
            <div v-if="showDescriptionField" class="form-group">
              <label for="description">Task Description</label>
              <textarea class="form-control" v-model="task.description" rows="3" ></textarea>
            </div>
            <div v-if="showDueDate" class="form-group">
              <label for="dueDate">Task Due Date</label>
              <input id="dueDate" class="form-control" v-model="task.dueDate">
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</div>
</template>
<script>
import flatpickr from "flatpickr";

export default {
  props: [],
  data() {
    return {
      showDescriptionField: false;
      showDueDate: false;
      task: {
        title: '',
        description: '',
        dueDate: '',
      },
    }
  },
  created: {
  flatpickr("#dueDate", {});
  },

}
<script>

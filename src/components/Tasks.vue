<template>
  <div class="tasks">
    <h3>to do</h3>
    <button>+</button>
    <list>
      <li class="clearfix" @mouseenter="show" @mouseleave="hide">
        <i>x</i>
        <h3>Hello world</h3>
        <div class="content">
          get a better jobget a better jobget a better jobget a better jobget a
          better job get a better jobget a better jobget a better jobget a
          better jobget a better jobget a better job get a better jobget a
          better jobget a better jobget a better jobget a better jobget a better
          job get a better jobget a better jobget a better jobget a better
          jobget a better jobget a better job get a better job
        </div>
      </li>
      <li class="clearfix">
        <h3>Hello world</h3>
        <div class="content">
          get a better jobget a better jobget a better jobget a better jobget a
          better job get a bet
        </div>
      </li>
    </list>
  </div>
</template>

<script>
import { reactive, ref } from "vue";

const del = ref("none");
const show = () => {
  console.log('show');
  del.value = "block";
};
const hide = () => {
  console.log('hide');
  del.value = "none";
};
</script>

<style scoped>
.tasks {
  display: flex;
  width: 30%;
  height: 100%;
  padding: 10px 16px;
  flex-direction: column;
  background-color: bisque;
}
.tasks > h3 {
  height: 4%;
  font-size: 18px;
  font-style: italic;
  font-weight: bold;
  margin-bottom: 3px;
}
button {
  width: 100%;
  height: 6%;
}
list {
  height: 90%;
  list-style: none;
}
list li {
  position: relative;
  padding: 6px 10px;
  background-color: aquamarine;
  margin: 12px 0;
  border-radius: 6px;
}
list li h3 {
  float: left;
  width: 100%;
  height: 30%;
  margin-bottom: 4px;
  font-size: 20px;
}
list li i {
  display: v-bind(del);
  position: absolute;
  top: 8px;
  right: 8px;
  width: 12px;
  height: 12px;
  background-color: red;
  border-radius: 50%;
  border: none;
  line-height: 10px;
  text-align: center;
  color: aliceblue;
  font-size: 12px;
  font-style: normal;
}
list li h3::before {
  content: "•";
  margin-right: 3px;
  color: orange;
}
.content {
  float: left;
  width: 100%;
}
</style>

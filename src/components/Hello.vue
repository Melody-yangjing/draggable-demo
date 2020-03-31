<template>
  <div>
    <div  class="row">
      <div class="col-4">
        <h3>未完成</h3>

        <draggable
                id="first"
                :list="list"
                class="list-group"
                draggable=".item"
                group="a"
        >
          <div
                  class="list-group-item item"
                  v-for="element in list"
                  :key="element.name"
          >{{ element.name }}</div>


        </draggable>
      </div>

      <div class="col-4">
        <h3>进行中</h3>

        <draggable :list="list2" class="list-group" draggable=".item" group="a">
          <div
                  class="list-group-item item"
                  v-for="element in list2"
                  :key="element.name"
          >{{ element.name }}</div>

        </draggable>
      </div>

      <div class="col-4">
        <h3>已完成</h3>

        <draggable :list="list3" class="list-group" draggable=".item" group="a">
          <div
                  class="list-group-item item"
                  v-for="element in list3"
                  :key="element.name"
          >{{ element.name }}</div>

        </draggable>
      </div>
    </div>


    <div style="display: flex">
      <div style="border: 1px solid #000" class="left">{{list}}</div>
      <div style="border: 1px solid #000;margin: 0 20px" class="center" >{{list2}}</div>
      <div style="border: 1px solid #000" class="right">{{list3}}</div>
    </div>

  </div>
</template>

<script>
  import draggable from "vuedraggable";
  export default {
    name: "two-list-headerslots",
    order: 14,
    components: {
      draggable
    },
    data() {
      return {
        list: [
          { name: "John 1", id: 0 },
          { name: "Joao 2", id: 1 },
          { name: "Jean 3", id: 2 },
          { name: "Jean 4", id: 3 },
          { name: "Jean 5", id: 4 },
          { name: "Jean 6", id: 5 }
        ],
        list2: [],
        list3: [],
      };
    },
  };
</script>

<style scoped>
  .row {
    width: 100%;
    height: 100%;
    margin-top: 50px;
    display: flex;
    justify-content: center;
    color: #555;
  }

  .col-4{
    height: 100%;
    border: 1px solid #000;
  }
  .row .list-group {
    width: 300px;
    border: 1px solid #ddd;
    text-align: center;
    margin-right: 50px;
    height: 100%;
  }
  .row .list-group div {
    padding: 10px;
    border-bottom: 1px dashed #ddd;
  }
</style>

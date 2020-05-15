<template>
  <div class="list2">
    <div class="aaa">
      ssssssssssssss
    </div>
    <ul>
      <li
        v-for="(item,index) in List"
        :key="index"
        :class="{activeColor:colorIndex===index}"
        @click="changeColor(item,index)"
      >
        <span>{{item.name}}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "list",
  components: {},
  data() {
    return {
      List: [
        { name: "总的" },
        { name: "部分1" },
        { name: "部分2" },
        { name: "部分3" }
      ],
      colorIndex: -1
    };
  },
  mounted() {},
  methods: {
    changeColor(item, index) {
      console.log(index)
      this.colorIndex = index;
    }
  }
};
</script>

<style lang="scss" scoped>
.list2 {
  width: 100px;
  ul {
    list-style: none;
    .activeColor {
      background-color: #f6fbff;
      color: #298adb;
    }
    li {
      cursor: pointer;
    }
  }
}
</style>
<style lang="sass" scoped>

.aaa
  color: pink

</style>

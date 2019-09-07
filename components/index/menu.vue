<template>
  <div class="m-menu">
    <dl class="nav">
      <dt>全部分类</dt>
      <dd v-for="(item, idx) in menu" :key="idx">
        <i :class="item.type" />
        {{item.name}}
        <span class="arrow" />
      </dd>
    </dl>
    <div class="detail">
      <template></template>
      <h4>标题</h4>
      <span>子项</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      kind: "",
      menu: [
        {
          type: "food",
          name: "美食",
          child: [
            {
              title: "美食",
              child: ["代金券", "甜点", "饮品", "自助餐"]
            }
          ]
        },
        {
          type: "takeout",
          name: "外卖",
          child: [
            {
              title: "美食",
              child: ["代金券", "甜点", "饮品", "自助餐"]
            }
          ]
        }
      ]
    };
  },
  computed: {
    curdetail: function() {
      return [];
    }
  }
};
</script>
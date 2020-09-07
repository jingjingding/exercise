<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <input type="text" :value='test' @input='handleClick(832388)'>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>

    <el-table
      :data="tableData"
      style="width: 100%">
      <el-table-column
        prop="date"
        v-if='true'
        label="日期"
        width="180">
         <template slot-scope="scope">
           <div v-if='scope.row.name === "丁静静"'>
             {{scope.row.name}}
           <input :value="scope.row.age" type="number" @input="handleClick">


           </div>
          <!-- <div class="product-price" v-if="!(scope.row.children && scope.row.children.length)">
            <span class="max-after-price" :class="{ 'visible' : scope.row.maxRefundPrice === '' }">最多可退{{ formatPrice(scope.row.maxRefundPrice) }}元</span>
            <input
              type="number"
              :class="{'disable-input' : !scope.row.canEdit || needAllRefund }"
              @input="changeProductNum(scope.row)"
              :disabled="!scope.row.canEdit || needAllRefund"
              v-model="scope.row.refundPrice"
              placeholder="请输入金额"
              class="price-input">
            <span class="company">元</span>
          </div>
          <span v-else>-</span> -->
        </template>
      </el-table-column>
      <el-table-column
        prop="name"
        label="姓名"
        width="180">
      </el-table-column>
      <el-table-column
        prop="address"
        label="地址">
      </el-table-column>
    </el-table>
    <!-- <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-typescript" target="_blank" rel="noopener">typescript</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-router" target="_blank" rel="noopener">router</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-vuex" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul> -->
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
  private test: any = '32';
  private tableData: any[] =  [{
            date: '2016-05-02',
            name: '丁静静',
            address: '上海市普陀区金沙江路 1518 弄',
            age: 333
          }, {
            date: '2016-05-04',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1517 弄',
            age: 333
          }, {
            date: '2016-05-01',
            name: '丁静静',
            address: '上海市普陀区金沙江路 1519 弄',
            age: 333
          }, {
            date: '2016-05-03',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1516 弄',
            age: 333
          }]
  handleClick(val: any) {
    console.log(val)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
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

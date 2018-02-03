<template>
  <div class="for-seven">
    <el-card class="box-card">
      <div slot="header" class="clearfix">
        <el-input-number v-model="num1" :min="2" :max="10" label="描述文字"></el-input-number>
      </div>
      <div class="style-show">
        <span v-for="n in msg" :key="n">
          <span style="color: red" v-if="n % num1 === 0 || n.toString().indexOf(num1.toString()) >= 0">
            啪
          </span>
          <span v-else>
            {{n}}
          </span>
        </span>
      </div>

    </el-card>

  </div>
</template>

<script>
export default {
  name: 'ForSeven',
  data () {
    return {
      msg: 100,
      num1: 1
    }
  }
  // methods: {
  //   show () {
  //     // console.log(this.num1)
  //     for (var i = 1; i < this.msg; i++) {
  //       if (i % this.num1 === 0 || i.toString().indexOf(this.num1.toString()) >= 0) {
  //         console.log('啪')
  //       } else {
  //         console.log(i)
  //       }
  //     }
  //   }
  // }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
<style>
  .style-show {
    width: 80%;
    margin-left:10%;
    text-align: left;
  }
  .text {
    font-size: 14px;
  }

  .item {
    margin-bottom: 18px;
  }

  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  .clearfix:after {
    clear: both
  }

  .box-card {
    margin-top:50%;
    width: 90%;
    margin-left: 5%;
  }
</style>

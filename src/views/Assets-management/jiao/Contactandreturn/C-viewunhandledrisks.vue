<template>
    <div>
      <Header></Header>
      <el-col :span="24"
        ><div class="grid-content bg-purple-dark storageBox">
          <p>教学设备管理>设备借出和归还</p>
          <div class="baikuang">
            <router-link tag="p" to="/jiao/contact" class="rukus">返回</router-link>
            <p>


<!-- Form -->
<el-button type="success" class="left20" style="background:#00b698">借出</el-button>
<el-button type="danger" class="left20" @click="dialogFormVisible = true">拒绝</el-button>

<el-dialog title="拒绝申请" :visible.sync="dialogFormVisible">
  <el-form :model="form">
   
    拒绝原因:<el-input
  type="textarea"
  :rows="2"
  placeholder="请输入内容"
  v-model="textarea">
</el-input>

  </el-form>
  <div slot="footer" class="dialog-footer">
    <el-button type="danger" @click="dialogFormVisible = false">确 定 拒 绝</el-button>
  </div>
</el-dialog>
            
            
            
            
            
            
            </p>
           <CviewunhandledrisksTable></CviewunhandledrisksTable>
            <div class="xiaobaikuang">
              <div id="zuo">
                
              </div>
              <div id="you">
                <el-pagination
                  class="mTop"
                  background
                  layout="prev, pager, next"
                  :total="1000"
                >
                </el-pagination>
              </div>
            </div>
          </div>
        </div>
      </el-col>
    </div>
</template>
<script>
import Header from '../../../../components/Header/Index'
import CviewunhandledrisksTable from '../../../../components/Table/C-viewunhandledrisksTable'
export default {
    components:{
        Header,
        CviewunhandledrisksTable
    },
     data() {
      return {
        textarea: '',
        dialogFormVisible: false,
        form: {
          name: '',
          region: '',
          date1: '',
          date2: '',
          delivery: false,
          type: [],
          resource: '',
          desc: ''
        },
        formLabelWidth: '120px'
      };
    }
}
</script>
<style scoped>
    .storageBox {
  background: #f4f4f6;
  padding: 20px;
  font-size: 15px;
}
.baikuang {
  background: white;
}
.shuru {
  width: 180px;
  margin-left: 20px;
}
.rukus{
  padding: 20px;

}
#zuo {
  float: left;
}
#you {
  float: right;
}
.xiaobaikuang {
  height: 50px;
}
.left20{
  margin-left: 20px;
}
</style>
    

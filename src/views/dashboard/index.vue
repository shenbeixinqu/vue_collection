<template>
  <div class="dashboard"> 
      <div cclass="dashboard-header"></div>
      <el-row class="dashboard-content">
          <el-col :span="6" class="dashboard-left">
             <div class="dashboard-left-element">
                <div class="user-info">
                    <img 
                      src="../../assets/img/img.jpg"
                      class="user-avator"
                    />
                    <div>
                      <div class="user-info-name">admin</div>
                      <div class="user-info-role">管理员</div>
                    </div>
                </div>
                <div class="last-time">上次登录时间:2020-10-16 12:58:36</div>
             </div>
             <div class="dashboard-left-element">
                <div id="circle"></div>
             </div>
             <div class="dashboard-left-element">
                <div id="column"></div>
             </div>
          </el-col>
          <el-col :span="12" class="dashboard-middle">
            中
          </el-col>
          <el-col :span="6" class="dashboard-right">
              右
          </el-col>
      </el-row>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'Dashboard',
  computed: {
    ...mapGetters([
      'name'
    ])
  }
}
</script>

<style lang="scss" scoped>
.dashboard {
  width: 100%;
  height: calc(100% - 50px);
  // color: #ffffff;
  border-radius: 4px;
}
.dashboard-header {
  width: 100%;
  height: 50px;
  font-size: 26px;
  line-height: 50px;
  text-align: center;
  letter-spacing: 4px;
}
.dashboard-content {
  width: 100%;
  height: calc(100% - 100px);
}
.user-info {
  display: flex;
  justify-content: space-between;
  width: 60%;
  margin: 0 auto;
  padding-top: 25px;
}
.user-avator {
  width: 60px;
  height: 60px;
  border-radius: 50%;
}
.user-info-name {
  margin-top: 5px;
  font-size: 26px;
}
.user-info-role {
  font-size: 10px;
}
.last-time {
  width: 60%;
  margin: 0 auto;
  margin-top: 5px;
  font-size:10px;
  padding-left:5px;
}
.dashboard-left,
.dashboard-middle,
.dashboard-right {
  height: 100%;
}
.dashboard-left-element {
  width: 96%;
  margin: 10px auto;
  border-radius: 2px;
}
.dashboard-left-element:nth-child(1) {
  height: 16%;
  margin-bottom: 0;
}
</style>

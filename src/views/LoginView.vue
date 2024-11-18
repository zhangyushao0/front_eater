<script setup lang="ts">
import { reactive } from "vue";
import { ElForm, ElFormItem, ElInput, ElButton } from "element-plus";

const loginForm = reactive({
  username: "",
  password: "",
});

const handleSubmit = () => {
  console.log("登录表单提交", loginForm);
  // 在这里处理登录逻辑
};
</script>

<template>
  <main>
    <el-form :model="loginForm" @submit.native.prevent="handleSubmit">
      <el-form-item label="用户名" prop="username">
        <el-input v-model="loginForm.username"></el-input>
      </el-form-item>
      <el-form-item label="密码" prop="password">
        <el-input type="password" v-model="loginForm.password"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="handleSubmit">登录</el-button>
      </el-form-item>
    </el-form>
  </main>
</template>

<style scoped>
/* 添加一些样式 */
</style>

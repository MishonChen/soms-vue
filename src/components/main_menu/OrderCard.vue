<script setup lang="ts">
import {  Ref, inject } from "vue";
// 接收全局变量
const globalSelect = inject<Ref<string>>("globalSelect");
// 检查 globalSelect 是否存在并设置默认值
if (!globalSelect) {
  throw new Error("globalSelect is not provided");
}
function updateGlobalSelect() {
  if (globalSelect?.value !== undefined) {
    globalSelect.value = "4";
  }
}
</script>

<template>
<div class="notificationCard">
  <p class="notificationHeading">订单管理</p>
<svg t="1718855964118" class="bellIcon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="6885" width="200" height="200"><path d="M539.88352 289.77152c58.20928-0.87552 104.68352-48.768 103.81824-106.97728v-0.0256a108.14464 108.14464 0 0 0-37.79584-82.6368c2.1504 6.85568 3.3024 13.98272 3.41504 21.1712 2.21696 39.168-27.73504 72.71936-66.89792 74.93632-39.16288 2.21696-72.71424-27.73504-74.93632-66.89792-0.1536-2.67776-0.1536-5.36064 0-8.0384 0.01536-5.75488 0.70144-11.47904 2.048-17.0752a108.14464 108.14464 0 0 0-33.46944 78.5408c-0.88576 58.20928 45.57824 106.11712 103.78752 107.00288h0.03072z" p-id="6886"></path><path d="M536.69376 153.17504c38.40512-1.11616 68.8128-32.83968 68.30592-71.25504 0-38.2208-30.99136-69.21216-69.21216-69.21216-38.22592 0-69.21216 30.98624-69.21216 69.21216-0.51712 38.41536 29.89056 70.144 68.29568 71.25504h1.82272zM47.90784 792.67328l167.10144 66.70336c-13.43488-27.776-68.29568-447.58016-68.29568-447.58016l-98.80576 380.8768zM727.4752 1012.37248l10.70592-163.9168-374.7328 38.92224z" p-id="6887"></path><path d="M840.63232 109.23008l0.68608-0.22528-182.12864 27.5456a143.0016 143.0016 0 0 1 17.30048 68.29568c0 75.43808-61.15328 136.59648-136.6016 136.59648-75.43808 0-136.59648-61.1584-136.59648-136.59648 0.01536-10.10176 1.08544-20.1728 3.18464-30.04928l-223.79008 34.37568c8.19712 216.73472 105.17504 647.70048 105.17504 647.70048l698.46528-122.25536c-48.4864-50.08384-145.69472-625.38752-145.69472-625.38752zM247.60832 261.36576l98.60096-15.14496c19.10272 89.44128 98.688 156.672 193.67424 156.672 109.19936 0 198.0416-88.84224 198.0416-198.03648a203.83744 203.83744 0 0 0-0.78336-17.95072l53.25824-8.05376c9.99424 56.31488 26.2912 145.60768 44.67712 236.48256 27.87328 137.7792 48.50688 220.8256 64.32256 272.13824l-563.9936 98.7136C311.94624 675.5328 262.12352 428.48256 247.60832 261.36576z" p-id="6888"></path><path d="M325.4272 481.21856l297.09824-59.29472 8.87296 53.48864-297.5488 60.20608zM378.9312 721.408l-10.70592-53.15072 365.17376-67.72224 11.38688 52.69504zM351.04256 628.1728l-9.22112-50.64192 471.26016-90.49088 9.216 52.70016z" p-id="6889"></path></svg>
  <p class="notificationPara">订单管理模块，可以查看、更新、修改、删除订单信息</p>
  <div class="buttonContainer">
    <button @click="updateGlobalSelect()" class="AllowBtn">立即查看</button>
  </div>


</div>


</template>

<style scoped>
.notificationCard {
  width: 220px;
  height: 280px;
  background: rgb(245, 245, 245);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 20px 35px;
  gap: 10px;
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.123);
  border-radius: 20px;
}

.bellIcon {
  width: 140px;
  margin: 10px 0px;
}

.bellIcon path {
  fill: #d9c01d;
}

.notificationHeading {
  color: black;
  font-weight: 600;
  font-size: 22px;
}

.notificationPara {
  color: rgb(133, 133, 133);
  font-size: 14px;
  font-weight: 600;
  text-align: center;
}

.buttonContainer {
  display: flex;
  flex-direction: column;
  gap: 5px;
}

.AllowBtn {
  width: 200px;
  height: 40px;
  background-color: #d9c01d;
  color: white;
  border: none;
  border-radius: 20px;
  font-size: 1em;
  font-weight: 600;
  cursor: pointer;
}

.NotnowBtn {
  width: 120px;
  height: 25px;
  color: #d9c01d;
  border: none;
  background-color: transparent;
  font-weight: 600;
  font-size: 0.7em;
  cursor: pointer;
  border-radius: 20px;
}

.NotnowBtn:hover {
  background-color: rgb(239, 227, 255);
}

.AllowBtn:hover {
  background-color: #d9c01d;
}
</style>
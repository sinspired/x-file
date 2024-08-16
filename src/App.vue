<template>
  <div class="min-h-screen bg-gray-100">
    <Navbar />
    <main class="container mx-auto py-8 px-4">
      <h1 class="text-4xl font-bold text-center text-blue-600 mb-8">我的计划概览</h1>
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
        <PlanCard id="work" title="近期工作计划" :items="workPlans" />
        <PlanCard id="fitness" title="近期健身计划" :items="fitnessPlans" />
        <PlanCard id="travel" title="近期旅游计划" :items="travelPlans" />
      </div>
    </main>
    <footer class="bg-blue-600 text-white text-center py-4 mt-8">
      <p>&copy; 2024 我的计划网站. 保留所有权利.</p>
    </footer>
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import PlanCard from './components/PlanCard.vue'

const workPlans = [
  '完成项目A的开发',
  '参加团队会议',
  '学习新技术'
]

const fitnessPlans = [
  '每周跑步3次，每次5公里',
  '增加力量训练',
  '保持健康饮食'
]

const travelPlans = [
  '计划下个月的海边度假',
  '研究潜水课程',
  '准备旅行所需文件'
]
</script>
<template>
	<view class="content">
		<TnTabbar
		    v-model="currentTabbar"
		    fixed
		  >
		    <TnTabbarItem
		      v-for="(item, index) in tabbarData"
		      :key="index"
		      :icon="item.icon"
		      :active-icon="item.activeIcon"
		      :text="item.name"
		    />
		  </TnTabbar>
	</view>
</template>

<script setup>
	// 首页
	import TnTabbar from '@/uni_modules/tuniaoui-vue3/components/tabbar/src/tabbar.vue'
	import TnTabbarItem from '@/uni_modules/tuniaoui-vue3/components/tabbar/src/tabbar-item.vue'
	import { ref } from 'vue'
	
	const currentTabbar = ref(0)
	
	// 导航栏数据
	const tabbarData = [
	  {
	    name: '消息',
	    icon: 'home',
	    activeIcon: 'home-fill',
	  },
	  {
	    name: '通讯录',
	    icon: 'like',
	    activeIcon: 'like-fill',
	  },
	  {
	    name: '发现',
	    icon: 'fire',
	    activeIcon: 'fire-fill',
	  },
	  {
	    name: '我',
	    icon: 'my-circle',
	    activeIcon: 'my-circle-fill',
	  },
	]
	
</script>

<style lang="scss" scoped>
</style>

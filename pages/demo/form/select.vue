<template>
	<cl-page :padding="20">
		<cl-card label="基础用法">
			<cl-select v-model="v1" :options="list"></cl-select>
		</cl-card>

		<cl-card label="日期">
			<cl-select v-model="v2" mode="date" fields="month"></cl-select>
		</cl-card>

		<cl-card label="时间">
			<cl-select v-model="v3" mode="time"></cl-select>
		</cl-card>

		<cl-card label="禁用">
			<cl-select v-model="v4" :options="list" disabled></cl-select>
		</cl-card>
	</cl-page>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const v1 = ref();
const v2 = ref();
const v3 = ref();
const v4 = ref(2);

const list = ref([
	{
		label: "海南东山羊",
		value: 1,
	},
	{
		label: "乌鱼子",
		value: 2,
	},
]);
</script>

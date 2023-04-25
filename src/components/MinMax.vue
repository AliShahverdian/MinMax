<template>
	<div>
		<button :disabled="isReducingDisabled" @click="reduceNum">-</button>
		<input type="number" v-model.number="num" />
		<button :disabled="isIncreasingDisabled" @click="increaseNum">+</button>
	</div>
</template>
<script>
	export default {
		data() {
			return {
				num: 1,
				minNum: 1,
				maxNum: 10,
			};
		},
		computed: {
			isReducingDisabled() {
				return this.num === this.minNum;
			},
			isIncreasingDisabled() {
				return this.num === this.maxNum;
			},
		},
		methods: {
			reduceNum() {
				this.num--;
			},
			increaseNum() {
				this.num++;
			},
		},
	};
</script>

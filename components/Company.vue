<template>
    <div>
        <section class="text-gray-600 body-font">
            <div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
                <div class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center">
                <h1 class="title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-900">会社概要
                </h1>
                <p class="mb-8 leading-relaxed">
                    商号　株式会社東京BAiTAi
                    <br>
                    本社　〒160‐0023
                    <br>
                    &emsp; 東京都新宿区西新宿3-2-9
                    <br>
                    &emsp; 新宿ワシントンホテルビル2階
                    <br>
                    設立　2017年11月
                    <br>
                    資本金　5,000,000円
                    <br>
                    業務　屋外広告代理業
                    <br>
                    許認可　屋外広告業　都広００００号
                </p>
                <div class="flex justify-center">
                    <button class="inline-flex text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">プライバシー・ポリシー</button>
                </div>
                </div>
                <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6">
                    <!-- <img class="object-cover object-center rounded" alt="hero" src="https://dummyimage.com/720x600"> -->
                    <nuxt-img :src="image_1" alt="東京baitai" class="object-cover object-center rounded" />
                </div>
            </div>
        </section>
    </div>
</template>

<script>
export default {
	components: {

	},
	data() {
		return {
			image_1: 'images/photo7-min.jpg',
		}
	},
	methods: {

    },
    created() {
	
        },

}
</script>

<style lang="scss" scoped>

</style>
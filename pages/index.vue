<template>
    <div>
        <video width="100%" poster="/images/photo2-min.jpg" loop muted autoplay playsinline>
            <source src="/movies/topmovie1.mp4" type="video/mp4">
            申し訳ありません。ご使用のブラウザがVideoタグに対応しておりません。
        </video>
        <section class="text-gray-600 body-font">
            <div class="container px-5 py-24 mx-auto">
                <div class="text-center mb-6">
                    <h1 class="sm:text-3xl text-2xl font-medium title-font text-gray-900 mb-4">The leading edge trends.</h1>
                    <p class="text-base leading-relaxed xl:w-2/4 lg:w-3/4 mx-auto text-gray-500s">屋外広告企業専門の「東京BAiTAi」は、関わりのある全ての皆様に、最大限の価値を創造します。</p>
                    <div class="flex mt-6 justify-center">
                        <div class="w-16 h-1 rounded-full bg-indigo-500 inline-flex"></div>
                    </div>
                </div>
            </div>

            <nuxt-img fit="cover" :src="image_1" width="100%" alt="東京baitai" class="mb-5" />

            <Contact />

            <nuxt-img fit="cover" :src="image_2" width="100%" alt="東京baitai" class="" />

            <Company />

            <nuxt-img fit="cover" :src="image_3" width="100%" alt="東京baitai" class="" />

        </section>
    </div>
</template>

<script>
import Contact from '~/components/Contact'
import Company from '~/components/Company.vue'

export default {
	components: {
        Contact,
        Company,
	},
	data() {
		return {
			image_1: 'images/photo2-min.jpg',
			image_2: 'images/photo9-min.jpg',
			image_3: 'images/photo8-min.jpg',
		}
	},
	methods: {

    },
    created() {
	
        },

}
</script>

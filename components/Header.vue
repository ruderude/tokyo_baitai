<template>
	<div>
		<header class="text-gray-600 body-font">
			<div class="g-navbar flex flex-wrap p-2 flex-col md:flex-row items-center mx-auto">
				<nuxt-link to="/" class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0" >
					<!-- <img :src="logo_src" width="180px" alt="東京baitai"> -->
					<nuxt-img :src="logo_src" width="180" alt="東京baitai" />
				</nuxt-link>
				<nav class="md:ml-auto flex flex-wrap items-center text-base justify-center">
					<nuxt-link to="/company" class="mr-5 hover:text-gray-900" >Home</nuxt-link>
					<nuxt-link to="/company" class="mr-5 hover:text-gray-900" >Company</nuxt-link>
					<nuxt-link to="/company" class="mr-5 hover:text-gray-900" >Contact</nuxt-link>
				</nav>
				<button class="inline-flex items-center bg-gray-100 border-0 py-1 px-3 focus:outline-none hover:bg-gray-200 rounded text-base mt-4 md:mt-0">Privacy & Policy
					<svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 ml-1" viewBox="0 0 24 24">
						<path d="M5 12h14M12 5l7 7-7 7"></path>
					</svg>
				</button>
			</div>

			<nuxt-link to="/" class="nav-logo flex title-font font-medium items-center text-gray-900 p-4 mb-4 md:mb-0" >
				<nuxt-img :src="logo_src" width="180" alt="東京baitai" />
			</nuxt-link>

			<!--ハンバーガーメニューのボタン-->
			<div class="hamburger_btn" v-on:click='ActiveBtn=!ActiveBtn'>
				<span class="line line_01" v-bind:class="{'btn_line01':ActiveBtn}"></span>
				<span class="line line_02" v-bind:class="{'btn_line02':ActiveBtn}"></span>
				<span class="line line_03" v-bind:class="{'btn_line03':ActiveBtn}"></span>
			</div>
			<!--サイドバー-->
			<transition name="menu">
				<div class="menu" v-show="ActiveBtn">
					<ul>
						<li>
							<nuxt-link to="/company" class="mr-5 hover:text-gray-900" >Home</nuxt-link>
						</li>
						<li>
							<nuxt-link to="/company" class="mr-5 hover:text-gray-900" >Company</nuxt-link>
						</li>
						<li>
							<nuxt-link to="/company" class="mr-5 hover:text-gray-900" >Contact</nuxt-link>
						</li>
					</ul>
				</div>
			</transition>
		</header>
	</div>
</template>

<script>

export default {
	components: {

	},
	data() {
		return {
			ActiveBtn: false,
			// logo_src: require("@/assets/images/logo_black.png"),
			logo_src: 'images/logo_black-min.png',
		}
	},
	methods: {

    },
    created() {
	
        },

}
</script>

<style lang="scss" scoped>
.nav-logo {
	display: none;
}
.hamburger_btn {
	display: none;
}

.menu {
	display: none;
}

// スマホ版
@media screen and (max-width: 767px) {
	.nav-logo {
		display: block;
	}
	.g-navbar {
		display: none;
	}
	/*ボタン*/
	.hamburger_btn {
		display: block;
		position: fixed; /*常に最上部に表示したいので固定*/
		top: 0;
		right: 0;
		width: 70px;
		height: 72px;
		cursor: pointer;
		z-index: 50;
	}

	.hamburger_btn .line {
		position: absolute;
		top: 0;
		left: 20px;
		width: 32px;
		height: 2px;
		background: #333333;
		text-align: center;
	}

	.hamburger_btn .line_01 {
		top: 16px;
		transition: 0.4s ease;
	}
	.hamburger_btn .line_02 {
		top: 26px;
		transition: 0.4s ease;
	}
	.hamburger_btn .line_03 {
		top: 36px;
		transition: 0.4s ease;
	}


	.btn_line01 {
		transform: translateY(10px) rotate(-45deg);
		transition: 0.4s ease;
	}
	.btn_line02 {
		transition: 0.4s ease;
		opacity: 0;
	}
	.btn_line03 {
		transform: translateY(-10px) rotate(45deg);
		transition: 0.4s ease;
	}

	/*サイドバー*/
	.menu-enter-active, .menu-leave-active {
		transition: opacity 0.4s;
	}
	.menu-enter, .menu-leave-to {
		opacity: 0;
		}
	.menu-leave, .menu-enter-to{
		opacity: 1;
	}

	.menu li {
		list-style: none;
		line-height: 1;
		padding: 1rem;
	}
	.menu {
		display: block;
		background-color: rgba(197, 197, 197, 0.671);
		z-index: 30;
		padding: 2rem 1rem;
		position: fixed;
		width: 20rem;
		height: 80rem;
		top: 0;
		right: 0;
	}
	.menu a {
		color: rgb(66, 66, 66);
		text-decoration: none;
		font-size: 1.2rem;
		padding: 0 2rem;
	}
	.menu ul{
		margin: 1rem;
		padding: 0;
	}
}
</style>
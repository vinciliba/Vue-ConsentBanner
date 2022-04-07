<template>
	<vsa-list>
		<!-- Here you can use v-for to loop through items  -->
		<vsa-item>
			<vsa-heading> Your Privacy </vsa-heading>
			<vsa-content>
				<h3>Your privacy is important to us</h3>
				<p>
					Cookies are very small text files that are stored on your computer
					when you visit a website. We use cookies for a variety of purposes and
					to enhance your online experience on our website (for example, to
					remember your account login details).
				</p>
				<p>
					You can change your preferences and decline certain types of cookies
					to be stored on your computer while browsing our website.
				</p>

				<p>
					You can also remove any cookies already stored on your computer, but
					keep in mind that deleting cookies may prevent you from using parts of
					our website.
				</p>
			</vsa-content>
		</vsa-item>

		<vsa-item>
			<vsa-heading> Strictly necessary cookies </vsa-heading>
			<vsa-content>
				<h3>Strictly necessary cookies</h3>
				<p>
					These cookies are essential to provide you with services available
					through our website and to enable you to use certain features of our
					website.
				</p>

				<p>
					Without these cookies, we cannot provide you certain services on our
					website.
				</p>

				<ToggleButton @toggle_callBack="callback1" />

			</vsa-content>
		</vsa-item>

		<vsa-item>
			<vsa-heading> Functionality cookies </vsa-heading>
			<vsa-content>
				<h3>Functionality cookies</h3>
				<p>
					These cookies are used to provide you with a more personalized
					experience on our website and to remember choices you make when you
					use our website.
				</p>
				<p>
					For example, we may use functionality cookies to remember your
					language preferences or remember your login details.
				</p>
				<ToggleButton @toggle_callBack="callback2" />
			</vsa-content>
		</vsa-item>

		<vsa-item>
			<vsa-heading> Tracking cookies </vsa-heading>
			<vsa-content>
				<h3>Tracking cookies</h3>
				<p>
					These cookies are used to collect information to analyze the traffic
					to our website and how visitors are using our website.
				</p>
				<p>
					For example, these cookies may track things such as how long you spend
					on the website or the pages you visit which helps us to understand how
					we can improve our website site for you.
				</p>
				<p>
					The information collected through these tracking and performance
					cookies do not identify any individual visitor.
				</p>
				<ToggleButton @toggle_callBack="callback3" />
			</vsa-content>
		</vsa-item>

		<vsa-item>
			<vsa-heading> Targeting and advertising cookies </vsa-heading>
			<vsa-content>
				<h3>Targeting and advertising cookies</h3>
				<p>
					These cookies are used to show advertising that is likely to be of
					interest to you based on your browsing habits.
				</p>
				<p>
					These cookies, as served by our content and/or advertising providers,
					may combine information they collected from our website with other
					information they have independently collected relating to your web
					browser's activities across their network of websites.
				</p>
				<p>
					If you choose to remove or disable these targeting or advertising
					cookies, you will still see adverts but they may not be relevant to
					you.
				</p>
				<ToggleButton @toggle_callBack="callback4" />
			</vsa-content>
		</vsa-item>

		<vsa-item>
			<vsa-heading> More information </vsa-heading>
			<vsa-content>
				<h3>More information</h3>
				<p>
					For any queries in relation to our policy on cookies and your choices,
					please contact us.
				</p>
			</vsa-content>
		</vsa-item>
	</vsa-list>
</template>


<script>
	import {
		VsaList,
		VsaItem,
		VsaHeading,
		VsaContent
	} from "vue-simple-accordion";
	import "vue-simple-accordion/dist/vue-simple-accordion.css";
	import ToggleButton from './ToggleButton.vue'

	export default {
		name: "Accordion",
		components: {
			VsaList,
			VsaItem,
			VsaHeading,
			VsaContent,
			ToggleButton
		},

		methods: {
			callback1(status) {
				console.log("callback1", status);
			},
			callback2(status) {
				console.log("callback2", status);
			},
			callback3(status) {
				console.log("callback3", status);
			},
			callback4(status) {
				console.log("callback4", status);
			},
		}
	};
</script>

<style scoped>
	.vsa-list {
		--vsa-max-width: 720px;
		--vsa-min-width: 300px;
		--vsa-text-color: rgba(55, 55, 55, 1);
		--vsa-highlight-color: #0069ff;
		--vsa-bg-color: rgba(255, 255, 255, 1);
		--vsa-border-color: rgba(0, 0, 0, 0.2);
		--vsa-border-width: 1px;
		--vsa-border-style: solid;
		--vsa-heading-padding: 1rem 1rem;
		--vsa-content-padding: 1rem 1rem;
		--vsa-default-icon-size: 0.3;
	}
</style>

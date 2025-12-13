<script lang="ts">
	import { ArrowUpRight } from 'lucide-svelte';
</script>

<header class="w-full px-4 md:px-8 py-6 flex items-center justify-between text-[10px] font-medium tracking-wide uppercase border-b border-transparent fixed top-0 left-0 z-50 bg-white/90 backdrop-blur-sm transition-all duration-300">
	<div class="flex-1">
		<a href="/" class="text-xl font-bold tracking-tight text-primary-600">DND</a>
	</div>

	<nav class="hidden md:flex items-center gap-12 text-gray-500">
		<a href="#features" class="hover:text-black transition-colors">Features</a>
		<a href="#how-it-works" class="hover:text-black transition-colors">How It Works</a>
		<a href="#testimonials" class="hover:text-black transition-colors">Testimonials</a>
		<a href="#about" class="hover:text-black transition-colors">About</a>
	</nav>

	<div class="flex-1 flex justify-end items-center gap-6 md:gap-8">
		<a href="#pricing" class="flex items-center gap-1 hover:opacity-70 transition-opacity">
			Pricing
		</a>
		<a href="#start" class="flex items-center gap-1 bg-primary-600 text-white px-4 py-2 rounded-full hover:bg-primary-700 transition-colors">
			<ArrowUpRight size={14} />
			Start Creating
		</a>
	</div>
</header>

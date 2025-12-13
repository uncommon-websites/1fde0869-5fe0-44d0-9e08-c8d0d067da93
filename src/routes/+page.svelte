<script lang="ts">
	import Header from "$lib/components/Header.svelte";
	import { ArrowUpRight, ArrowRight, Zap, BookOpen, Users, Sparkles } from 'lucide-svelte';

	const features = [
		{ id: '01', name: 'AI-POWERED GENERATION', description: 'Create complete campaign modules from simple prompts in seconds' },
		{ id: '02', name: 'INSTANT PLAYABILITY', description: 'Every module is ready to run at your table immediately' },
		{ id: '03', name: 'COMPLETE MODULES', description: 'NPCs, encounters, maps, loot, and story hooks included' },
		{ id: '04', name: 'COMMUNITY SHARING', description: 'Share your modules and discover content from other DMs' },
		{ id: '05', name: 'CUSTOMIZABLE CONTENT', description: 'Edit and adapt any generated content to fit your campaign' },
		{ id: '06', name: 'TIME SAVING', description: 'Reduce prep time from hours to minutes' }
	];

	const testimonials = [
		{ 
			name: 'SARAH CHEN', 
			role: 'DUNGEON MASTER - 5 YEARS', 
			img: '/generated/image-excited-dungeon-master-reading-through-a-1765661247352-7.webp',
			quote: 'This tool saved me 10+ hours of prep time. My players had no idea the entire dungeon was AI-generated!'
		},
		{ 
			name: 'MARCUS RODRIGUEZ', 
			role: 'DUNGEON MASTER - 3 YEARS', 
			img: '/generated/image-dungeon-master-sitting-at-gaming-table-w-1765661226964-0.webp',
			quote: 'As a busy DM with a full-time job, this is a game-changer. I can finally run weekly sessions without the stress.'
		},
		{ 
			name: 'EMILY WATSON', 
			role: 'DUNGEON MASTER - 7 YEARS', 
			img: '/generated/image-excited-dungeon-master-reading-through-a-1765661247352-7.webp',
			quote: 'The quality is incredible. NPCs feel alive, encounters are balanced, and the story hooks are creative.'
		}
	];

	const steps = [
		{ number: '01', title: 'Describe Your Vision', description: 'Enter a simple prompt describing the module you need' },
		{ number: '02', title: 'AI Generates Content', description: 'Our AI creates a complete, playable module in seconds' },
		{ number: '03', title: 'Customize & Play', description: 'Edit as needed and bring it to your table immediately' }
	];
</script>

<div class="min-h-screen bg-white text-[#1A1A1A] font-sans selection:bg-primary-600 selection:text-white overflow-x-hidden">
	<Header />

	<main>
		<!-- Hero Section -->
		<section class="pt-12 md:pt-20 pb-10 px-4 md:px-8">
			<div class="flex flex-col md:flex-row justify-between items-start mb-12 md:mb-24 relative">
				<div class="max-w-[200px] text-[10px] leading-relaxed uppercase tracking-wide font-medium mt-2">
					<p>AI-powered D&D module generator that creates complete, playable campaign content instantly from your prompts.</p>
				</div>
				<h1 class="text-[14vw] md:text-[9rem] lg:text-[11rem] leading-[0.8] font-thin tracking-tighter text-right mt-8 md:mt-0 uppercase">
					Create <br />
					Epic
				</h1>
			</div>

			<!-- Hero Images -->
			<div class="grid grid-cols-5 gap-2 md:gap-4 mb-8 h-[30vh] md:h-[50vh]">
				<div class="overflow-hidden h-full">
					<img src="/generated/image-dungeon-master-sitting-at-gaming-table-w-1765661226964-0.webp" alt="Dungeon Master at table" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="/generated/image-close-up-of-colorful-polyhedral-dice-on--1765661231062-1.webp" alt="D&D dice" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="/generated/image-hand-drawn-fantasy-map-with-dungeon-layo-1765661233793-2.webp" alt="Fantasy map" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="/generated/image-group-of-friends-playing-dd-around-a-tab-1765661236652-3.webp" alt="D&D gaming group" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="/generated/image-stack-of-dd-rulebooks-and-campaign-guide-1765661239408-4.webp" alt="D&D books" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
			</div>

			<div class="flex flex-col md:flex-row justify-between items-start">
				<span class="text-[10px] uppercase tracking-wide font-medium mt-4 hidden md:block">Scroll</span>
				<h1 class="text-[14vw] md:text-[9rem] lg:text-[11rem] leading-[0.8] font-thin tracking-tighter text-right w-full uppercase">
					Modules <br />
					Instantly
				</h1>
			</div>
		</section>

		<!-- Features Section -->
		<section class="py-20 md:py-32 bg-gray-50" id="features">
			<div class="flex justify-center mb-16 md:mb-24">
				<span class="text-[10px] font-bold uppercase tracking-widest">Features</span>
			</div>

			<div class="border-t border-gray-300">
				{#each features as feature}
					<div class="group border-b border-gray-300 py-6 md:py-10 px-4 md:px-8 flex flex-col md:flex-row items-start md:items-center justify-between hover:bg-white transition-colors cursor-pointer">
						<span class="text-[10px] font-medium text-gray-500 w-8 md:w-12 mb-2 md:mb-0">/{feature.id}</span>
						<div class="flex-1 md:px-8">
							<h2 class="text-2xl md:text-5xl lg:text-6xl font-thin tracking-tight group-hover:text-primary-600 transition-all duration-300 uppercase mb-2">{feature.name}</h2>
							<p class="text-xs md:text-sm text-gray-600 max-w-2xl">{feature.description}</p>
						</div>
						<div class="flex items-center gap-1 text-[10px] font-medium uppercase opacity-0 group-hover:opacity-100 transition-opacity translate-x-[-10px] group-hover:translate-x-0 duration-300 mt-2 md:mt-0">
							<ArrowUpRight size={12} />
							Learn More
						</div>
					</div>
				{/each}
			</div>
		</section>

		<!-- How It Works Section -->
		<section class="py-20 px-4 md:px-8 bg-white" id="how-it-works">
			<div class="flex flex-col md:flex-row justify-between items-start mb-16 md:mb-24">
				<h2 class="text-4xl md:text-6xl font-light tracking-tight mb-8 md:mb-0 uppercase">How It Works</h2>
				<div class="max-w-xs text-[10px] leading-relaxed uppercase tracking-wide font-medium text-right md:text-left">
					<p>From prompt to playable module in seconds. Our AI handles the heavy lifting so you can focus on running an amazing game.</p>
				</div>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-3 gap-8 md:gap-12 mb-20">
				{#each steps as step}
					<div class="group">
						<div class="text-6xl md:text-8xl font-thin text-primary-600 mb-6 opacity-30 group-hover:opacity-100 transition-opacity">
							{step.number}
						</div>
						<h3 class="text-xl md:text-2xl font-medium uppercase tracking-tight mb-4">{step.title}</h3>
						<p class="text-sm text-gray-600 leading-relaxed">{step.description}</p>
					</div>
				{/each}
			</div>

			<!-- Process Visualization -->
			<div class="bg-gray-50 rounded-2xl p-8 md:p-12">
				<div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
					<div>
						<h3 class="text-2xl md:text-4xl font-light tracking-tight mb-6 uppercase">Example Prompt</h3>
						<div class="bg-white border border-gray-200 rounded-lg p-6 mb-6">
							<p class="text-sm italic text-gray-700">"Create a haunted mansion module for level 5 characters with a mystery to solve and a ghostly villain."</p>
						</div>
						<div class="flex items-start gap-3 text-xs text-gray-600">
							<Sparkles size={16} class="text-primary-600 mt-1" />
							<p>AI generates complete module with NPCs, encounters, maps, treasure, and story hooks in under 30 seconds.</p>
						</div>
					</div>
					<div class="overflow-hidden rounded-lg">
						<img src="/generated/image-gaming-table-setup-with-battle-mat-minia-1765661253115-9.webp" alt="Gaming table setup" class="w-full h-full object-cover" />
					</div>
				</div>
			</div>
		</section>

		<!-- Testimonials Section -->
		<section class="py-20 px-4 md:px-8 bg-gray-50" id="testimonials">
			<div class="flex flex-col lg:flex-row mb-16 gap-12 lg:gap-24">
				<div class="flex-1">
					<h2 class="text-4xl md:text-6xl font-light tracking-tight uppercase">Loved by DMs</h2>
				</div>
				<div class="flex-1">
					<h2 class="text-3xl md:text-5xl font-light tracking-tight mb-8 text-left uppercase leading-tight">Saving hours<br/>every week</h2>
					<div class="grid grid-cols-1 md:grid-cols-2 gap-8 text-[10px] leading-relaxed uppercase tracking-wide font-medium">
						<p>Dungeon Masters across the world are using DND to create engaging campaign content without spending hours on prep work.</p>
						<p>From one-shots to full campaigns, our AI-powered generator helps DMs focus on what matters most: creating memorable experiences for their players.</p>
					</div>
					<a href="#start" class="inline-flex items-center gap-1 text-[10px] font-medium uppercase mt-8 hover:opacity-60 transition-opacity">
						<ArrowUpRight size={10} />
						Start Creating
					</a>
				</div>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
				{#each testimonials as testimonial}
					<div class="bg-white rounded-lg p-8 group hover:shadow-lg transition-shadow">
						<div class="aspect-square overflow-hidden mb-6 bg-gray-200 rounded-lg">
							<img src={testimonial.img} alt={testimonial.name} class="w-full h-full object-cover" />
						</div>
						<p class="text-sm text-gray-700 mb-6 italic leading-relaxed">"{testimonial.quote}"</p>
						<h3 class="text-xs font-bold uppercase tracking-wide mb-1">{testimonial.name}</h3>
						<p class="text-[10px] text-gray-500 uppercase tracking-wide">{testimonial.role}</p>
					</div>
				{/each}
			</div>
		</section>

		<!-- About Section -->
		<section class="py-20 px-4 md:px-8 bg-white" id="about">
			<div class="max-w-6xl mx-auto">
				<div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center mb-16">
					<div>
						<h2 class="text-4xl md:text-6xl font-light tracking-tight mb-8 uppercase">About DND</h2>
						<div class="space-y-4 text-sm text-gray-700 leading-relaxed">
							<p>DND is revolutionizing how Dungeon Masters create campaign content. We understand that prep time is the biggest barrier to running great D&D sessions.</p>
							<p>Our AI-powered module generator creates complete, playable content in seconds - from NPCs and encounters to maps and story hooks. Everything you need to run an amazing session, instantly.</p>
							<p>Starting with D&D players, we're capturing the $15B tabletop gaming market through AI-generated modules and community sharing. Join thousands of DMs who are already saving hours every week.</p>
						</div>
					</div>
					<div class="overflow-hidden rounded-lg">
						<img src="/generated/image-dungeon-master-behind-dm-screen-with-lap-1765661241933-5.webp" alt="DM with laptop" class="w-full h-full object-cover" />
					</div>
				</div>

				<!-- Stats -->
				<div class="grid grid-cols-2 md:grid-cols-4 gap-8 py-12 border-t border-gray-200">
					<div class="text-center">
						<div class="text-4xl md:text-5xl font-light text-primary-600 mb-2">10+</div>
						<div class="text-xs uppercase tracking-wide text-gray-600">Hours Saved</div>
					</div>
					<div class="text-center">
						<div class="text-4xl md:text-5xl font-light text-primary-600 mb-2">1000s</div>
						<div class="text-xs uppercase tracking-wide text-gray-600">Modules Created</div>
					</div>
					<div class="text-center">
						<div class="text-4xl md:text-5xl font-light text-primary-600 mb-2">30s</div>
						<div class="text-xs uppercase tracking-wide text-gray-600">Generation Time</div>
					</div>
					<div class="text-center">
						<div class="text-4xl md:text-5xl font-light text-primary-600 mb-2">100%</div>
						<div class="text-xs uppercase tracking-wide text-gray-600">Playable Content</div>
					</div>
				</div>
			</div>
		</section>

		<!-- CTA Section -->
		<section class="py-32 px-4 md:px-8 bg-primary-600 text-white text-center" id="start">
			<span class="text-[10px] font-medium uppercase tracking-widest mb-6 block opacity-80">Ready to Save Time?</span>
			<h2 class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mb-12 uppercase">
				Start Creating <br />
				Epic Modules
			</h2>
			<a href="#pricing" class="inline-block bg-white text-primary-600 px-10 py-4 rounded-full text-[10px] font-bold uppercase tracking-widest hover:bg-gray-100 transition-colors">
				Get Started Free
			</a>
		</section>

		<!-- Bottom Gallery -->
		<div class="grid grid-cols-2 md:grid-cols-5 h-[60vh]">
			<div class="overflow-hidden">
				<img src="/generated/image-close-up-of-colorful-polyhedral-dice-on--1765661231062-1.webp" alt="D&D dice" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="/generated/image-fantasy-character-miniatures-arranged-on-1765661244389-6.webp" alt="Miniatures" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="/generated/image-hand-drawn-fantasy-map-with-dungeon-layo-1765661233793-2.webp" alt="Fantasy map" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="/generated/image-dd-player-character-sheet-with-dice-and--1765661250280-8.webp" alt="Character sheet" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden hidden md:block">
				<img src="/generated/image-group-of-friends-playing-dd-around-a-tab-1765661236652-3.webp" alt="Gaming group" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
		</div>

		<!-- Footer Marquee -->
		<div class="overflow-hidden py-6 border-b border-gray-200 bg-white">
			<div class="whitespace-nowrap animate-marquee flex">
				<span class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mx-4 uppercase">Create Epic Modules Instantly — AI-Powered D&D Content — Create Epic Modules Instantly — </span>
				<span class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mx-4 uppercase">Create Epic Modules Instantly — AI-Powered D&D Content — Create Epic Modules Instantly — </span>
			</div>
		</div>
	</main>

	<footer class="px-4 md:px-8 py-12 text-[10px] font-medium uppercase tracking-wide bg-white">
		<div class="flex flex-col md:flex-row justify-between items-start md:items-end gap-12 md:gap-8">
			<div class="flex flex-col gap-3">
				<a href="#features" class="hover:opacity-60">Features</a>
				<a href="#how-it-works" class="hover:opacity-60">How It Works</a>
				<a href="#testimonials" class="hover:opacity-60">Testimonials</a>
				<a href="#about" class="hover:opacity-60">About</a>
				<a href="#pricing" class="hover:opacity-60">Pricing</a>
			</div>

			<div class="text-left md:text-center">
				<p class="text-lg md:text-2xl font-normal tracking-tight mb-6">HELLO@DNDMODULES.AI</p>
				<div class="flex gap-4 justify-center">
					<a href="https://reddit.com/r/DnD" target="_blank" class="hover:text-primary-600 transition-colors">Reddit</a>
					<a href="#twitter" class="hover:text-primary-600 transition-colors">Twitter</a>
					<a href="#discord" class="hover:text-primary-600 transition-colors">Discord</a>
				</div>
			</div>

			<div class="flex flex-col gap-3 text-left md:text-right">
				<a href="#privacy" class="hover:opacity-60">Privacy Policy</a>
				<a href="#terms" class="hover:opacity-60">Terms & Conditions</a>
			</div>
		</div>

		<div class="flex flex-col md:flex-row justify-between items-center mt-20 pt-8 border-t border-gray-200 text-[10px] text-gray-400 gap-4">
			<p>©2024 DND MODULE GENERATOR. ALL RIGHTS RESERVED</p>
			<div class="flex items-center gap-1">
				<span class="text-primary-600 text-lg font-bold tracking-tight">DND</span>
			</div>
			<p>AI-POWERED D&D CONTENT</p>
		</div>
	</footer>
</div>

<style>
	@keyframes marquee {
		0% { transform: translateX(0); }
		100% { transform: translateX(-50%); }
	}
	.animate-marquee {
		animation: marquee 30s linear infinite;
	}
</style>


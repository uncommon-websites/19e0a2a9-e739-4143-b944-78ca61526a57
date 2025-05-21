<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
		{
			title: "Flexible Work",
			description: "Remote-first with flexible hours that respect work-life balance.",
			icon: IconBriefcase
		},
		{
			title: "Growth Opportunities",
			description: "Continuous learning with mentorship and education stipends.",
			icon: IconUsers
		},
		{
			title: "Comprehensive Benefits",
			description: "Health coverage, retirement plans, and generous paid time off.",
			icon: IconHeart
		}
	];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Wei Chen",
    position: "AI engineer",
    company: "Engineering Team",
    quote:
      "From our first all-hands hackathon where I pitched a feature, I knew Headscout AI valued every voice. Building the AI-powered outreach model alongside recruiters now automates 85% of outreach tasks and cuts candidate screening time by 40%.",
    image: "/generated/image-a-candid-headshot-of-an-asian-male-engin.webp"
  },
  {
    name: "Amina Bakare",
    position: "Senior product manager",
    company: "Product Team",
    quote:
      "At Headscout AI, when I learned recruiters were spending half their day toggling between spreadsheets, I spearheaded our unified sourcing and tracking dashboard. In six months it reduced time-to-hire by 25% and I coached three new team members on end-to-end product strategy. Leading this project has been the fastest growth I’ve experienced in my career.",
    image: "/generated/image-a-professional-portrait-of-a-black-femal.webp"
  },
  {
    name: "Rowan Hayes (they/them)",
    position: "Customer success specialist",
    company: "Support Team",
    quote:
      "Joining as a support specialist, I immediately appreciated the flexible remote-first setup and open communication channels. Building our automated interview scheduler saved recruiters 20 hours a week, and I set my own hours while collaborating with engineering to fine-tune it. The trust and autonomy here keep me motivated every day.",
    image: "/generated/image-a-relaxed-and-confident-white-nonbinary-.webp"
  }
];

	const processSteps = [
		{
			step: 1,
			title: "Apply",
			description:
				"Submit your application through our careers portal with your resume and portfolio."
		},
		{
			step: 2,
			title: "Interview",
			description: "Meet with our team to discuss your experience, skills, and career aspirations."
		},
		{
			step: 3,
			title: "Welcome aboard",
			description: "Join our team and start your journey building the future with us."
		}
	];

	const values = [
		{
			icon: IconHeart,
			title: "Passion",
			description: "We're driven by a shared passion for innovation and excellence."
		},
		{
			icon: IconUsers,
			title: "Collaboration",
			description: "We believe in teamwork and collaboration to achieve great things."
		},
		{
			icon: IconGlobe,
			title: "Global Impact",
			description: "We're committed to making a positive impact on the world."
		}
	];
</script>

<!-- Hero Section -->

<SecondaryHero
  title="Engineers and designers, transform hiring"
  subtitle="Work flexibly with an AI-native team and cut hiring time. Thrive alongside supportive peers, shape the future of the hiring industry, and make meaningful impact."
  imageSrc="/generated/image-a-diverse-team-collaborating-in-a-modern.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Architect our AI engine that slashes hiring time from months to weeks by automating 85% of screening tasks and delivering smarter candidate experiences." />

	<div class="prose max-w-3xl mx-auto text-lg mt-10 mb-10">
		<ul class="list-disc pl-5">
			<li>Tackle the hardest talent gaps at top-tier startups, designing solutions that connect engineering, product, and executive leaders with world-class candidates.</li>
			<li>Shape our product vision and equity upside—own 0.5–1% equity, drive strategy alongside founder Grace Juba and advisor Jon Holland, and scale our seed-stage startup backed by top-tier VCs.</li>
			<li>Accelerate your career in a funded remote-first environment by joining our 15-person team, enjoying flexible work, rapid role growth, and direct impact as we bring our early-access recruiting platform to market.</li>
		</ul>
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>

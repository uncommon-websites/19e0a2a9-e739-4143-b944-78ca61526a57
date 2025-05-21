<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials={[
    {
      name: "Anika Reyes",
      position: "Founder and CEO",
      company: "Omnisync",
      quote:
        "Headscout AI paid for itself on our first placement, cutting our time to hire to 18 days and slashing recruiting costs by 70% compared to external agencies.",
      image: "/generated/image-a-professional-african-american-woman-sm.webp"
    },
    {
      name: "Jamal Thompson",
      position: "Chief Operating Officer",
      company: "Driftbase",
      quote:
        "As a lean startup with no in-house recruiter, we automated 85% of our outreach and candidate tracking, hiring engineers 50% faster and saving 60% on recruiting expenses.",
      image: "/generated/image-a-professional-asian-man-in-a-relaxed-ca.webp"
    },
    {
      name: "Maya Chen",
      position: "Vice President of People",
      company: "AlloyOS",
      quote:
        "I was skeptical about AI for executive hiring, but Headscout AI delivered a fully qualified shortlist in five days at 20% of the cost of a retained search firm.",
      image: "/generated/image-a-professional-middle-eastern-woman-wear.webp"
    }
  ]}
/>

<CallToAction
  title="Cut your time to hire from months to weeks"
  subtitle="Automate 85% of recruiting. Start in minutes."
  description="Join our waitlist today and see how fast, easy, and cost-effective hiring can be for founders and tech leaders."
  imageSrc="/generated/image-a-cheerful-business-professional-in-a-mo.webp"
  callsToAction={[
    { href: '/waitlist', label: 'Join the waitlist', variant: 'primary' },
    { href: '/contact', label: 'Talk to sales', variant: 'secondary' }
  ]}
/>


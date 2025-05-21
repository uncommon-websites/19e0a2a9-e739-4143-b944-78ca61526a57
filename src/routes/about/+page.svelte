<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
  {
    title: "AI-first mindset, continuous innovation",
    description:
      "We build, test and refine our own AI tools. By automating routine tasks ourselves, we free each other to focus on creative sourcing, share insights across teams and grow our AI expertise together. Team members are encouraged to propose and pilot new ideas that push our forward-thinking vision."
  },
  {
    title: "Rapid experimentation, agile impact",
    description:
      "We break big challenges into small experiments, gather feedback in hours and adjust by evening. This pace keeps us nimble, accelerates learning and drives real-world impact for hiring."
  },
  {
    title: "Open collaboration and inclusive growth",
    description:
      "We speak plainly, share honest feedback and collaborate on challenges. Regular hackathons, peer reviews and mentorship circles help us learn from each other. We respect diverse perspectives and foster a supportive environment where every voice counts."
  },
  {
    title: "Purpose-driven hiring, measurable results",
    description:
      "Every project links back to helping startups find top talent faster. We combine our recruiting know-how with AI experiments and customer stories to deliver measurable results and shape the future of hiring."
  }
];
</script>

<SecondaryHero
  title="Rethink hiring with ai for ambitious tech teams"
  subtitle="Automate 85% of recruiting tasks, hire in weeks"
  imageSrc="/mockups/airport-screen-1747837377731.png"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"For nearly a decade, our founder Grace Juba worked as an executive recruiter, helping fast-growing startups make complex, high-stakes hires across engineering, product, and leadership. She saw firsthand how much time teams spent buried in repetitive tasks—copying links, rewriting messages, tracking candidates across disjointed tools. Hiring great people was critical, but the process was painfully slow and manual. It was clear to her: there had to be a better way.",
		"That was the starting point for Headscout AI. We built the platform we wished existed—one that actually speeds up hiring instead of getting in the way. By automating 85% of the busywork, Headscout AI helps teams source, engage, track, and close candidates in a fraction of the time. It’s not about replacing recruiters—it’s about giving them better tools to move fast and make smart decisions without burning out.",
		"Our goal is simple: help teams hire smarter and faster so they can get back to building. We believe hiring shouldn’t hold companies back—it should fuel their growth. With Headscout AI, top talent doesn’t take months to find. It takes weeks."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
  stakeholderType="team"
  title="Our team."
  subtitle="Your partners in hiring."
  stakeholders={[
    {
      name: "Grace Juba",
      position: "Founder & CEO",
      bio: "Grace has spent nearly a decade leading high-stakes talent searches for fast-growing tech companies. She’s placed over 200 leaders and specialists across engineering, product, and executive roles—consistently cutting hiring cycles from months to weeks. Now she’s combining that expertise with AI at Headscout AI, automating 85 percent of repetitive tasks to streamline sourcing, engagement, tracking, and hiring.",
      image: "/generated/image-a-professional-headshot-of-a-female-saas.webp"
    },
    {
      name: "Jon Holland",
      position: "Advisor",
      bio: "Jon brings more than 15 years of experience scaling SaaS and consumer products businesses. He built high-performing teams at Wells Fargo and JPM Chase, led five successful exits, and raised over $125 million in capital. As a strategic advisor, he applies his operational finance and growth expertise to guide Headscout AI’s roadmap and fuel our next phase of expansion.",
      image: "/generated/image-a-professional-headshot-of-a-male-saas-a.webp"
    }
  ]}
/>




<!-- CTA Section -->
<CallToAction
  title="Get ahead of the hiring curve"
  subtitle="Join the waitlist or connect with us"
  description="Headscout AI automates 85% of repetitive recruiting tasks and cuts hiring time from months to weeks. If you’re a tech startup or venture-backed company making high-stakes hires, join the waitlist for early access or reach out to learn more and connect with us."
  callsToAction={[
    {
      href: '/waitlist',
      label: 'Join waitlist',
      variant: 'primary'
    },
    {
      href: '/contact',
      label: 'Contact us',
      variant: 'secondary'
    }
  ]}
/>

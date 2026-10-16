<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
const activeAgent = ref(0)
const agents = [
  { icon: '✳', name: 'Customer Support', detail: 'Answers questions around the clock', tag: 'CHAT · EMAIL · WHATSAPP' },
  { icon: '⌘', name: 'Workflow Agents', detail: 'Connects tools and gets work done', tag: 'N8N · MAKE · APIS' },
  { icon: '⌕', name: 'Research Agents', detail: 'Finds information and turns it into insights', tag: 'WEB · DATA · REPORTS' },
  { icon: '◈', name: 'Custom AI Agents', detail: 'Built around your unique business process', tag: 'YOUR RULES · YOUR TOOLS' },
]
const services = [
  { icon: '✳', title: 'AI Agents', text: 'Helpful AI assistants for support, research, lead qualification and everyday tasks.', tag: 'THINK · RESPOND · ACT' },
  { icon: '⌘', title: 'Workflow Automation', text: 'Connect your apps and remove repetitive work with n8n, Make and APIs.', tag: 'CONNECT · AUTOMATE' },
  { icon: '◉', title: 'Customer Support Bots', text: 'Give customers faster answers across your website and messaging channels.', tag: '24/7 CUSTOMER CARE' },
  { icon: '⤢', title: 'Web Applications', text: 'Build modern, scalable applications using Laravel, Vue and reliable APIs.', tag: 'PHP · LARAVEL · VUE' },
]
const projects = [
  { num: '01', title: 'AI Automation System', type: 'AI AUTOMATION', desc: 'A smart workflow that processes form submissions, routes information and sends useful alerts.', stack: ['n8n', 'Google Sheets', 'Email'], icon: '⌘' },
  { num: '02', title: 'Subscription SaaS Platform', type: 'SAAS · PAYMENTS', desc: 'Subscription plans, access control and payment flows designed around business needs.', stack: ['Laravel', 'Vue.js', 'Stripe'], icon: '◈' },
  { num: '03', title: 'E-commerce Experience', type: 'WEB APPLICATION', desc: 'A streamlined storefront with product management, checkout integrations and admin tools.', stack: ['Laravel', 'Vue.js', 'MySQL'], icon: '▧' },
  { num: '04', title: 'Lead Management System', type: 'BUSINESS SOFTWARE', desc: 'A central place to organize leads, follow up with prospects and track the sales pipeline.', stack: ['PHP', 'Vue.js', 'MySQL'], icon: '⌁' },
]
const skills = [
  { icon: 'Ｐ', name: 'PHP', sub: 'Backend' }, { icon: 'L', name: 'Laravel', sub: 'Framework' }, { icon: 'V', name: 'Vue.js', sub: 'Frontend' },
  { icon: '⌘', name: 'n8n', sub: 'Automation' }, { icon: 'M', name: 'Make', sub: 'Automation' }, { icon: '◉', name: 'AI & LLMs', sub: 'Intelligence' },
  { icon: '▤', name: 'MySQL', sub: 'Database' }, { icon: '↗', name: 'REST APIs', sub: 'Integrations' },
]
const closeMenu = () => { menuOpen.value = false }
</script>

<template>
  <div class="site-shell">
    <div class="ambient ambient-one"></div><div class="ambient ambient-two"></div>
    <header class="topbar">
      <a class="brand" href="#home" @click="closeMenu"><span class="brand-mark">M<span>A</span></span><span class="brand-copy"><b>MUBASHAR AYUB</b><small>PHP · LARAVEL · VUE · AI AUTOMATION</small></span></a>
      <button class="menu-toggle" aria-label="Toggle navigation" @click="menuOpen = !menuOpen">{{ menuOpen ? '✕' : '☰' }}</button>
      <nav :class="['nav-links', { 'nav-open': menuOpen }]">
        <a href="#home" @click="closeMenu">Home</a><a href="#about" @click="closeMenu">About</a><a href="#services" @click="closeMenu">Services</a><a href="#skills" @click="closeMenu">Skills</a><a href="#projects" @click="closeMenu">Projects</a><a href="#contact" @click="closeMenu">Contact</a>
      </nav>
      <a class="nav-cta" href="#contact">Let's talk <span>↗</span></a>
    </header>

    <main>
      <section id="home" class="hero section-wrap">
        <div class="hero-copy">
          <div class="eyebrow"><span class="status-dot"></span> SOFTWARE ENGINEER & AI AUTOMATION SPECIALIST</div>
          <h1>Build <span class="gradient-text">AI Agents</span><br />That Work <span class="outline-text">For You.</span></h1>
          <p class="hero-kicker">Turning ideas into <strong>smart digital solutions.</strong></p>
          <p class="hero-description">I build intelligent AI agents, automated workflows and modern web applications that save time, reduce manual work and help businesses grow.</p>
          <div class="hero-pills"><span><i>✳</i> AI Agents</span><span><i>⌘</i> Workflow Automation</span><span><i>〈〉</i> Web Development</span></div>
          <div class="hero-actions"><a class="button button-primary" href="#projects">Explore my work <span>↗</span></a><a class="button button-ghost" href="#about"><span>⌄</span> Discover my world</a></div>
          <div class="availability"><span class="pulse-dot"></span> Available for selected projects <span class="availability-line"></span><span class="availability-muted">REMOTE · WORLDWIDE</span></div>
        </div>
        <div class="hero-art" aria-label="Futuristic science fiction landscape illustration">
          <div class="hero-image"></div><div class="hero-image-shade"></div>
          <div class="planet-orbit orbit-a"></div><div class="planet-orbit orbit-b"></div>
          <div class="hud-card hud-status"><div class="hud-label"><span class="mini-orb">✳</span> AGENT STATUS</div><div class="hud-value">Autonomy <b>ONLINE</b></div><div class="hud-bars"><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i></div><small>WORKFLOW EXECUTION // 024</small></div>
          <div class="hud-card hud-agent"><span class="hud-icon">◈</span><div><b>AI AGENTS</b><small>Analyze · Decide · Act</small></div><span class="live-tag">LIVE</span><div class="agent-line"></div><div class="agent-line short"></div></div>
          <div class="floating-label label-left"><span class="label-symbol">⌘</span><span><b>CONNECTED SYSTEMS</b><small>One intelligent ecosystem</small></span></div>
          <div class="floating-label label-right"><span class="label-symbol">↗</span><span><b>IDEA → IMPACT</b><small>Built for what comes next</small></span></div>
          <div class="hero-coordinates">31° 32' N&nbsp;&nbsp; 74° 21' E <span> / </span> FUTURE SYSTEMS</div>
        </div>
        <div class="hero-bottom-line"><span>SCROLL TO EXPLORE</span><span class="scroll-line"></span><span>01 — 06</span></div>
      </section>

      <section id="services" class="section section-wrap services-section">
        <div class="section-heading"><div><div class="eyebrow">WHAT I CREATE <span class="heading-index">/ 01</span></div><h2>Technology with<br /><span class="gradient-text">a purpose.</span></h2></div><p>Less repetitive work. More room for the ideas that move your business forward.</p></div>
        <div class="service-grid"><article v-for="(service, index) in services" :key="service.title" class="service-card"><div class="service-top"><span class="service-icon">{{ service.icon }}</span><span class="card-index">0{{ index + 1 }}</span></div><h3>{{ service.title }}</h3><p>{{ service.text }}</p><div class="service-footer"><span>{{ service.tag }}</span><a href="#contact" :aria-label="'Discuss ' + service.title">↗</a></div></article></div>
      </section>

      <section class="agent-feature section-wrap">
        <div class="feature-grid-bg"></div><div class="feature-intro"><div class="eyebrow"><span class="status-dot"></span> FEATURED CAPABILITY</div><h2>Meet your next<br /><span class="gradient-text">digital teammate.</span></h2><p>AI agents that do more than answer questions. They can understand a task, work with your tools and help move real work forward.</p><a class="text-link" href="#contact">Let's design your agent <span>↗</span></a></div>
        <div class="agent-core-wrap"><div class="core-ring ring-one"></div><div class="core-ring ring-two"></div><div class="core-ring ring-three"></div><div class="agent-core"><span>✳</span><small>AI</small></div><span class="node node-one">✉</span><span class="node node-two">◉</span><span class="node node-three">⌘</span><span class="node node-four">▤</span><span class="node node-five">↗</span><span class="node node-six">◈</span><div class="core-caption">INTELLIGENCE<br /><b>IN MOTION</b></div></div>
        <div class="agent-selector"><div class="selector-title">CHOOSE AN AGENT <span>↘</span></div><button v-for="(agent, index) in agents" :key="agent.name" :class="['agent-option', { selected: activeAgent === index }]" @click="activeAgent = index"><span class="option-icon">{{ agent.icon }}</span><span class="option-copy"><b>{{ agent.name }}</b><small>{{ agent.detail }}</small></span><span class="option-arrow">{{ activeAgent === index ? '●' : '↗' }}</span></button><div class="agent-detail"><small>{{ agents[activeAgent].tag }}</small><p>{{ agents[activeAgent].detail }} — designed around the way your business works.</p></div></div>
      </section>

      <section class="section section-wrap workflow-section"><div class="section-heading"><div><div class="eyebrow">THE PROCESS <span class="heading-index">/ 02</span></div><h2>From idea to impact<br /><span class="gradient-text">in three steps.</span></h2></div><p>Practical automation, built around your current tools and the outcomes you actually need.</p></div>
        <div class="workflow-track"><div class="workflow-line"></div><article class="workflow-step"><span class="step-number">01</span><div class="step-icon">⌘</div><h3>Connect your tools</h3><p>Bring your apps, data and existing workflows into one connected system.</p><span class="step-meta">INPUT / CONNECT</span></article><article class="workflow-step"><span class="step-number">02</span><div class="step-icon step-icon-active">✳</div><h3>Build with intelligence</h3><p>Design the logic, AI prompts and automations that make the process work.</p><span class="step-meta">THINK / AUTOMATE</span></article><article class="workflow-step"><span class="step-number">03</span><div class="step-icon">↗</div><h3>Launch and improve</h3><p>Test the flow, monitor outcomes and refine it as your business grows.</p><span class="step-meta">OUTPUT / OPTIMIZE</span></article></div>
      </section>

      <section id="projects" class="section section-wrap projects-section"><div class="section-heading"><div><div class="eyebrow">SELECTED WORK <span class="heading-index">/ 03</span></div><h2>Ideas made <span class="gradient-text">real.</span></h2></div><a class="text-link" href="#contact">Have a project in mind? <span>↗</span></a></div><div class="project-grid"><article v-for="project in projects" :key="project.num" class="project-card"><div class="project-visual"><span class="project-number">{{ project.num }} / 04</span><div class="project-orbit"><span>{{ project.icon }}</span></div><div class="project-ui-lines"><i></i><i></i><i></i></div><span class="project-type">{{ project.type }}</span></div><div class="project-content"><div class="project-title-row"><h3>{{ project.title }}</h3><span class="project-arrow">↗</span></div><p>{{ project.desc }}</p><div class="tech-tags"><span v-for="tech in project.stack" :key="tech">{{ tech }}</span></div></div></article></div><p class="project-note"><span class="status-dot"></span> Selected concepts and project categories — replace these with your live demos and verified case studies.</p></section>

      <section id="about" class="section section-wrap about-section"><div class="about-visual"><div class="about-visual-grid"></div><div class="about-monogram">M<span>A</span></div><div class="about-scan"></div><div class="about-visual-caption"><span>IDENTITY / 001</span><b>BUILDER OF<br />DIGITAL FUTURES</b></div><div class="about-orb orb-top"></div><div class="about-orb orb-bottom"></div></div><div class="about-copy"><div class="eyebrow">A LITTLE ABOUT ME <span class="heading-index">/ 04</span></div><h2>Engineer by craft.<br /><span class="gradient-text">Curious by nature.</span></h2><p>I'm Mubashar Ayub, a software engineer working across AI automation and full-stack web development. I combine practical engineering with a future-focused mindset to create tools that solve real problems.</p><p>From Laravel applications and Vue interfaces to AI agents and connected workflows, I enjoy turning complicated processes into experiences that feel simple.</p><div class="stats-grid"><div><b>5<span>+</span></b><small>Years building<br />digital products</small></div><div><b>AI<span>+</span></b><small>Automation-first<br />mindset</small></div><div><b>∞</b><small>Curiosity for<br />what comes next</small></div></div><a class="button button-ghost" href="#contact">Let's work together <span>↗</span></a></div></section>

      <section id="skills" class="section section-wrap skills-section"><div class="section-heading"><div><div class="eyebrow">MY TOOLKIT <span class="heading-index">/ 05</span></div><h2>Built with the <span class="gradient-text">right tools.</span></h2></div><p>A mix of proven engineering foundations and modern AI automation technologies.</p></div><div class="skills-layout"><div class="skill-grid"><article v-for="skill in skills" :key="skill.name" class="skill-card"><span class="skill-symbol">{{ skill.icon }}</span><b>{{ skill.name }}</b><small>{{ skill.sub }}</small></article></div><div class="code-panel"><div class="code-panel-top"><span><i></i><i></i><i></i></span><small>future.workflow.js</small><span class="code-live">● LIVE</span></div><pre><span class="code-purple">const</span> future = <span class="code-blue">async</span> () =&gt; {
  <span class="code-purple">const</span> ideas = <span class="code-green">'your vision'</span>
  <span class="code-purple">const</span> tools = [<span class="code-green">'Laravel'</span>, <span class="code-green">'Vue'</span>, <span class="code-green">'AI'</span>]

  <span class="code-purple">return</span> build({
    ideas,
    tools,
    impact: <span class="code-green">'real results'</span>
  })
}</pre><div class="code-panel-foot"><span>● SYSTEM READY</span><span>BUILD · AUTOMATE · EVOLVE</span></div></div></div></section>

      <section id="contact" class="contact-section section-wrap"><div class="contact-stars"></div><div class="contact-content"><div class="eyebrow">YOUR NEXT CHAPTER STARTS HERE</div><h2>Have a bold idea?<br /><span class="gradient-text">Let's build it.</span></h2><p>Tell me what you're imagining — an AI agent, a smarter workflow or a web application built to scale.</p><div class="contact-actions"><a class="button button-primary" href="mailto:hello@example.com?subject=Let's%20build%20something">Start a conversation <span>↗</span></a><a class="button button-ghost" href="https://wa.me/000000000000" target="_blank" rel="noreferrer">WhatsApp <span>↗</span></a></div><small class="replace-note">Before publishing: update the email and WhatsApp link in src/App.vue.</small></div><div class="contact-visual"><div class="contact-planet"></div><div class="contact-planet-ring"></div><span class="contact-signal signal-one"></span><span class="contact-signal signal-two"></span><span class="contact-signal signal-three"></span><div class="contact-visual-label">NEXT STOP <b>THE FUTURE</b></div></div></section>
    </main>

    <footer class="footer section-wrap"><a class="brand footer-brand" href="#home"><span class="brand-mark">M<span>A</span></span><span class="brand-copy"><b>MUBASHAR AYUB</b><small>ENGINEERING WHAT'S NEXT</small></span></a><div class="footer-links"><a href="#about">About</a><a href="#services">Services</a><a href="#projects">Projects</a><a href="#contact">Contact</a></div><div class="social-links"><a href="https://www.linkedin.com/" aria-label="LinkedIn" target="_blank" rel="noreferrer">in</a><a href="https://github.com/" aria-label="GitHub" target="_blank" rel="noreferrer">⌘</a><a href="mailto:hello@example.com" aria-label="Email">✉</a></div><div class="copyright">© {{ new Date().getFullYear() }} Mubashar Ayub<br /><span>Code. Automate. Build the future.</span></div></footer>
  </div>
</template>

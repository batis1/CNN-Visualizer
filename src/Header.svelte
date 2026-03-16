<script>
  export let links = [
    {
      href: "https://arxiv.org/abs/2004.15004",
      title: "Research paper",
      icon: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path><polyline points="14 2 14 8 20 8"></polyline><line x1="16" y1="13" x2="8" y2="13"></line><line x1="16" y1="17" x2="8" y2="17"></line><polyline points="10 9 9 9 8 9"></polyline></svg>',
      alt: "pdf icon",
    },
    {
      href: "https://youtu.be/HnWIHWFbuUQ",
      title: "Demo video",
      icon: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="6" width="20" height="12" rx="2" ry="2"></rect><polygon points="10 15 15 12 10 9 10 15"></polygon></svg>',
      alt: "youtube icon",
    },
    {
      href: "https://github.com/poloclub/cnn-explainer",
      title: "Open-source code",
      icon: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path></svg>',
      alt: "github icon",
    },
  ];
</script>

<header class="app-header">
  <div class="top-bar">
    <div class="brand-block">
      <div class="brand-row">
        <div class="brand-mark">CNN EXPLAINER</div>
      </div>
      <div class="brand-subtitle">
        Learn Convolutional Neural Network (CNN) in your browser!
      </div>
    </div>
    <nav class="icon-links" aria-label="Project links">
      {#each links as link}
        <a
          class="icon-link"
          href={link.href}
          target="_blank"
          rel="noreferrer"
          title={link.title}
          aria-label={link.title}
        >
          {@html link.icon}
        </a>
      {/each}
    </nav>
  </div>
</header>

<style>
  :global(*) {
    box-sizing: border-box;
  }

  .app-header {
    width: 100%;
    background: #ffffff;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
      Helvetica, Arial, sans-serif;
  }
  .top-bar {
    padding: 16px 24px;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 20px;
  }
  .brand-block {
    display: flex;
    flex-direction: column;
    gap: 4px;
    min-width: 0;
  }
  .brand-row {
    display: flex;
    align-items: baseline;
    gap: 16px;
    flex-wrap: wrap;
    margin-bottom: 2px;
  }
  .brand-mark {
    font-family: "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    font-size: 24px;
    font-weight: 800;
    line-height: 1;
    color: #333333;
    letter-spacing: -0.01em;
  }
  .brand-tag {
    color: #93c5fd; /* Soft blue */
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.08em;
  }
  .brand-subtitle {
    color: #d1d5db; /* Light gray */
    font-size: 16px;
    font-weight: 400;
    line-height: 1.3;
  }
  .icon-links {
    display: flex;
    align-items: center;
    gap: 16px;
    flex-shrink: 0;
    padding-top: 4px;
  }
  .icon-link {
    width: 28px;
    height: 28px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    color: #9ca3af;
    transition: color 0.15s ease;
  }
  .icon-link:hover {
    color: #4b5563;
  }
  /* Target the SVGs inside the link */
  :global(.icon-link svg) {
    width: 22px;
    height: 22px;
    stroke-width: 2px;
  }
  @media (max-width: 768px) {
    .top-bar {
      flex-direction: column;
      align-items: flex-start;
    }
    .icon-links {
      padding-top: 12px;
    }
  }
</style>

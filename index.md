<style>
  .hero {
    text-align: center;
    padding: 3rem 1rem 2rem;
    border-bottom: 1px solid #e5e7eb;
    margin-bottom: 2.5rem;
  }
  .hero h1 {
    font-size: 2.4rem;
    margin-bottom: 0.5rem;
    background: linear-gradient(90deg, #4f46e5, #06b6d4);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  .hero .tagline {
    font-size: 1.1rem;
    color: #6b7280;
    max-width: 600px;
    margin: 0 auto;
  }
  .topics {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1rem;
    margin: 2.5rem 0;
  }
  .topic-card {
    border: 1px solid #e5e7eb;
    border-radius: 12px;
    padding: 1.25rem;
    transition: transform 0.15s ease, box-shadow 0.15s ease;
  }
  .topic-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 24px rgba(0,0,0,0.07);
  }
  .topic-card h3 { margin: 0 0 0.4rem; font-size: 1.05rem; }
  .topic-card p { margin: 0; color: #6b7280; font-size: 0.92rem; }
  .section-heading {
    font-size: 1.5rem;
    margin: 2.5rem 0 1rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  .section-heading::after {
    content: "";
    flex: 1;
    height: 1px;
    background: #e5e7eb;
  }
  .post-list { list-style: none; padding: 0; }
  .post-list li {
    display: flex;
    align-items: baseline;
    gap: 0.75rem;
    padding: 0.75rem 0;
    border-bottom: 1px solid #f3f4f6;
  }
  .post-list .post-date {
    color: #9ca3af;
    font-size: 0.85rem;
    font-variant-numeric: tabular-nums;
    white-space: nowrap;
    min-width: 110px;
  }
  .post-list a {
    text-decoration: none;
    color: #1f2937;
    font-weight: 500;
  }
  .post-list a:hover { color: #4f46e5; }
  .empty-note { color: #9ca3af; font-style: italic; }
</style>
 
<div class="hero">
  <h1>Vidya Sagar's Notebook</h1>
  <p class="tagline">
    MS Computer Science @ George Mason University — exploring AI, LLMs,
    autonomous agents, and the frontier of where software is headed.
  </p>
</div>
 
<p>
  Welcome to my public notebook. This is where I think out loud about the
  technology shaping our future — distilled into notes, takeaways, and the
  occasional rabbit hole.
</p>
 
<div class="topics">
  <div class="topic-card">
    <h3>📰 Articles</h3>
    <p>Interesting reads I come across, with notes on why they matter.</p>
  </div>
  <div class="topic-card">
    <h3>📚 Books</h3>
    <p>Notes and takeaways from what I'm currently reading.</p>
  </div>
  <div class="topic-card">
    <h3>🤖 AI &amp; Tools</h3>
    <p>New models, agent frameworks, and developer tools worth knowing.</p>
  </div>
  <div class="topic-card">
    <h3>⚡ Tech Updates</h3>
    <p>What's actively shaping the future of software and AI.</p>
  </div>
</div>
 
<h2 class="section-heading">Recent Posts</h2>
 
<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% else %}
    <li class="empty-note">No posts yet — first one coming soon. Stay tuned!</li>
  {% endfor %}
</ul>

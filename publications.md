---
layout: page
title: Publications
---
<main>
<head>
<style>
/* 1. Enable smooth scrolling */
html {
  scroll-behavior: smooth;
}
/* 2. Make nav sticky */
main > nav {
  position: sticky;
  top: 5rem;
  align-self: start;
}
/* 3. ScrollSpy active styles (see JS tab for activation) */
.section-nav li.active > a {
  color: #333;
  font-weight: 500;
}
/* Sidebar Navigation */
.section-nav {
  padding-left: 0;
  border-left: 1px solid #efefef;
}
.section-nav a {
  text-decoration: none;
  display: block;
  padding: .125rem 0;
  color: #ccc;
  transition: all 50ms ease-in-out; /* 💡 This small transition makes setting of the active state smooth */
}
.section-nav a:hover,
.section-nav a:focus {
  color: #666;
}
/** Poor man's reset **/
* {
  box-sizing: border-box;
  }
html, body {
  background: #fff;
}
body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Cantarell", "Fira Sans", "Droid Sans", "Helvetica Neue", sans-serif;
}
ul, ol {
  list-style: none;
  margin: 0;
  padding: 0;
}
li {
  margin-left: 1rem;
}
h1 {
  font-weight: 300;
}
/** page layout **/
main {
  display: grid;
  grid-template-columns: 800px 300px;
  max-width: 1500px;
  width: 90%;
  margin: 0 auto;
}
/** enlarge the sections for this demo, so that we have a long scrollable page **/
section {
  padding-bottom: 10rem;
}
</style>
</head>
  <div>
    <h1>Publications</h1>
    
    <section id="densephysnet">
      <h2>DensePhysNet: Learning Dense Physical Object Representations via Multi-step Dynamic Interactions</h2>
      <p>Zhenjia Xu, Jiajun Wu, Andy Zeng, Joshua Tenenbaum, Shuran Song</p>
      <p><em>Robotics: Science and Systems 2019 (RSS 2019)</em></p>
      <p>
        <a href="http://www.zhenjiaxu.com/DensePhysNet/">Webpage</a> |
        <a href="https://arxiv.org/pdf/1906.03853.pdf">Paper</a> |
        <a href="https://github.com/zhenjia-xu/DensePhysNet-Simulation">Code</a>
      </p>
      <img src="assets/densephysnet.mp4" alt="DensePhysNet">
    </section>

    <section id="tossingbot">
      <h2>TossingBot: Learning to Throw Arbitrary Objects with Residual Physics</h2>
      <p>Andy Zeng, Shuran Song, Stefan Welker, Johnny Lee, Alberto Rodriguez, Thomas Funkhouser</p>
      <p><em>Robotics: Science and Systems 2019 (RSS 2019), IEEE Transactions on Robotics (T-RO 2020)</em></p>
      <p><strong>Best System Paper Award, Best Student Paper Finalist</strong></p>
      <p>
        <a href="https://tossingbot.cs.princeton.edu/">Webpage</a> |
        <a href="https://arxiv.org/abs/1903.11239">Paper</a>
      </p>
      <img src="assets/tossing_small.jpg" alt="TossingBot">
    </section>
  </div>
  
  <nav class="section-nav">
    <ol>
      <li><a href="#densephysnet">DensePhysNet</a></li>
      <li><a href="#tossingbot">TossingBot</a></li>
    </ol>
  </nav>
</main>
<script>
window.addEventListener('DOMContentLoaded', () => {
	const observer = new IntersectionObserver(entries => {
		entries.forEach(entry => {
			const id = entry.target.getAttribute('id');
			if (entry.intersectionRatio > 0) {
				document.querySelector(`nav li a[href="#${id}"]`).parentElement.classList.add('active');
			} else {
				document.querySelector(`nav li a[href="#${id}"]`).parentElement.classList.remove('active');
			}
		});
	});
	// Track all sections that have an `id` applied
	document.querySelectorAll('section[id]').forEach((section) => {
		observer.observe(section);
	});
});
</script>

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



 <section id="Journal">
  &nbsp;
    <h2>Journal Publications</h2>
    <div markdown="1">
{% include render_pub_list.liquid variable="category" value="journal" check="==" %}
</div>
</section>


	 <section id="Conferences">
&nbsp;
    <h2>Full-length Conference Publications</h2>
    <div markdown="1">
{% include render_pub_list.liquid variable="category" value="conference" check="==" %}
</div>
</section>







 <section id="workshop">
&nbsp;
    <h2>Workshop and Short Conference Publications</h2>
    <div markdown="1">
{% include render_pub_list.liquid variable="category" value="workshop" check="==" %}
</div>
</section>

  </div>
  <nav class="section-nav">
    <ol>
      <li><a href="#Journal">Journal</a></li>
      <li><a href="#Conferences">Conference</a></li>
      <li><a href="#workshop">Workshop and Short Conference</a></li>
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

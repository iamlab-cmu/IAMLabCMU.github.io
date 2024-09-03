layout: page
title: Publications
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
<main>
  <div>
Research
DensePhysNet: Learning Dense Physical Object Representations via Multi-step Dynamic Interactions
Zhenjia Xu, Jiajun Wu, Andy Zeng, Joshua Tenenbaum, Shuran Song
Robotics: Science and Systems 2019 (RSS 2019)
Webpage | Paper | Code
Show Image
TossingBot: Learning to Throw Arbitrary Objects with Residual Physics
Andy Zeng, Shuran Song, Stefan Welker, Johnny Lee, Alberto Rodriguez, Thomas Funkhouser
Robotics: Science and Systems 2019 (RSS 2019), IEEE Transactions on Robotics (T-RO 2020)
Best System Paper Award, Best Student Paper Finalist
Webpage | Paper
Show Image
  </div>
</main>

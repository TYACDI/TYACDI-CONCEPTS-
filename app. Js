// Typewriter for hero tagline
function typeWriter(el, text, speed=45){
  el.textContent=""; let i=0;
  (function tick(){ el.textContent = text.slice(0, i++); if(i<=text.length){ setTimeout(tick, speed);} })();
}
document.addEventListener("DOMContentLoaded", ()=>{
  const t = document.querySelector(".type");
  if(t) typeWriter(t, "Learn. Create. Innovate.");
  // Reveal on scroll
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting) e.target.classList.add("show"); });
  },{threshold:.12});
  document.querySelectorAll(".fade-in").forEach(el=>io.observe(el));
  // Simple active link highlighter
  const here = location.pathname.split("/").pop();
  document.querySelectorAll("nav a").forEach(a=>{
    const file = a.getAttribute("href"); if (file===here || (here==="" && file==="index.html")) a.classList.add("active");
  });
});

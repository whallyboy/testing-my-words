const btn = document.querySelector('.nav-toggle');  
const nav = document.getElementById('main-nav');  
  
btn.addEventListener('click', () => {  
  const isOpen = nav.classList.toggle('is-open');  
  btn.setAttribute('aria-expanded', isOpen);  
  btn.textContent = isOpen ? '✕' : '☰';  
});  

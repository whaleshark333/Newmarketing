// Preloader
window.addEventListener('load', () => {
  const preloader = document.getElementById('preloader');
  preloader.style.opacity = '0';
  setTimeout(() => preloader.style.display = 'none', 500);
});

// AOS Animations
AOS.init({
  duration: 1000,
  once: true,
});

// Theme Switcher (Dark/Light)
const themeToggle = document.getElementById('theme-toggle');
themeToggle.addEventListener('click', () => {
  document.body.classList.toggle('dark');
  themeToggle.textContent = document.body.classList.contains('dark') ? '☀️' : '🌙';
});

// EmailJS Contact Form
(function(){
  emailjs.init("YOUR_EMAILJS_USER_ID"); // Replace with your EmailJS user ID
})();

document.getElementById('contactForm').addEventListener('submit', function(e) {
  e.preventDefault();

  emailjs.sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', this)
    .then(() => {
      alert('Thank you! Your message has been sent.');
      this.reset();
    }, (error) => {
      alert('Oops! Something went wrong. Please try again.');
      console.log(error);
    });
});

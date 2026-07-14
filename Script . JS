/* ==========================================
   GREBY MARKETPLACE V2.0
   SCRIPT.JS - PART 1
   Core Features
========================================== */

// ==========================
// Sticky Header
// ==========================

const header = document.querySelector("header");

window.addEventListener("scroll", () => {

    if (window.scrollY > 60) {

        header.style.background = "rgba(5,15,40,.95)";
        header.style.boxShadow = "0 12px 30px rgba(0,207,255,.25)";

    } else {

        header.style.background = "rgba(6,18,40,.75)";
        header.style.boxShadow = "none";

    }

});

// ==========================
// Smooth Scroll
// ==========================

document.querySelectorAll('a[href^="#"]').forEach(link => {

    link.addEventListener("click", function(e) {

        e.preventDefault();

        const target = document.querySelector(this.getAttribute("href"));

        if(target){

            target.scrollIntoView({

                behavior:"smooth"

            });

        }

    });

});

// ==========================
// Search Bar
// ==========================

const searchInput = document.querySelector(".search-box input");

if(searchInput){

searchInput.addEventListener("keyup",function(){

const value = this.value.toLowerCase();

console.log("Searching:",value);

});

}

// ==========================
// Scroll Reveal Animation
// ==========================

const observer = new IntersectionObserver(entries=>{

entries.forEach(entry=>{

if(entry.isIntersecting){

entry.target.classList.add("show");

}

});

},{
threshold:0.15
});

document.querySelectorAll("section").forEach(section=>{

section.classList.add("hidden");

observer.observe(section);

});

// ==========================
// Hero Image Animation
// ==========================

const heroImage = document.querySelector(".hero-right img");

if(heroImage){

setInterval(()=>{

heroImage.style.transform="translateY(-10px)";

setTimeout(()=>{

heroImage.style.transform="translateY(0px)";

},1200);

},3500);

}

// ==========================
// Button Hover Effect
// ==========================

document.querySelectorAll(".primary-btn,.secondary-btn,.buy-btn,.video-btn").forEach(btn=>{

btn.addEventListener("mouseenter",()=>{

btn.style.transform="translateY(-4px)";

});

btn.addEventListener("mouseleave",()=>{

btn.style.transform="translateY(0px)";

});

});

// ==========================
// Logo Click
// ==========================

const logo=document.querySelector(".logo");

if(logo){

logo.addEventListener("click",()=>{

window.scrollTo({

top:0,

behavior:"smooth"

});

});

}

console.log("Greby Marketplace Loaded Successfully");/* ==========================================
   GREBY MARKETPLACE V2.0
   SCRIPT.JS - PART 2
   Product Interactions
========================================== */

// ==========================
// Buy Button
// ==========================

document.querySelectorAll(".buy-btn").forEach(button=>{

button.addEventListener("click",(e)=>{

e.preventDefault();

button.innerHTML="⏳ Redirecting...";

button.disabled=true;

setTimeout(()=>{

alert("Affiliate link integration will be connected in the next phase.");

button.innerHTML="🛒 Buy Now";

button.disabled=false;

},1800);

});

});

// ==========================
// Save Product
// ==========================

document.querySelectorAll(".save-btn").forEach(button=>{

button.addEventListener("click",()=>{

if(button.classList.contains("saved")){

button.classList.remove("saved");

button.innerHTML="❤️ Save Product";

}else{

button.classList.add("saved");

button.innerHTML="💙 Saved";

showNotification("Product added to your wishlist.");

}

});

});

// ==========================
// Review Video
// ==========================

document.querySelectorAll(".video-btn").forEach(button=>{

button.addEventListener("click",(e)=>{

e.preventDefault();

showNotification("Video reviews will open here in the next version.");

});

});

// ==========================
// Product Card Hover
// ==========================

document.querySelectorAll(".product-card").forEach(card=>{

card.addEventListener("mouseenter",()=>{

card.style.transform="translateY(-12px) scale(1.02)";

});

card.addEventListener("mouseleave",()=>{

card.style.transform="translateY(0px) scale(1)";

});

});

// ==========================
// Category Click
// ==========================

document.querySelectorAll(".category-card").forEach(card=>{

card.addEventListener("click",()=>{

const category=card.innerText.trim();

showNotification(category+" selected.");

});

});

// ==========================
// Notification Function
// ==========================

function showNotification(message){

const notify=document.createElement("div");

notify.className="greby-notification";

notify.innerText=message;

document.body.appendChild(notify);

notify.style.position="fixed";
notify.style.top="25px";
notify.style.right="25px";
notify.style.background="#00CFFF";
notify.style.color="#05111d";
notify.style.padding="15px 25px";
notify.style.borderRadius="15px";
notify.style.fontWeight="600";
notify.style.zIndex="9999";
notify.style.boxShadow="0 15px 35px rgba(0,207,255,.35)";

setTimeout(()=>{

notify.style.opacity="0";
notify.style.transition=".4s";

},2200);

setTimeout(()=>{

notify.remove();

},2700);

}

// ==========================
// Product Image Animation
// ==========================

document.querySelectorAll(".product-card img").forEach(image=>{

image.addEventListener("mouseenter",()=>{

image.style.transform="scale(1.08)";

});

image.addEventListener("mouseleave",()=>{

image.style.transform="scale(1)";

});

});

console.log("Greby Product Features Loaded");/* ==========================================
   GREBY MARKETPLACE V2.0
   SCRIPT.JS - PART 3
   Premium Features & Final Polish
========================================== */

// ==========================
// Back To Top Button
// ==========================

const topButton = document.createElement("button");

topButton.innerHTML = "⬆";

topButton.className = "topButton";

document.body.appendChild(topButton);

window.addEventListener("scroll", () => {

    if (window.scrollY > 400) {

        topButton.style.display = "block";

    } else {

        topButton.style.display = "none";

    }

});

topButton.addEventListener("click", () => {

    window.scrollTo({

        top: 0,

        behavior: "smooth"

    });

});

// ==========================
// Animated Counters
// ==========================

const counters = document.querySelectorAll(".stat-box h2");

const counterObserver = new IntersectionObserver((entries) => {

entries.forEach(entry => {

if (entry.isIntersecting) {

const counter = entry.target;

const target = parseInt(counter.innerText);

let count = 0;

const speed = Math.max(10, Math.floor(target / 100));

const timer = setInterval(() => {

count += speed;

if (count >= target) {

counter.innerText = target + "+";

clearInterval(timer);

} else {

counter.innerText = count + "+";

}

}, 20);

}

});

});

counters.forEach(counter => {

counterObserver.observe(counter);

});

// ==========================
// Newsletter
// ==========================

const subscribeButton = document.querySelector(".newsletter-box button");

if (subscribeButton) {

subscribeButton.addEventListener("click", () => {

const email = document.querySelector(".newsletter-box input");

if (email.value.trim() === "") {

showNotification("Please enter your email.");

return;

}

showNotification("Thanks for subscribing!");

email.value = "";

});

}

// ==========================
// Contact Cards
// ==========================

document.querySelectorAll(".contact-card").forEach(card => {

card.addEventListener("mouseenter", () => {

card.style.transform = "translateY(-10px)";

});

card.addEventListener("mouseleave", () => {

card.style.transform = "translateY(0px)";

});

});

// ==========================
// Keyboard Shortcut
// Press "/" to focus search
// ==========================

document.addEventListener("keydown", (event) => {

if (event.key === "/") {

event.preventDefault();

if (searchInput) {

searchInput.focus();

}

}

});

// ==========================
// Welcome Message
// ==========================

window.addEventListener("load", () => {

setTimeout(() => {

showNotification("Welcome to Greby — Grab the Best, Skip the Rest.");

}, 1000);

});

// ==========================
// Console Banner
// ==========================

console.log("%cGREBY MARKETPLACE","color:#00CFFF;font-size:28px;font-weight:bold;");

console.log("Grab the Best, Skip the Rest.");

console.log("Greby Marketplace v2.0 Loaded Successfully.");

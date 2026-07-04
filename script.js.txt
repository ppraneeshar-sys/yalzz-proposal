const msg1=`Nee dhan enoda lucky charm pah! 🍀❤️

Nee vandhadhuku aprm dhan naan Sanchana va marandhu unkuda sandhosama irundhen.

Aana...

Namma sanda potadhuku aprm en andha akka kitta pesunen nu enake therla...

Adhukku manasaara sorry Yalzz. 😔❤️`;

const msg2=`Naan panadhu thappu dhan...

Adha naan othukuren. 😔

Inime andha thappa oru naalum repeat panna maten.

Un trust ah naan kandippa kaapathuven. 💯

Idhuku aprm unakitta poi solli unnai hurt panna maten.

Indha oru vaati enna nambu...

Enoda motha love-um unakku dhaan. 🤌🏻💕`;

const msg3=`Unna lose panna enakku viruppam illa...🥺

Thirumba enakku innoru chance kudu pahh.

Unakaga dhaan naan kathukite iruken. 🤌🏻🫠❤️`;

function typeWriter(id,text){
let i=0;
document.getElementById(id).innerHTML="";
let speed=35;

function typing(){
if(i<text.length){
document.getElementById(id).innerHTML+=text.charAt(i);
i++;
setTimeout(typing,speed);
}
}
typing();
}

typeWriter("text1",msg1);

function nextPage(page){

document.querySelectorAll(".page").forEach(p=>p.classList.remove("active"));

document.getElementById("page"+page).classList.add("active");

if(page==2){
typeWriter("text2",msg2);
}

if(page==3){
typeWriter("text3",msg3);
}
}

function yes(){
alert("Thank You Yalzz ❤️🥹\nYou made me the happiest person. 💖");
}

function moveNo(){
let btn=document.getElementById("no");

btn.style.position="absolute";
btn.style.left=Math.random()*70+"%";
btn.style.top=Math.random()*70+"%";
}

const hearts=document.querySelector(".hearts");

setInterval(()=>{
let heart=document.createElement("span");
heart.innerHTML="❤️";
heart.style.left=Math.random()*100+"vw";
heart.style.fontSize=(20+Math.random()*20)+"px";
heart.style.animationDuration=(4+Math.random()*4)+"s";
hearts.appendChild(heart);

setTimeout(()=>{
heart.remove();
},8000);

},300);

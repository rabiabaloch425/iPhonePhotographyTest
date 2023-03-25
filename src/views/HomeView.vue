
<template>
  <main>
    <div class="container">
      <div class="mt-[62px] sm:ml-[25px] md:ml-[156px] mb-[-18px]">
      <img src="../../public/images/ips-logo.png" alt="ips-logo" class="w-[180px] h-[45px]">
    </div>
    <div class="md:flex sm:block">
      <div class="sm:w-[100%] md:w-[40%] sm:ml-[25px] md:ml-[156px]  mt-[200px]">
        <h3
          class="w-[128px] h-[28px] bg-[#2B5341] rounded-[32px] gap-[8px]  flex justify-center  text-[#EEECEC]  text-[12px] items-center cursor-pointer">
          NEW COURSE
        </h3>
        <h1
          class="primary-font-regular !font-normal mt-[24px] sm:!text-[40px] md:!text-[63px] sm:w-[286px] md:w-[449px] h-[126px] leading-[63px] text-[#EEECEC]">
          iPhone Photo Academy
        </h1>
        <h4
          class="text-[#EEECEC] primary-font-regular sm:w-[298px] md:w-[320px] h-[60px] leading-[30px] mt-[32px] !font-normal text-[22px]">
          Sign up now to get notified when this course is available!
        </h4>
        <div class="relative w-[423px]">
          <input type="email" id="myText" value="" placeholder="Enter your Email Address" class="outline-none text-[16px] box-border p-[16px] sm:w-[290px] md:w-[423px] h-[62px] bg-[#171715] border-[1px] text-[#EEECEC] sm:mt-[40px] md:mt-[18px] border-[#3A3A3A] rounded-[6px]">
          <img src="../../public/images/icon.png" class="absolute sm:right-[9rem] md:right-4 sm:top-[3.5em] md:top-[2.2em]" alt="">
        </div>
        <p id="email-validation" class="text-red-800"></p>
        <button class="text-[#EEECEC] box-border text-[16px] py-[16px] px-[24px] sm:w-[290px] md:w-[201px] mt-[18px] rounded-[6px] button-bg"  @click="notifyMe()">Please Notify Me</button>
      </div>
      <div class="sm:w-[140%] md:w-[60%] bg-[url('../../public/images/ambient-background.png')] bg-no-repeat">
      <Carosel/>
      </div>
    </div>
    </div>
</main></template>
<script setup>
import Carosel from '../components/Carosel.vue';
// access value of email input
const notifyMe = ()=> {
  let emailValue = document.getElementById("myText").value;
  var filter = /^([a-zA-Z0-9_\.\-])+\@(([a-zA-Z0-9\-])+\.)+([a-zA-Z0-9]{2,4})+$/;
   if(!filter.test(emailValue)){
    document.getElementById('email-validation').innerHTML = "Please enter a valid email";
   }
   else {
    window.location.href = '/thank-you';
   }
}
</script>

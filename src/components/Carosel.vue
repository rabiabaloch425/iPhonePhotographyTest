

<template>
 <div class="pr-0 py-[2em] sm:pl-[2em] sm:pr-[2em] md:pr-0 md:pl-[10em] relative">
    <div id="dvImage" class="z-40 h-[692px] w-[335px] " >
        
        </div>
        <div class="progress top-3 left-5">
            <div id="length"></div>
            <div id="progress__animation"></div>
            <div class="slider__count">
                <div class="count"></div>
                <div class="count"></div>
                <div class="count"></div>
                <div class="count"></div>
            </div>
        </div>
 </div>
</template>
<script setup >
  var images = ["iPhone-mockup1.png", "iPhone-mockup2.png", "iPhone-mockup3.png", "iPhone-mockup4.png", ];
        $(function () {
            var i = 0;
            $("#dvImage").css("background-image", "url(../../public/images/" + images[i] + ")");
            setInterval(function () {
                i++;
                if (i == images.length) {
                    i = 0;
                }
                $("#dvImage").show("slow", function () {
                    $(this).css("background-image", "url(../../public/images/" + images[i] + ")");
                    $(this).show("slow");
                });
            }, 8000);
        });
</script>
<style lang="scss" scoped>

</style>
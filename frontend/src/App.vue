<template>
    <div id="app">
        <div id="header-panel">
            <div id="header">
                <img src="wedding-title.png">
            </div>
        </div>
        <div id="info-panel">
            <div class="section-divider"></div>
            <div id="info">

                <div id="main-pic">
                    <slider animation="fade" style="height: 100%;" interval="10000">
                        <div id="main-pic-bck">
                            <slider-item><img class="main-pic-img" src="gallery/img000.jpg"></slider-item>
                            <slider-item><img class="main-pic-img" src="gallery/img001.jpg"></slider-item>
                            <slider-item><img class="main-pic-img" src="gallery/img002.jpg"></slider-item>
                            <slider-item><img class="main-pic-img" src="gallery/img003.jpg"></slider-item>
                            <slider-item><img class="main-pic-img" src="gallery/img004.jpg"></slider-item>
                            <slider-item><img class="main-pic-img" src="gallery/img005.jpg"></slider-item>
                            <slider-item><img class="main-pic-img" src="gallery/img006.jpg"></slider-item>
                        </div>
                    </slider>
                </div>

                <div class="section-divider"></div>

                <div id="general-info" class="section">
                    <div id="general-info-title" class="section-title">General Information</div>
                    <div id="general-info-img"><img src="caballero.jpg"></div>
                    <div id="general-info-content"><br>
                        Day of the Event: 01/19/2019<br>
                        El Caballero Country Club<br>
                        18300 Tarzana Dr. Tarzana, CA 91356<br><br>
                        <span style="font-size: 24px;font-weight: bold;"><a href="https://www.amazon.com/wedding/natalia-minassian-carlos-galavis-tarzana-january-2019/registry/3MT3413YVDB80"  target="_blank">
                            Visit Our Registry
                        </a></span>
                    </div>
                </div>

                <div class="section-divider"></div>

                <div id="program" class="section">
                    <div id="program-title" class="section-title">Program</div>
                    <div id="program-content" style="text-align: left;">
                        <table>
                            <tr><td style="width: 75px;">&nbsp;05:00PM</td><td>Ceremony</td></tr>
                            <tr><td>&nbsp;06:00PM</td><td>Cocktail Hour / Pictures</td></tr>
                            <tr><td>&nbsp;07:00PM</td><td>First Dance</td></tr>
                            <tr><td>&nbsp;07:05PM</td><td>Father Daughter Dance</td></tr>
                            <tr><td>&nbsp;07:30PM</td><td>Toast</td></tr>
                            <tr><td>&nbsp;07:45PM</td><td>Dinner</td></tr>
                            <tr><td>&nbsp;09:00PM</td><td>Sunday Bar</td></tr>
                            <tr><td>&nbsp;09:30PM</td><td>Open Dance Floor</td></tr>
                            <tr><td>&nbsp;11:00PM</td><td>End</td></tr>

                        </table>
                    </div>
                    <div id="program-img"><img src="reception.jpg"></div>
                </div>

                <div class="section-divider"></div>

                <div id="menu" class="section">
                    <div id="menu-title" class="section-title">Dinner Menu</div>
                    <div id="menu-img"><img src="menu.jpg"></div>
                    <div id="menu-content"><br>
                        <div class="menu-section">Salad</div>
                        Beet and Goat Salad<br>
                        Djon Vinaigrette<br><br>

                        <div class="menu-section">Entree</div>
                        Miso and Soy Chilean Sea Bass<br>
                        Petite Filet with Red Wine Reduction<br>
                        Mushroom Risotto<br>
                        Seasonal Roasted Vegetables<br>
                    </div>
                </div>
            </div><br>

            <span style="font-size: 12px; color: brown;">
                <p>
                    Copyright ©2018 All Rights Reserved<br>
                    Images provided by Lin and Jirsa Premiere Wedding Photography
                </p>
            </span>
            <br><br>
        </div>
    </div>
</template>

<script>
    import { Slider, SliderItem } from 'vue-easy-slider';

    export default {
        name: 'app',
        components: {
            Slider,
            SliderItem
        },

        data() {
            return {
                list: []
            }
        },
    }
</script>

<style>
    a {
        color: brown;
    }

    #app {
        display: grid;
        grid-template-rows: 180px 1fr;
        grid-template-areas:
            "header header header"
            "info info info";

        width: 100%;
        height: 100%;
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
    }

    /* HEADER */

    #header-panel {
        grid-area: header;
        width: 100%;
        height: 100%;
        background-color: bisque;
        border-bottom: solid 2px burlywood;
    }

    #header {
        height: 100%;
        background-image: url("assets/bck-canvas.jpg");
    }

    #header > img {
        height: 100%;
        opacity: 0.7;
        object-fit: cover;
    }


    /* INFO */

    #info-panel {
        grid-area: info;
        width: 100%;
        height: auto;
        overflow: auto;
    }

    #info {
        max-width: 900px;
        margin-left: auto;
        margin-right: auto;
    }

    #main-pic {
        width: 100%;
        height: 400px;
        background-color: white;
        border: thin solid burlywood;
        //box-shadow: 2px 2px 6px saddlebrown;
    }

    #main-pic-bck {
        width: 100%;
        height: 100%;
        background-color: antiquewhite;
    }

    .main-pic-img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }


    /* Info Sections */

    .section-divider {
        height: 4px;
    }

    .section {
        width: 100%;
        text-align: center;
        font-size: 14px;
        color: sienna;
    }

    .section-title {
        width: 100%;
        text-align: center;
        background-color: sienna;
        color: antiquewhite;
        font-weight: bold;
        font-size: 18px;
    }


    /*  General Info */

    #general-info {
        width: 100%;
        display: grid;
        border: thin solid sienna;

        grid-template-columns: 1fr 300px;
        grid-template-areas:
            "general-info-title general-info-title"
            "general-info-img general-info-content"
        ;
        grid-template-rows: 26px 150px
    }

    #general-info-title {
        grid-area: general-info-title;
    }

    #general-info-img {
        grid-area: general-info-img;
        margin: 1px;
        opacity: 0.8;
    }

    #general-info-img > img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        opacity: 0.9;
    }

    #general-info-content {
        grid-area: general-info-content;
    }


    /* Program */

    #program {
        width: 100%;
        display: grid;
        border: thin solid sienna;

        grid-template-columns: 300px 1fr;
        grid-template-areas:
            "program-title program-title"
            "program-content program-img"
        ;
        grid-template-rows: 26px 220px
    }

    #program-title {
        grid-area: program-title;
    }

    #program-img {
        grid-area: program-img;
        margin: 1px;
    }

    #program-img > img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        opacity: 0.8;
    }

    #program-content {
        grid-area: program-content;
        padding: 6px;
    }


    /* Menu */

    #menu {
        width: 100%;
        display: grid;
        border: thin solid sienna;

        grid-template-columns: 1fr 350px;
        grid-template-areas:
            "program-title program-title"
            "program-img program-content"
        ;
        grid-template-rows: 26px 220px
    }

    #menu-title {
        grid-area: program-title;
    }

    #menu-img {
        grid-area: program-img;
        margin: 1px;
    }

    #menu-img > img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        opacity: 0.8;
    }

    #menu-content {
        grid-area: program-content;
        text-align: center;
    }

    .menu-section {
        width: 100%;
        font-size: 16px;
        font-weight: bold;
    }

</style>

<template>
    <div id="app">
        <div id="header-panel">
            <div id="header">
                <img src="title2.png">
            </div>
        </div>

        <div id="space-panel"></div>

        <div id="info-panel">
            <div id="info">
                <div id="main-pic">
                    <slider animation="fade" style="height: 100%;" :interval="10000">
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
                    <div id="general-info-img">
                        <img src="caballero.jpg">
                        <iframe id="info-map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3301.461727746905!2d-118.53503934813945!3d34.160110819387704!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80c299aa631697a3%3A0x190c32e28cad0295!2sEl+Caballero+Country+Club!5e0!3m2!1sen!2sus!4v1542837136116" frameborder="0" allowfullscreen></iframe>
                    </div>
                    <div id="general-info-content"><br><br>
                        <b>Wellcome to Our Wedding Site</b><br>
                        Come celebrate with us<br>
                        The ceremony wil be held on<br>
                        <b>January 19th 2019 at 5:00PM</b><br>
                        The reception will follow<br><br>
                        Location:<br><br>
                        <b>El Caballero Country Club</b><br>
                        18300 Tarzana Dr. Tarzana, CA 91356<br><br>
                        <span style="font-size: 24px;font-weight: bold;"><a href="https://www.amazon.com/wedding/natalia-minassian-carlos-galavis-tarzana-january-2019/registry/3MT3413YVDB80"  target="_blank">
                            Visit Our Registry
                        </a></span><br><br>
                        Our families and closest<br>
                        friends will gather to dance, dine and<br>
                        have a great time. Hope you can make it!!

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
                    ***<br><br>
                    Copyright ©2018 All Rights Reserved<br>
                    Images provided by Lin and Jirsa Premiere Wedding Photography
                </p>
            </span>
            <br>
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

        grid-template-columns: 1fr;
        grid-template-rows: 90px 8px 1fr;
        grid-template-areas:
            "header"
            "space"
            "info";

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
        opacity: 0.8;
        object-fit: cover;
    }

    #space-panel {
        grid-area: space;
    }


    /* INFO */

    #info-panel {
        grid-area: info;
        width: 100%;
        height: auto;
        overflow-y: auto;
        overflow-x: hidden;
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
        grid-template-rows: auto 400px
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
        height: 150px;
        object-fit: cover;
        opacity: 0.9;
    }

    #info-map {
        width: 100%;
        height: 244px;
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
        grid-template-rows: auto 220px
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
        grid-template-rows: auto 220px
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

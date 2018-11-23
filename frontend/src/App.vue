<template>
    <div id="app">
        <div id="header-panel">
            <div id="header">
                <img src="title3.png">
            </div>
        </div>
        <div id="info-panel">
            <div id="info-sections">
                <div style="height: 16px"></div>
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

                    <div id="general-info" class="section">
                        <div id="general-info-img">
                            <img src="caballero.jpg">
                            <iframe id="info-map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3301.461727746905!2d-118.53503934813945!3d34.160110819387704!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80c299aa631697a3%3A0x190c32e28cad0295!2sEl+Caballero+Country+Club!5e0!3m2!1sen!2sus!4v1542837136116" frameborder="0" allowfullscreen></iframe>
                        </div>
                        <div id="general-info-content">
                            <b>Wellcome to Our Wedding Site</b><br>
                            Come celebrate with us<br>
                            The ceremony wil be held on<br>
                            <b>January 19th 2019 at 5:00PM</b><br>
                            The reception will follow<br><br>
                            Location:<br><br>
                            <b>El Caballero Country Club</b><br>
                            18300 Tarzana Dr. Tarzana, CA 91356<br><br>
                            Our families and closest<br>
                            friends will gather to dance, dine and<br>
                            have a great time. Hope you can make it!!<br><br>

                            Visit our registry below <br><br>
                            <span style="font-size: 28px">👍</span><br><br>

                            <div style="border: 2px solid sienna; margin-left: 24px; margin-right: 24px;">
                                <span style="font-size: 42px; font-weight: bold;"><a href="https://www.amazon.com/wedding/natalia-minassian-carlos-galavis-tarzana-january-2019/registry/3MT3413YVDB80"  target="_blank">
                                    Registry
                                </a></span>
                            </div>
                        </div>
                    </div>

                    <div id="program" class="section">
                        <div id="program-content" style="text-align: left;">
                            &nbsp;04:45PM&nbsp;&nbsp;&nbsp;Arrival<br>
                            &nbsp;05:00PM&nbsp;&nbsp;&nbsp;Ceremony<br>
                            &nbsp;06:00PM&nbsp;&nbsp;&nbsp;Cocktail Hour<br>
                            &nbsp;07:00PM&nbsp;&nbsp;&nbsp;First Dance<br>
                            &nbsp;07:05PM&nbsp;&nbsp;&nbsp;Father and Daughter Dance<br>
                            &nbsp;07:30PM&nbsp;&nbsp;&nbsp;Champagne Toast<br>
                            &nbsp;07:45PM&nbsp;&nbsp;&nbsp;Dinner<br>
                            &nbsp;09:00PM&nbsp;&nbsp;&nbsp;Sunday Bar<br>
                            &nbsp;09:30PM&nbsp;&nbsp;&nbsp;Open Dance Floor<br>
                            &nbsp;11:00PM&nbsp;&nbsp;&nbsp;Thee End<br>
                        </div>
                        <div id="program-img" class="section-img"><div class="section-title">Program</div></div>
                    </div>

                    <div id="menu" class="section">
                        <div id="menu-img" class="section-img"><div class="section-title">Menu</div></div>
                        <div id="menu-content">
                            <div class="menu-section">Appetizers</div>
                            Cheese and bread bar will be available<br>
                            during the cocktail hour<br><br>

                            <div class="menu-section">Salad</div>
                            Roasted Beets<br>
                            Arugula, Pickled Red Onion<br>
                            Feta Cheese and Lemon Vinaigrette<br><br>

                            <div class="menu-section">Entree</div>
                            Chilean Sea Bass with Miso ButterSauce<br>
                            Filet Mignon with Port Reduction<br>
                            Mushroom Risotto<br>
                            Creamy Parmesan Polenta<br>
                            Seasonal Roasted Vegetables<br><br>

                            <div class="menu-section">Dessert</div>
                            Sundae Bar will be available<br>
                            after dinner<br>
                        </div>
                    </div>
                </div><br>

                <span style="font-size: 12px; color: brown;">
                    <p>
                        **<br><br>
                        Copyright ©2018 All Rights Reserved<br>
                        Images provided by Lin and Jirsa Premiere Wedding Photography
                    </p>
                </span>
                <br>
            </div>
        </div>
        <div id="footer-panel">
            <div id="footer"></div>
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
        text-decoration: none;
    }

    #app {
        display: grid;

        grid-template-columns: 1fr;
        grid-template-rows: 84px 4px 1fr 12px;
        grid-template-areas:
            "header"
            "."
            "info"
            "footer";

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
        border-bottom: solid 4px burlywood;
    }

    #footer-panel {
        grid-area: footer;
        width: 100%;
        height: 100%;
        background-color: bisque;
        background-image: url("assets/bck-canvas.jpg");
    }

    #footer {
        border-top: solid 4px burlywood;
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


    /* INFO */

    #info-panel {
        grid-area: info;
        display: grid;
        grid-template-columns: 16px 1fr 16px;
        grid-template-areas: ". sections .";


        width: 100%;
        height: auto;
        overflow-y: auto;
        overflow-x: hidden;
        -webkit-overflow-scrolling: touch;
    }

    #info-sections {
        grid-area: sections;
    }

    #info {
        max-width: 1000px;
        margin-left: auto;
        margin-right: auto;
        box-shadow: 1px 1px 25px #ca907a;;
    }

    #main-pic {
        width: 100%;
        height: 440px;
        background-color: white;
        border: thin solid sienna;
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

    .section {
        width: 100%;
        text-align: center;
        font-size: 14px;
        color: sienna;
    }

    .section-img {
        margin: 1px;
        background-size: cover;
        opacity: 0.8;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .section-title {
        color: white;
        font-size: 64px;
        font-weight: bold;
        -webkit-text-stroke-width: 2px;
        -webkit-text-stroke-color: maroon;
    }


    /*  General Info */

    #general-info {
        width: 100%;
        display: grid;
        border: thin solid sienna;
        border-top: 0;

        grid-template-columns: 1fr auto;
        grid-template-rows: auto;
        grid-template-areas:
            "general-info-img general-info-content"
        ;
    }

    #general-info-img {
        grid-area: general-info-img;
        height: 100%;
        margin: 1px;
        opacity: 0.8;
    }

    #general-info-img > img {
        width: 100%;
        height: 210px;
        object-fit: cover;
        opacity: 0.9;
    }

    #info-map {
        margin-top: -4px;
        width: 100%;
        height: calc(100% - 213px);
    }

    #general-info-content {
        grid-area: general-info-content;
        border-left: sienna thin solid;
        padding: 16px;
    }


    /* Program */

    #program {
        width: 100%;
        display: grid;
        border: thin solid sienna;

        grid-template-columns: auto 1fr;
        grid-template-areas:
            "program-title program-title"
            "program-content program-img"
        ;
        grid-template-rows: auto auto
    }

    #program-img {
        grid-area: program-img;
        background-image: url("assets/reception.jpg");
    }

    #program-content {
        grid-area: program-content;
        border-right: sienna thin solid;
        padding: 16px;
    }


    /* Menu */

    #menu {
        width: 100%;
        display: grid;
        border: thin solid sienna;

        grid-template-columns: 1fr auto;
        grid-template-areas:
            "program-title program-title"
            "program-img program-content"
        ;
        grid-template-rows: auto auto
    }

    #menu-img {
        grid-area: program-img;
        position: relative;
        background-image: url("assets/menu.jpg");
    }

    #menu-content {
        grid-area: program-content;
        text-align: center;
        border-left: sienna thin solid;
        padding: 16px;
    }

    .menu-section {
        width: 100%;
        font-size: 16px;
        font-weight: bold;
    }

</style>

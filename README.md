
<?xml version="1.0" encoding="UTF-8"?><!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "https://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd"><html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en" class=""><head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta id="descriptionTag" name="description" content="This is a description for the site.">
    <title>Ready To Respond</title>
    <link id="favicon" rel="icon" href="https://heyleia.com/images/favicon.png">
    <script src="https://code.jquery.com/jquery-latest.min.js"></script>
    <script type="text/javascript" src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
    <link href="https://use.fontawesome.com/releases/v5.0.8/css/all.css" rel="stylesheet">
    <script src="https://heyleia.com/js/analytics.js"></script>
    <link href="/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://heyleia.com/css/sweetalert.css" rel="stylesheet">
    <script src="https://heyleia.com/js/swal.min.js"></script>
    <link href="https://fonts.googleapis.com/css?family=Lato&amp;display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css?family=Poppins:800,800i&amp;display=swap" rel="stylesheet">

    <link href="https://fonts.googleapis.com/css?family=Noto+Sans+HK:900&amp;display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css?family=Lato&amp;display=swap" rel="stylesheet">
    
    <style id="fontFamilyStyle">
    
    h1, h2, h3, h4, h5, h6, h1 div, h2 div, h3 div, h4 div, h5 div, h6 div {
        font-family: 'Noto Sans HK', sans-serif;
    }
    p, span, label, a, button, strong, div, em {
        font-family: 'Lato', sans-serif;
    }
    </style>
    <link href="https://heyleia.com/css/leia.css" rel="stylesheet">
    <script>    
        $.browser = {}; $.support.opacity = true;
    </script>
    <script src="/lib/fancybox/jquery.fancybox-1.3.4.pack.js?v=1687529737"></script>
    <script src="/lib/fancybox/jquery.easing-1.3.pack.js"></script>
    <script src="/lib/fancybox/jquery.mousewheel-3.0.4.pack.js"></script>
    <script>
        var setCategoryClicksBackup = function() {
            $(".categoryButton").unbind();
            $('.categoryButton').click(function(){
                // let offsetHeight = document.getElementById('galleryRowContainer').offsetHeight.toString() + 'px';
                var value = $(this).attr('data-filter');
                // $('#galleryRowContainer').css({'min-height':offsetHeight}); 

                // setTimeout(function(){
                //     $('#galleryRowContainer').animate({'min-height':'0'});
                // },3000)

                if (value === 'all') {
                    $('.categoryFilter').show('1000');
                    $(this).addClass('categoryButtonSelected');
                    $('.categoryButton').not(this).removeClass('categoryButtonSelected');
                } else if ($(this).hasClass('categoryButtonSelected')) {
                    $('.categoryFilter').show('1000');
                    $(this).removeClass('categoryButtonSelected');
                    $('.allCategoryButton').addClass('categoryButtonSelected');
                }
                else {
                    $('.categoryFilter').not('.' + value).hide('3000');
                    $('.categoryFilter').filter('.' + value).show('3000');
                    $('.allCategoryButton').removeClass('categoryButtonSelected');
                    $('.categoryButton').not(this).removeClass('categoryButtonSelected');
                    $(this).toggleClass('categoryButtonSelected');
                }
            });

            $("a[rel=scrollGroup]").fancybox({
                'transitionIn'		: 'fade',
                'transitionOut'		: 'fade',
                'titlePosition' 	: 'over',
                'type'              : 'image',
                'titleFormat'		: function(title) {
                    return '<span id="fancybox-title-over">' + title + '';
                }
            });
        }
    </script>
    
</head>
<body style="">
<nav id="mainMenu" style="opacity: 1;">
    <button class="menuButton" id="trigger-overlay" style="opacity: 1;" altonclick="null" althref="null">
        <i class="openMenuIcon fa fa-bars" aria-hidden="true" altonclick="null" althref="null"></i>
    </button>
    <div id="menuOverlaySection" class="overlay overlay-contentpush" style="opacity: 1;">
        <button id="close-menu" class="overlay-close" altonclick="null" althref="null">
            <i class="closeMenuIcon fa fa-times" aria-hidden="true" altonclick="null" althref="null"></i>
        </button>
        <nav id="mainNav" role="navigation">
            <a id="menuTitle" class="navbar-brand page-scroll" altonclick="null" href="#">Ready</a>
            <hr id="menuTitleHr">
            <ul id="menuItems" class="nav navbar-nav">
                
                <li class="menuItemLi">
                    <a id="aboutMenuItem" class="menuItemA" altonclick="null" href="#about">About</a>
                </li>
                <li class="menuItemLi">
                    <a id="featuresMenuItem" class="menuItemA" altonclick="null" href="#features">Features</a>
                </li>
                <li class="menuItemLi">
                    <a id="galleryMenuItem" class="menuItemA" altonclick="null" href="#gallery">Gallery</a>
                </li>
                <li class="menuItemLi">
                    <a id="teamMenuItem" class="menuItemA" altonclick="null" href="#team">Team</a>
                </li>
                <li class="menuItemLi">
                    <a id="blogMenuItem" class="menuItemA" altonclick="null" href="#blog">Blog</a>
                </li>
                <li class="menuItemLi">
                    <a id="contactMenuItem" class="menuItemA" altonclick="null" href="#contact">Contact</a>
                </li>
                <li class="menuItemLi">
                    <a id="bookMenuItem" class="menuItemA" altonclick="null" href="/book">Book</a>
                </li>
            </ul>
        </nav>
    </div>
    <style>
        #mainMenu {
            word-break: break-word;
        }

        #mainMenu .floatingToolbox {
            z-index: 10000 !important;
        }

        #trigger-overlay {
            left: 50px;
            top: 50px;
            font-size: 30px;
            background: rgba(0,0,0,0);
            color: white;
            border: none;
            cursor: pointer;
        }

        .overlay nav {
            top: 40%;
        }

        #menuOverlaySection {
            background: rgba(0,0,0,0.5);
            width: 20%;
            min-width: 250px;
            word-wrap: break-word;
            overflow-y: scroll;
            overflow: -moz-scrollbars-none;
            -ms-overflow-style: none;
        }

        #menuOverlaySection::-webkit-scrollbar { 
            width: 0 !important 
        }

        #menuTitle {
            color: white;
            font-size: 40px;
            line-height: normal;
            text-transform: uppercase;
            display: table;
        }

        #menuTitleHr {
            border: 2px solid white;
            width: 90%;
            float: left;
            margin-left: 4%;
        }

        #close-menu {
            color: white;
            background: rgba(0,0,0,0);
            font-size: 30px;
            cursor: pointer;
        }

        #menuItems .menuItemA {
            color: white;
            transition: background 0.6s ease 0s !important;
            font-size: 20px;
            text-transform: uppercase;
            text-align: left;
        }

        #menuItems .menuItemA:hover, #menuItems .menuItemA:active, #menuItems .menuItemA:focus {
            background: rgb(255,159,78) !important;
            color: white;
        }

        .menuItemLi {
            width: 100%;
        }

        @media only screen and (max-width : 900px) {

            #menuOverlaySection {
                background: rgba(0,0,0,0.8);
            }
        }

        @media only screen and (max-width : 767px) {

            .overlay nav {
                top: 30%;
            }
        }
    </style>
</nav>
        <script>
            $(document).ready(function() {
                $('nav').fadeIn();
            });
        </script>
        <script src="/js/modernizer.js" class="overlayScript"></script>
        <script src="/js/bankers.js" class="overlayScript"></script>
        <script src="/js/menu.js" class="overlayScript"></script>
<header style="margin-bottom: 0px;">

        <div class="sectionOverlay" id="headerOverlay" style="background: rgba(0, 0, 0, 0.3)"></div>
        <div id="outerHeader" class="noCustomElement">
    <div id="headerContainer" class="noCustomElement">
        <div id="headerContent" class="row noCustomElement">
            <div id="mainBox" class="col-md-6 col-md-offset-3 noCustomElement">
                <div id="estDateWrap">
                    <span class="descriptions estSpan" altonclick="null" althref="null">EST</span>
                    <span class="descriptions estSpan" altonclick="null" althref="null"> | </span>
                    <span class="descriptions estSpan" altonclick="null" althref="null">2023</span>
                </div>
                <div id="headerTitleWrap"><h1 id="headerTitle" class="headerTitles" altonclick="null" althref="null">Ready To Respond</h1></div>
                <div id="headerSubtitleWrap"><h3 id="headerSubtitle" class="headerSubtitles" altonclick="null" althref="null">From Crisis to Recovery, Hand in Hand</h3></div>
                <div id="headerButtons"><div><a class="headerButton" altonclick="null" althref="null">Call Now</a></div></div>
            </div>
        </div>
    </div>
    <style type="text/css">

        #headerContent {
            color: white;
            text-align: center;
            word-break: break-word;
            overflow: hidden;
        }   

        #mainBox {
            border: 3px outset rgba(255,159,78,0.5);
            padding: 22px;
        }

        #estDateWrap {
            font-size: 20px;
        }

        .estSpan {
            padding: 16px
        }

        #headerTitle {
            font-size: 80px;
            width: 80%;
            margin: 20px auto;
            text-transform: uppercase;
        }

        #headerSubtitle {
            width: 80%;
            margin: 20px auto 15px;
            font-size: 20px;
        }

        .headerButton {
            color: white;
            text-decoration: none;
            cursor: pointer;
            padding: 6px 42px;
            background-color: transparent;
            border-radius: 3px;
            border: 4px solid rgba(255,159,78,0.5);
            transition: 0.5s;
            display: inline-block;
            margin-top: 20px;
        }

        .headerButton:hover {
            background-color: rgba(255,159,78,0.5);
            color: white;
            text-decoration: none;
        }

        header .customTitle {
            font-size: 30px;
            display: block;
        }

        header .customParagraph {
            font-size: 18px;
            display: block;
        }

        header .customLink {
            color: white;
            font-size: 20px;
            display: block;
            width: 100%;
        }

        header .customLink:hover {
            opacity: 0.4;
            text-decoration: none;
        }

        header .customIcon {
            font-size: 36px;
        }

        header .customTitle,
        header .customParagraph,
        header .customLink,
        header .customIcon,
        header .customButton,
        header .customImage,
        header .customEmbed {
            margin: 10px 0;
        }
        
        header #estDateWrap .customTitle,
        header #estDateWrap .customParagraph,
        header #estDateWrap .customLink,
        header #estDateWrap .customIcon,
        header #estDateWrap .customButton,
        header #estDateWrap .customImage,
        header #estDateWrap .customEmbed {
            margin: 10px 0 0;
        }
        
        header #headerTitleWrap .customTitle,
        header #headerTitleWrap .customParagraph,
        header #headerTitleWrap .customLink,
        header #headerTitleWrap .customIcon,
        header #headerTitleWrap .customButton,
        header #headerTitleWrap .customImage,
        header #headerTitleWrap .customEmbed {
            margin: 0 0 10px;
        }
        
        header #headerButtons .customTitle,
        header #headerButtons .customParagraph,
        header #headerButtons .customLink,
        header #headerButtons .customIcon,
        header #headerButtons .customButton,
        header #headerButtons .customImage,
        header #headerButtons .customEmbed {
            margin: 20px 0 0;
        }

        @media only screen and (max-width : 1024px) {

            #headerTitle {
                font-size: 54px;
            }
        }

        @media only screen and (max-width : 767px) {

            #mainBox {
                border-left: none;
                border-right: none;
            }

            #headerTitle {
                width: 95%;
            }
            
            #headerSubtitle {
                width: 90%;
                text-align: justify;
                text-align-last: center;
                font-size: 18px;
            }

            .headerButton {
                font-size: 12px;
                padding: 6px 30px;
            }

            header .customTitle {
                font-size: 24px;
            }

            header .customLink {
                color: white;
                font-size: 18px;
            }

            header #headerSubtitleWrap .customTitle,
            header #headerSubtitleWrap .customParagraph,
            header #headerSubtitleWrap .customLink,
            header #headerSubtitleWrap .customIcon,
            header #headerSubtitleWrap .customButton,
            header #headerSubtitleWrap .customImage,
            header #headerSubtitleWrap .customEmbed {
                margin: 10px 0 0;
            }
        }
        
        @media only screen and (max-width : 320px) {

            #headerTitle {
                font-size: 36px;
            }

            #headerSubtitle {
                font-size: 16px;
            }
        }
    </style>
</div>
        <style>

            header {
                background: url('/img/disaster-c9gQB-GiVyj-YWt4C-NJTmK-jxB7k.jpg');
                background-repeat: no-repeat;
                background-size: cover;
                background-position: top;
                background-attachment: fixed;
            }
            #headerLogoImage {
                position: fixed;
                left: 3%;
                bottom: 10px;
                width: 200px;
                max-width: 30%;
                z-index: 100;
            }
        </style>
        
        
        
    </header>
    
<section id="about">
            <div class="sectionOverlay" id="aboutOverlay" style="background: rgba(0, 0, 0, 0)"></div>
            <div id="outerAbout" class="outerSection noCustomElement">
    <div id="aboutContainer" class="sectionContainer noCustomElement">
        <div id="aboutContent" class="sectionContent container-fluid noCustomElement">
            <div class="row noCustomElement">
                <div id="aboutTitleWrap" class="col-sm-10 col-sm-offset-1">
                    <h2 id="aboutTitle" class="aboutTitles" altonclick="null" althref="null">About Us</h2>
                </div>
            </div>
            <div id="aboutRow" class="row noCustomElement">
                <div class="outerGrid col-lg-4 col-lg-offset-2 col-sm-5 col-sm-offset-1 noCustomElement">
                    <div class="innerGridTable noCustomElement">
                        <div class="innerTableContent noCustomElement">
                            <div id="aboutImage1" class="innerTableContent"><img class="aboutImages" src="/img/disaster-U0DRy-cShle-6zNzf-rYwsG-Fs7NC.jpg" altonclick="null" althref="null"></div>
                        </div>
                    </div>
                </div>
                <div id="aboutBottom" class="outerGrid col-lg-4 col-sm-5 noCustomElement">
                    <div class="innerGridTable noCustomElement">
                        <div class="innerTableContent noCustomElement">
                            <div id="aboutParagraph1Wrap"><p id="aboutParagraph1" class="aboutParagraph" altonclick="null" althref="null">The Disaster response recovery business can function admirably in light of the fact that the two sides - the customer just as the provider - rely upon the soundness of a trusting solution. We understand that this is a critical idea, which is why we take pride in our ability to always match these two values. Maintaining these values as our relationship begins is a core value of ours, and we are very excited to tell your more about what we do.</p></div>
                            <div id="aboutParagraph2Wrap"><p id="aboutParagraph2" class="aboutParagraph" altonclick="null" althref="null">We are one of the the top Disaster response recovery solutions in the area. We have been giving high caliber, intensely evaluated Disaster response recovery solutions to all who come to us for years. In that time, we have found out about client administration and the benefit of realizing our customers needs. We adore driving by ordinary and perceiving how extraordinary we can become together!</p></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <style>
        #about {
            color: black;
        }

        #about .aboutImageBg {
            color: white;
        }

        #aboutTitleWrap {
            text-align: center;
            margin-bottom: 40px;
        }

        #aboutTitle {
            font-size: 48px;
            margin-bottom: 15px;
        }

        #aboutRow {
            display: flex;
        }

        #aboutImage1 {
            text-align: right;
        }

        .aboutImages {
            width: 100%;
        }

        #about .aboutImageBg .aboutImages {
            border: 2px solid white;
        }

        #aboutBottom {
            padding-left: 20px;
        }

        .aboutParagraph {
            font-size: 16px;
            letter-spacing: 0.05em;
            line-height: 1.6;
        }

        #aboutParagraph1 {
            margin-bottom: 20px;
        }

        #aboutButtons {
            margin: 26px 0 64px;
        }

        #about .customTitle {
            font-size: 35px;
            display: block;
        }

        #about .customParagraph {
            font-size: 16px;
            letter-spacing: 0.05em;
            line-height: 1.6;
        }

        #about .customLink {
            color: black;
            font-size: 20px;
            width: 100%;
        }

        #about .aboutImageBg .customLink {
            color: white;
        }

        #about .customLink:hover {
            opacity: 0.5;
            text-decoration: none;
        }

        #about .customIcon {
            font-size: 36px;
        }

        #about .customTitle,
        #about .customParagraph,
        #about .customLink,
        #about .customIcon,
        #about .customButton,
        #about .customImage,
        #about .customEmbed {
            margin: 10px 0;
        }
        
        #about #aboutImage1 .customTitle,
        #about #aboutImage1 .customParagraph,
        #about #aboutImage1 .customLink,
        #about #aboutImage1 .customIcon,
        #about #aboutImage1 .customButton,
        #about #aboutImage1 .customImage,
        #about #aboutImage1 .customEmbed {
            margin: 20px 0 0;
        }
        
        #about #aboutParagraph1Wrap .customTitle,
        #about #aboutParagraph1Wrap .customParagraph,
        #about #aboutParagraph1Wrap .customLink,
        #about #aboutParagraph1Wrap .customIcon,
        #about #aboutParagraph1Wrap .customButton,
        #about #aboutParagraph1Wrap .customImage,
        #about #aboutParagraph1Wrap .customEmbed {
            margin: 0 0 20px;
        }

        @media only screen and (max-width : 800px) {

            #aboutTitle {
                font-size: 30px;
                margin-bottom: 0;
            }  

            #aboutBottom {
                margin-top: 36px;
            }

            #about .customTitle {
                font-size: 30px;
            }
        }

        @media only screen and (max-width : 767px) {

            #aboutRow {
                display: initial;
            }

            #aboutTitle {
                font-size: 42px;
                margin-bottom: 24px;
            }

            #aboutImage1 {
                text-align: center;
            }

            #aboutBottom {
                padding-left: 0;
            }

            #about #aboutTitleWrap .customTitle,
            #about #aboutTitleWrap .customParagraph,
            #about #aboutTitleWrap .customLink,
            #about #aboutTitleWrap .customIcon,
            #about #aboutTitleWrap .customButton,
            #about #aboutTitleWrap .customImage,
            #about #aboutTitleWrap .customEmbed {
                margin: 0;
            }

            #about #aboutTitleWrap .customImage,
            #about #aboutTitleWrap .customEmbed {
                padding: 0 15px;
            }
        }
    </style>
</div>
            <style>
                #aboutContainer {
                background: rgb(255,255,255);
            }
            </style>
        </section>
<section id="features">
            <div class="sectionOverlay" id="featuresOverlay" style="background: rgba(0 ,0, 0, 0.5)"></div>
            <div id="outerFeatures" class="outerSection noCustomElement">
    <div id="featuresContainer" class="sectionContainer featuresImageBg noCustomElement">
        <div id="featuresContent" class="sectionContent container-fluid noCustomElement">
            <div class="row noCustomElement">
                <div id="featuresTop" class="col-sm-10 col-sm-offset-1 col-xs-12 noCustomElement">
                    <div id="featuresTitleWrap"><h2 id="featuresTitle" class="featuresTitles" altonclick="null" althref="null">Our Qualities</h2></div>
                    <div id="featuresSubtitleWrap"><h4 id="featuresSubtitle" class="featuresSubtitles" altonclick="null" althref="null"></h4></div>
                </div>
            </div>
            <div class="row noCustomElement">
                <div class="col-md-10 col-md-offset-1 col-sm-12 col-xs-12 noCustomElement">
                    <div id="featuresRowContainer" class="noCustomElement">
                        <!-- featuresTemplate start --><div class="features3 row noCustomElement">
                            <div class="featuresTemplate outerGrid col-sm-4 noCustomElement">
                                <div class="innerGridTable noCustomElement">
                                    <div class="featuresTemplateInner innerTableContent noCustomElement">
                                        <div class="featuresHeaderWrap"><h5 class="featuresHeader" altonclick="null" althref="null">Reliable</h5></div>
                                        <div class="featuresHrWrap"><hr class="featuresHr"></div>
                                        <div class="outerGrid col-sm-12 col-xs-12 noCustomElement">
                                            <div class="innerGridTable noCustomElement">
                                                <div class="innerTableContent noCustomElement">
                                                    <div class="featuresIconRow row">
                                                        <div class="featuresIconOuter outerGrid col-lg-4 col-lg-offset-1 col-sm-4 col-xs-4 noCustomElement">
                                                            <div class="innerGridTable noCustomElement">
                                                                <div class="featuresIcons innerTableContent"><i class="featuresIcon fa fa-lock" altonclick="null" althref="null"></i></div>
                                                            </div>
                                                        </div>
                                                        <div class="outerGrid col-lg-6 col-sm-8 col-xs-8 noCustomElement">
                                                            <div class="innerGridTable noCustomElement">
                                                                <div class="featuresTextWrap innerTableContent noCustomElement">
                                                                    <p class="featuresText" altonclick="null" althref="null">You can count on us to make sure your project is completed with care.</p>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="featuresTemplate outerGrid col-sm-4 noCustomElement">
                                <div class="innerGridTable noCustomElement">
                                    <div class="featuresTemplateInner innerTableContent noCustomElement">
                                        <div class="featuresHeaderWrap"><h5 class="featuresHeader" altonclick="null" althref="null">Global</h5></div>
                                        <div class="featuresHrWrap"><hr class="featuresHr"></div>
                                        <div class="outerGrid col-sm-12 col-xs-12 noCustomElement">
                                            <div class="innerGridTable noCustomElement">
                                                <div class="innerTableContent noCustomElement">
                                                    <div class="featuresIconRow row">
                                                        <div class="featuresIconOuter outerGrid col-lg-4 col-lg-offset-1 col-sm-4 col-xs-4 noCustomElement">
                                                            <div class="innerGridTable noCustomElement">
                                                                <div class="featuresIcons innerTableContent"><i class="featuresIcon fa fa-globe" altonclick="null" althref="null"></i></div>
                                                            </div>
                                                        </div>
                                                        <div class="outerGrid col-lg-6 col-sm-8 col-xs-8 noCustomElement">
                                                            <div class="innerGridTable noCustomElement">
                                                                <div class="featuresTextWrap innerTableContent noCustomElement">
                                                                    <p class="featuresText" altonclick="null" althref="null">The fact that our work has spread to regions all of the globe is a true indication of our quality.</p>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="featuresTemplate outerGrid col-sm-4 noCustomElement">
                                <div class="innerGridTable noCustomElement">
                                    <div class="featuresTemplateInner innerTableContent noCustomElement">
                                        <div class="featuresHeaderWrap"><h5 class="featuresHeader" altonclick="null" althref="null">Dedicated</h5></div>
                                        <div class="featuresHrWrap"><hr class="featuresHr"></div>
                                        <div class="outerGrid col-sm-12 col-xs-12 noCustomElement">
                                            <div class="innerGridTable noCustomElement">
                                                <div class="innerTableContent noCustomElement">
                                                    <div class="featuresIconRow row">
                                                        <div class="featuresIconOuter outerGrid col-lg-4 col-lg-offset-1 col-sm-4 col-xs-4 noCustomElement">
                                                            <div class="innerGridTable noCustomElement">
                                                                <div class="featuresIcons innerTableContent"><i class="featuresIcon fas fa-users" altonclick="null" althref="null"></i></div>
                                                            </div>
                                                        </div>
                                                        <div class="outerGrid col-lg-6 col-sm-8 col-xs-8 noCustomElement">
                                                            <div class="innerGridTable noCustomElement">
                                                                <div class="featuresTextWrap innerTableContent noCustomElement">
                                                                    <p class="featuresText" altonclick="null" althref="null">Loving what you do is the first step in delivering quality work every time - and we do.</p>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            </div><div class="features3 row noCustomElement">
                            <div class="featuresTemplate outerGrid col-sm-4 noCustomElement">
                                <div class="innerGridTable noCustomElement">
                                    <div class="featuresTemplateInner innerTableContent noCustomElement">
                                        <div class="featuresHeaderWrap"><h5 class="featuresHeader" altonclick="null" althref="null">On Time</h5></div>
                                        <div class="featuresHrWrap"><hr class="featuresHr"></div>
                                        <div class="outerGrid col-sm-12 col-xs-12 noCustomElement">
                                            <div class="innerGridTable noCustomElement">
                                                <div class="innerTableContent noCustomElement">
                                                    <div class="featuresIconRow row">
                                                        <div class="featuresIconOuter outerGrid col-lg-4 col-lg-offset-1 col-sm-4 col-xs-4 noCustomElement">
                                                            <div class="innerGridTable noCustomElement">
                                                                <div class="featuresIcons innerTableContent"><i class="featuresIcon fa fa-calendar" altonclick="null" althref="null"></i></div>
                                                            </div>
                                                        </div>
                                                        <div class="outerGrid col-lg-6 col-sm-8 col-xs-8 noCustomElement">
                                                            <div class="innerGridTable noCustomElement">
                                                                <div class="featuresTextWrap innerTableContent noCustomElement">
                                                                    <p class="featuresText" altonclick="null" althref="null">Our projects are never late. They are always completed with care and delivered on time.</p>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="featuresTemplate outerGrid col-sm-4 noCustomElement">
                                <div class="innerGridTable noCustomElement">
                                    <div class="featuresTemplateInner innerTableContent noCustomElement">
                                        <div class="featuresHeaderWrap"><h5 class="featuresHeader" altonclick="null" althref="null">Professional</h5></div>
                                        <div class="featuresHrWrap"><hr class="featuresHr"></div>
                                        <div class="outerGrid col-sm-12 col-xs-12 noCustomElement">
                                            <div class="innerGridTable noCustomElement">
                                                <div class="innerTableContent noCustomElement">
                                                    <div class="featuresIconRow row">
                                                        <div class="featuresIconOuter outerGrid col-lg-4 col-lg-offset-1 col-sm-4 col-xs-4 noCustomElement">
                                                            <div class="innerGridTable noCustomElement">
                                                                <div class="featuresIcons innerTableContent"><i class="featuresIcon fa fa-briefcase" altonclick="null" althref="null"></i></div>
                                                            </div>
                                                        </div>
                                                        <div class="outerGrid col-lg-6 col-sm-8 col-xs-8 noCustomElement">
                                                            <div class="innerGridTable noCustomElement">
                                                                <div class="featuresTextWrap innerTableContent noCustomElement">
                                                                    <p class="featuresText" altonclick="null" althref="null">Every step of the process will be handled by our team with true professionalism.</p>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="featuresTemplate outerGrid col-sm-4 noCustomElement">
                                <div class="innerGridTable noCustomElement">
                                    <div class="featuresTemplateInner innerTableContent noCustomElement">
                                        <div class="featuresHeaderWrap"><h5 class="featuresHeader" altonclick="null" althref="null">Observant</h5></div>
                                        <div class="featuresHrWrap"><hr class="featuresHr"></div>
                                        <div class="outerGrid col-sm-12 col-xs-12 noCustomElement">
                                            <div class="innerGridTable noCustomElement">
                                                <div class="innerTableContent noCustomElement">
                                                    <div class="featuresIconRow row">
                                                        <div class="featuresIconOuter outerGrid col-lg-4 col-lg-offset-1 col-sm-4 col-xs-4 noCustomElement">
                                                            <div class="innerGridTable noCustomElement">
                                                                <div class="featuresIcons innerTableContent"><i class="featuresIcon fas fa-eye" altonclick="null" althref="null"></i></div>
                                                            </div>
                                                        </div>
                                                        <div class="outerGrid col-lg-6 col-sm-8 col-xs-8 noCustomElement">
                                                            <div class="innerGridTable noCustomElement">
                                                                <div class="featuresTextWrap innerTableContent noCustomElement">
                                                                    <p class="featuresText" altonclick="null" althref="null">We keep a close eye on every component of our work to ensure nothing is left out.</p>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            </div><!-- featuresTemplate end -->
                    </div>
                </div>
            </div>
        </div>
    </div>
    <style>
        #features {
            color: black;
        }

        #features .featuresImageBg {
            color: white;
        }

        #featuresTop {
            text-align: center;
        }

        #featuresTitleWrap {
            margin: 0 0 25px;
        }

        #featuresTitle {
            color: rgb(255,159,78);
            font-size: 45px;
            letter-spacing: 0.09em;
            margin: 0 0 10px;
        }

        #features .featuresImageBg #featuresTitle {
            color: white;
        }

        #featuresSubtitleWrap {
            margin: 0 0 50px;
        }

        #featuresSubtitle {
            font-size: 28px;
            letter-spacing: 0.09em;
            font-style: italic;
        }

        .features3, 
        .featuresIconRow {
            display: flex;
        }

        .featuresTemplate {
            box-shadow: 0 0 8px 1px rgb(255,159,78);
            text-align: center;
            margin: 10px;
        }

        #features .featuresImageBg .featuresTemplate {
            box-shadow: 0 0 8px 1px white;
        }

        .featuresTemplateInner {
            padding: 12px 0;
        }

        .featuresHeader {
            color: rgb(255,159,78);
            font-size: 20px;
        }

        #features .featuresImageBg .featuresHeader {
            color: white;
        }

        .featuresHr {
            border: 1px solid black;
            margin: 5px auto 10px;
        }

        #features .featuresImageBg .featuresHr {
            border-color: white;
        }

        .featuresIcon {
            color: rgb(255,159,78);
            font-size: 65px;
        }

        #features .featuresImageBg .featuresIcon {
            color: white;
        }

        .featuresText {
            font-size: 12px;
        }

        #features .customTitle {
            color: rgb(255,159,78);
            font-size: 45px;
            letter-spacing: 0.09em;
            display: block;
        }

        #features #featuresRowContainer .customTitle {
            font-size: 20px;
            letter-spacing: normal;
        }

        #features .featuresImageBg .customTitle {
            color: white;
        }

        #features .customParagraph {
            font-size: 18px;
            display: block;
        }
        
        #features #featuresRowContainer .customParagraph {
            font-size: 12px;
        }

        #features .customLink {
            color: rgb(255,159,78);
            font-size: 18px;
            display: block;
            width: 100%;
        }

        #features #featuresRowContainer .customLink {
            font-size: 12px;
        }

        #features .featuresImageBg .customLink {
            color: white;
        }

        #features .customLink:hover {
            opacity: 0.6;
            text-decoration: none;
        }

        #features .customIcon {
            font-size: 30px;
        }

        #features .customTitle,
        #features .customParagraph,
        #features .customLink,
        #features .customIcon, 
        #features .customButton,
        #features .customImage,
        #features .customEmbed {
            margin: 10px 0;
        }

        #features #featuresTitleWrap .customIcon, 
        #features #featuresTitleWrap .customButton,
        #features #featuresTitleWrap .customImage {
            margin: 5px 0 0;
        }
        
        #features #featuresSubtitleWrap .customIcon, 
        #features #featuresSubtitleWrap .customButton,
        #features #featuresSubtitleWrap .customImage {
            margin: 0 0 10px;
        }
        
        #features .featuresHeaderWrap .customTitle,
        #features .featuresHeaderWrap .customParagraph,
        #features .featuresHeaderWrap .customLink,
        #features .featuresHeaderWrap .customEmbed {
            margin: 10px 0 15px;
        }

        #features .featuresHeaderWrap .customIcon, 
        #features .featuresHeaderWrap .customButton,
        #features .featuresHeaderWrap .customImage {
            margin: 0 0 5px;
        }
        
        #features .featuresHrWrap .customIcon, 
        #features .featuresHrWrap .customButton,
        #features .featuresHrWrap .customImage {
            margin: 0 0 10px;
        }

        #features .featuresTextWrap .customTitle,
        #features .featuresTextWrap .customParagraph,
        #features .featuresTextWrap .customLink,
        #features .featuresTextWrap .customIcon, 
        #features .featuresTextWrap .customButton,
        #features .featuresTextWrap .customImage,
        #features .featuresTextWrap .customEmbed {
            margin: 0 0 10px;
        }

        @media only screen and (max-width : 991px) {

            .featuresIcon {
                font-size: 45px;
            }
        }

        @media only screen and (max-width : 767px) {

            .features3 {
                display: grid;
            }

            .featuresTemplate {
                padding-bottom: 10px;
                margin-top: 25px;
            }
        }
    </style>
</div>
            <style>
                #featuresContainer {
                background: url('/img/disaster-c9gQB-GiVyj-YWt4C-NJTmK-jxB7k.jpg');
                background-repeat: no-repeat;
                background-size: cover;
                background-position: center;
                background-attachment: fixed;
            }
            </style>
        </section>
<section id="gallery">
            <script>
                // script start 
                $.browser = {}; $.support.opacity = true;
                // script end
            </script>
            <script src="https://cdnjs.cloudflare.com/ajax/libs/fancybox/3.1.25/jquery.fancybox.min.js"></script>
            <script src="/lib/fancybox/jquery.easing-1.3.pack.js"></script>
            <script src="/lib/fancybox/jquery.mousewheel-3.0.4.pack.js"></script>
            <link href="/lib/fancybox/jquery.fancybox-1.3.4.css" rel="stylesheet">
            <div class="sectionOverlay" id="galleryOverlay" style="background: rgba(0, 0, 0, 0)"></div>
            <div id="outerGallery" class="outerSection noCustomElement">
    <div id="galleryContainer" class="sectionContainer noCustomElement">
        <div id="galleryContent" class="sectionContent container-fluid noCustomElement">
            <div class="row noCustomElement">
                <div class="col-sm-10 col-sm-offset-1 col-xs-12 noCustomElement">
                    <div id="galleryTop" class="row noCustomElement">
                        <div class="col-sm-8 col-sm-offset-2 col-xs-12 noCustomElement">
                            <div id="galleryTitleWrap"><h2 id="galleryTitle" class="galleryTitles" altonclick="null" althref="null">Our Projects</h2></div>
                            <div id="gallerySubtitleWrap"><h4 id="gallerySubtitle" class="gallerySubtitles" altonclick="null" althref="null"></h4></div>
                        </div>
                        <div class="col-sm-12 col-xs-12 noCustomElement">
                            <div id="categoryButtonContainer">
                                <div id="categoryButtonRow" class="buttons4 noCustomElement">
                                    <div class="categoryButtonContainer noCustomElement">
                                        <div class="categoryButtonWrap noCustomElement"><a id="allCategoriesBtn" class="categoryButton allCategoryButton categoryButtonSelected" data-filter="all" altonclick="null" althref="null">All</a></div>
                                    </div>
                                    <div class="categoryButtonContainer categoryButtonOuter noCustomElement">
                                        <div class="categoryButtonWrap noCustomElement"><a class="categoryButton" data-filter="category1" altonclick="null" althref="null">Category 1</a></div>
                                    </div>
                                    <div class="categoryButtonContainer categoryButtonOuter noCustomElement">
                                        <div class="categoryButtonWrap noCustomElement"><a class="categoryButton" data-filter="category2" altonclick="null" althref="null">Category 2</a></div> 
                                    </div>
                                    <div class="categoryButtonContainer categoryButtonOuter noCustomElement">
                                        <div class="categoryButtonWrap noCustomElement"><a class="categoryButton" data-filter="category3" altonclick="null" althref="null">Category 3</a></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div id="galleryRowContainer" class="noCustomElement">
                        <!-- galleryTemplate start --><div class="gallery4 row">
                            <div class="categoryFilter col-sm-3 col-xs-12 noCustomElement category1" style="display: block;">
                                <div class="galleryImage noCustomElement">
                                    <a rel="scrollGroup" href="/img/disaster-DpDTD-dXayt-LH0dB-Cmb7k-b4soY.jpg" class="fancybox" title="Photo 1" altonclick="null">
                                        <img class="galleryImages img-fluid" src="/img/disaster-DpDTD-dXayt-LH0dB-Cmb7k-b4soY.jpg" altonclick="null" althref="null">
                                        <div class="galleryOverlay overlayFade overlayFadeToggle noCustomElement">
                                            <h4 class="galleryText" altonclick="null" althref="null">Photo 1</h4>
                                        </div>
                                    </a>
                                </div>
                            </div>
                            
                            <div class="categoryFilter col-sm-3 col-xs-12 noCustomElement category2" style="display: block;">
                                <div class="galleryImage noCustomElement">
                                    <a rel="scrollGroup" href="/img/disaster-GV79V-f8Bgq-zArL1-twei9-uTG1I.jpg" class="fancybox" title="Photo 2" altonclick="null">
                                        <img class="galleryImages img-fluid" src="/img/disaster-GV79V-f8Bgq-zArL1-twei9-uTG1I.jpg" altonclick="null" althref="null">
                                        <div class="galleryOverlay overlayFade overlayFadeToggle noCustomElement">
                                            <h4 class="galleryText" altonclick="null" althref="null">Photo 2</h4>
                                        </div>
                                    </a>
                                </div>
                            </div>
                            
                            <div class="categoryFilter col-sm-3 col-xs-12 noCustomElement category3" style="display: block;">
                                <div class="galleryImage noCustomElement">
                                    <a rel="scrollGroup" href="/img/disaster-vcZb9-yVErJ-u8wTJ-upRYE-wuKpE.jpg" class="fancybox" title="Photo 3" altonclick="null">
                                        <img class="galleryImages img-fluid" src="/img/disaster-vcZb9-yVErJ-u8wTJ-upRYE-wuKpE.jpg" altonclick="null" althref="null">
                                        <div class="galleryOverlay overlayFade overlayFadeToggle noCustomElement">
                                            <h4 class="galleryText" altonclick="null" althref="null">Photo 3</h4>
                                        </div>
                                    </a>
                                </div>
                            </div>
                            
                            <div class="categoryFilter col-sm-3 col-xs-12 noCustomElement category1" style="display: block;">
                                <div class="galleryImage noCustomElement">
                                    <a rel="scrollGroup" href="/img/disaster-gNzda-2gSsl-UlAOh-r56rK-6LVw3.jpg" class="fancybox" title="Photo 4" altonclick="null">
                                        <img class="galleryImages img-fluid" src="/img/disaster-gNzda-2gSsl-UlAOh-r56rK-6LVw3.jpg" altonclick="null" althref="null">
                                        <div class="galleryOverlay overlayFade overlayFadeToggle noCustomElement">
                                            <h4 class="galleryText" altonclick="null" althref="null">Photo 4</h4>
                                        </div>
                                    </a>
                                </div>
                            </div>
                            </div><!-- galleryTemplate end -->
                    </div>
                </div>
            </div>
        </div>
    </div>
    <style>
        #gallery {
            color: black;
        }

        #gallery .galleryImageBg {
            color: white;
        }

        #galleryContent {
            padding-bottom: 160px;
        }

        #galleryContent {
            word-wrap: break-word;
            text-align: center;
            background-color: rgba(255,159,78,0.2);
        }

        #galleryTitle {
            font-size: 50px;
            margin-bottom: 15px;
        }

        #gallerySubtitle {
            font-size: 25px;
            margin-bottom: 50px;
        }

        .categoryButtonContainer {
            display: inline-block;
            margin-bottom: 25px;
        }

        .categoryButton {
            font-size: 15px;
            color: black;
            padding: 6px 32px;
            cursor: pointer;
            background-color: white;
            border: 2px solid white;
            border-radius: 2px;
            margin: 5px;
            transition: 0.4s;
            text-decoration: none;
            display: inline-block;
        }

        #gallery .galleryImageBg .categoryButton {
            color: white;
            background-color: transparent;
        }

        .categoryButton:hover,
        .categoryButton:focus,
        .categoryButtonSelected {
            color: black;
            border: 2px solid black;
            background-color: white;
            text-decoration: none;
        }

        #gallery .galleryImageBg .categoryButton:hover,
        #gallery .galleryImageBg .categoryButton:focus,
        #gallery .galleryImageBg .categoryButtonSelected {
            border-color: white;
            background-color: rgb(255,159,78);
        }

        .galleryMainRow {
            display: block;
            margin-top: 40px;
        }

        .categoryFilter {
            padding: 1px;
        }

        .galleryImage a {
            border: 10px solid white;
        }

        .fancybox {
            padding: 0;
        }

        .galleryImages {
            height: 300px;
            width: 100%;
            object-fit: cover;
            display: block;
        }

        #fancybox-content {
            background: white;
        }

        #fancybox-title {
            margin-left: 0 !important;
            background: white;
        }

        #fancybox-title-over {
            color: black;
            font-size: 20px;
            font-style: italic;
            text-align: center;
        }

        .galleryOverlay {
            position: absolute;
            transition: all .3s ease;
            opacity: 0;
            transition: 0.9s;
            z-index: 1100;
        }

        .fancybox:hover .galleryOverlay {
            opacity: 1;
        }

        .galleryText {
            color: white;
            text-shadow: 1px 1px rgb(255,159,78);
            position: absolute;
            bottom: 0;
            left: 45%;
            transform: translate(-50%,-50%);
            font-size: 20px;
        }

        .overlayFade {
            height: 100%;
            width: 99%;
            top: 0;
            padding-right: 0;
        }

        .galleryTextGone {
            display: none;
        }

        #fancybox-close {
            right: -35px;
        }

        #fancybox-right {
            right: -20px;
        }

        #fancybox-bg-nw,
        #fancybox-bg-ne,
        #fancybox-bg-sw,
        #fancybox-bg-se {
            display: none;
        }

        /* * * * * * * * * */

        #gallery .customTitle {
            font-size: 40px;
            display: block;
        }

        #gallery .customParagraph {
            font-size: 18px;
            display: block;
        }

        #gallery .customLink {
            color: black;
            font-size: 18px;
            display: block;
            width: 100%;
        }

        #gallery .galleryImageBg .customLink {
            color: white;
        }

        #gallery .customLink:hover {
            opacity: 0.6;
            text-decoration: none;
        }

        #gallery .customIcon {
            font-size: 32px;
        }

        #gallery .customTitle,
        #gallery .customParagraph,
        #gallery .customLink,
        #gallery .customIcon, 
        #gallery .customButton,
        #gallery .customImage,
        #gallery .customEmbed {
            margin: 10px 0;
        }

        @media only screen and (max-width : 1050px) {

            .galleryImages {
                height: 250px;
            }

            .categoryButton {
                padding: 6px 20px;
            }

            .galleryOverlay {
                display: none;
            }

            #fancybox-left, #fancybox-right {
                display: block !important;
                opacity: 0.5;
            }
        }
        
        @media only screen and (max-width : 800px) {

            .galleryImages {
                height: 200px;
            }
        }
                        
        @media only screen and (max-width : 767px) {

            #galleryTitle {
                font-size: 40px;
                margin-top: 80px;
            }

            #gallerySubtitle {
                font-size: 22px;
            }

            #categoryButtonRow {
                display: initial;
            }

            .galleryImages {
                height: 350px;
            }
        }
    </style>
    <script>
    // script start

        var setCategoryClicks = function () {
            $(".categoryButton").unbind();
            $('.categoryButton').click(function(){
                // let offsetHeight = document.getElementById('galleryRowContainer').offsetHeight.toString() + 'px';
                var value = $(this).attr('data-filter');
                // $('#galleryRowContainer').css({'min-height':offsetHeight}); 

                if (value === 'all') {
                    $('.categoryFilter').show('1000');
                    $(this).addClass('categoryButtonSelected');
                    $('.categoryButton').not(this).removeClass('categoryButtonSelected');
                } else if ($(this).hasClass('categoryButtonSelected')) {
                    $('.categoryFilter').show('1000');
                    $(this).removeClass('categoryButtonSelected');
                    $('.allCategoryButton').addClass('categoryButtonSelected');
                }
                else {
                    $('.categoryFilter').not('.' + value).hide('3000');
                    $('.categoryFilter').filter('.' + value).show('3000');
                    $('.allCategoryButton').removeClass('categoryButtonSelected');
                    $('.categoryButton').not(this).removeClass('categoryButtonSelected');
                    $(this).toggleClass('categoryButtonSelected');
                }

                // setTimeout(function(){
                //     $('#galleryRowContainer').animate({'min-height':'0'});
                // },3000)

                $('.fancybox').click(function() {
                    $('.galleryText').addClass('galleryTextGone');
                    $('.overlayFadeToggle').removeClass('galleryOverlay').removeClass('overlayFade');
                })

                document.getElementById('fancybox-overlay').onclick = function() {
                    document.getElementById('fancybox-close').click();
                    window.event.preventDefault();
                    window.event.stopPropagation();
                }

                $('#fancybox-close').click(function(){
                    $('.galleryText').removeClass('galleryTextGone');
                    $('.overlayFadeToggle').addClass('galleryOverlay').addClass('overlayFade');
                })
            });

            $("a[rel=scrollGroup]").fancybox({
                'transitionIn'		: 'fade',
                'transitionOut'		: 'fade',
                'titlePosition' 	: 'inside',
                'type'              : 'image',
                'titleFormat'		: function(title) {
                    return '<span id="fancybox-title-over">' + title + '</span>';
                }
            });
        }
    // script end
    </script>
</div>
            <style>
                #galleryContainer {
                background: rgb(255,255,255);
            }
            </style>
            <script>
                $(document).ready(function(){
                    setCategoryClicks();
                });
            </script>
        </section>

<section id="team">
            <div class="sectionOverlay" id="teamOverlay" style="background: rgba(0 ,0, 0, 0.5)"></div>
            <div id="outerTeam" class="outerSection noCustomElement">
    <div id="teamContainer" class="sectionContainer teamImageBg noCustomElement">
        <div id="teamContent" class="sectionContent container-fluid noCustomElement">
            <div id="teamTop" class="row noCustomElement">
                <div class="col-sm-10 col-sm-offset-1 noCustomElement">
                    <div id="teamTitleWrap"><h2 id="teamTitle" class="teamTitles" altonclick="null" althref="null">Our Leadership</h2></div>
                </div>
            </div>
            <div class="row noCustomElement">
                <div class="col-sm-10 col-sm-offset-1 noCustomElement">
                    <div id="teamRowContainer" class="noCustomElement">
                        <!-- teamTemplate start --><div class="team3 row noCustomElement">
                            <div class="teamTemplate outerGrid col-md-4 col-sm-4 col-xs-12 noCustomElement">
                                <div class="teamMemberWrapOuter innerGridTable noCustomElement">
                                    <div class="teamMemberWrap innerTableContent noCustomElement">
                                        <div class="teamMemberImage"><img class="teamMemberImages" src="/img/team/EricHernandez.jpg" altonclick="null" althref="null"></div>
                                        <div class="teamMemberNameWrap"><h3 class="teamMemberName" altonclick="null" althref="null">Eric Hernandez</h3></div>
                                        <div class="teamMemberTitleWrap"><h3 class="teamMemberTitle" altonclick="null" althref="null">Chief Executive Officer</h3></div>
                                        <div class="teamMemberTextWrap"><p class="teamMemberText" altonclick="null" althref="null">Eric, our founder and director, boasts years of industry expertise and an inspirational commitment to our vision. Without leadership like this, we would not be who we are today.</p></div>
                                        <div class="teamIconRow">
                                            <i class="teamIcon teamFacebook fab fa-facebook-f" altonclick="null" althref="null"></i>
                                            <i class="teamIcon teamTwitter fab fa-twitter" altonclick="null" althref="null"></i>
                                            <i class="teamIcon teamLinkedin fab fa-linkedin-in" altonclick="null" althref="null"></i>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="teamTemplate outerGrid col-md-4 col-sm-4 col-xs-12 noCustomElement">
                                <div class="teamMemberWrapOuter innerGridTable noCustomElement">
                                    <div class="teamMemberWrap innerTableContent noCustomElement">
                                        <div class="teamMemberImage"><img class="teamMemberImages" src="/img/team/MeganGarcia.jpg" altonclick="null" althref="null"></div>
                                        <div class="teamMemberNameWrap"><h3 class="teamMemberName" altonclick="null" althref="null">Megan Garcia</h3></div>
                                        <div class="teamMemberTitleWrap"><h3 class="teamMemberTitle" altonclick="null" althref="null">Head of Sales</h3></div>
                                        <div class="teamMemberTextWrap"><p class="teamMemberText" altonclick="null" althref="null">Megan was instrumental in our record breaking sales. She joined the team in 2016 and her leadership continues to drive the progress of the sales team.</p></div>
                                        <div class="teamIconRow">
                                            <i class="teamIcon teamFacebook fab fa-facebook-f" altonclick="null" althref="null"></i>
                                            <i class="teamIcon teamTwitter fab fa-twitter" altonclick="null" althref="null"></i>
                                            <i class="teamIcon teamLinkedin fab fa-linkedin-in" altonclick="null" althref="null"></i>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="teamTemplate outerGrid col-md-4 col-sm-4 col-xs-12 noCustomElement">
                                <div class="teamMemberWrapOuter innerGridTable noCustomElement">
                                    <div class="teamMemberWrap innerTableContent noCustomElement">
                                        <div class="teamMemberImage"><img class="teamMemberImages" src="/img/team/EmilyYoung.jpg" altonclick="null" althref="null"></div>
                                        <div class="teamMemberNameWrap"><h3 class="teamMemberName" altonclick="null" althref="null">Emily Young</h3></div>
                                        <div class="teamMemberTitleWrap"><h3 class="teamMemberTitle" altonclick="null" althref="null">Lead Developer</h3></div>
                                        <div class="teamMemberTextWrap"><p class="teamMemberText" altonclick="null" althref="null">Emily is a certified computer engineer and has won numerous awards in the field. She has over fifteen years experience as an engineer in a variety of technical platforms.</p></div>
                                        <div class="teamIconRow">
                                            <i class="teamIcon teamFacebook fab fa-facebook-f" altonclick="null" althref="null"></i>
                                            <i class="teamIcon teamTwitter fab fa-twitter" altonclick="null" althref="null"></i>
                                            <i class="teamIcon teamLinkedin fab fa-linkedin-in" altonclick="null" althref="null"></i>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            </div><!-- teamTemplate end -->
                    </div>
                </div>
            </div>
        </div>
    </div>
    <style>
        #team {
            color: black;
        }

        #team .teamImageBg {
            color: white;
        }

        #teamContent {
            text-align: center;
        }

        #teamTitle {
            font-size: 40px;
        }

        #teamSubtitle {
            font-size: 18px;
        }

        .team3 {
            /* display: flex; */
            margin: 0;
        }

        .teamTemplate {
            padding: 0;
            margin-top: 30px;
        }

        .teamMemberWrapOuter {
            padding: 20px;
            word-wrap: break-word;
        }

        .teamMemberWrap {
            padding-top: 20px;
            background: white;
            color: black;
            padding: 10px 5px;
        }

        .teamMemberImages {
            width: 70%;
            height: 260px;
            object-fit: cover;
        }

        .teamMemberNameWrap {
            margin: 20px 0 10px;
        }

        .teamMemberName {
            font-size: 28px;
            margin: 0;
        }
        
        .teamMemberTitle {
            margin: 0 0 15px;
            font-size: 20px;
        }

        .teamMemberText {
            font-size: 14px;
        }

        .teamIconRow {
            margin: 20px 0;
            width: 100%;
        }

        .teamIcon {
            display: inline;
            font-size: 20px;
            margin: 0 15px;
            cursor: pointer;
            transition: 0.4s;
        }

        .teamIcon:hover{ 
            opacity: 0.6;
        }

        /* * * * * * * * */

        #team .customTitle {
            font-size: 40px;
            display: block;
        }

        #team #teamRowContainer .customTitle {
            font-size: 28px;
        }

        #team .customParagraph {
            font-size: 16px;
            display: block;
        }

        #team #teamRowContainer .customLink,
        #team #teamRowContainer .customParagraph {
            font-size: 14px;
        }

        #team .customLink {
            color: black;
            font-size: 16px;
            display: block;
            width: 100%;
        }

        #team .teamImageBg .customLink {
            color: white;
        }

        #team .customLink:hover {
            opacity: 0.6;
            text-decoration: none;
        }

        #team .customIcon {
            font-size: 30px;
        }

        #team .customTitle,
        #team .customParagraph,
        #team .customLink,
        #team .customIcon,
        #team .customButton,
        #team .customImage,
        #team .customEmbed {
            margin: 10px 0;
        }
        
        #team #teamTitleWrap .customTitle,
        #team #teamTitleWrap .customParagraph,
        #team #teamTitleWrap .customLink,
        #team #teamTitleWrap .customEmbed,
        #team .teamMemberImage .customIcon,
        #team .teamMemberImage .customButton,
        #team .teamMemberImage .customImage,
        #team .teamMemberNameWrap .customIcon,
        #team .teamMemberNameWrap .customButton,
        #team .teamMemberNameWrap .customImage,
        #team .teamIconRow .customTitle,
        #team .teamIconRow .customParagraph,
        #team .teamIconRow .customLink,
        #team .teamIconRow .customIcon,
        #team .teamIconRow .customButton,
        #team .teamIconRow .customImage,
        #team .teamIconRow .customEmbed {
            margin: 10px 0 0;
        }

        #team #teamTitleWrap .customIcon,
        #team #teamTitleWrap .customButton,
        #team #teamTitleWrap .customImage {
            margin: 0;
        }

        #team .teamMemberTitleWrap .customIcon,
        #team .teamMemberTitleWrap .customButton,
        #team .teamMemberTitleWrap .customImage,
        #team .teamMemberTextWrap .customTitle,
        #team .teamMemberTextWrap .customParagraph,
        #team .teamMemberTextWrap .customLink,
        #team .teamMemberTextWrap .customIcon,
        #team .teamMemberTextWrap .customButton,
        #team .teamMemberTextWrap .customImage,
        #team .teamMemberTextWrap .customEmbed {
            margin: 0 0 10px;
        }

        @media only screen and (max-width : 1050px) {

            .teamIcon {
                margin: 0 10px;
            }

            .teamMemberImages {
                width: 95%;
            }
        }

        @media only screen and (max-width : 991px) {

            .teamIcon {
                margin: 0 4px;
            }
        }

        @media only screen and (max-width : 800px) {

            .teamMemberWrapOuter {
                padding: 10px;
            }
        }

        @media only screen and (max-width : 767px) {

            .team3 {
                display: initial;
            }

            .teamMemberImages {
                height: auto;
                width: 80%;
            }

            .teamIcon {
                margin: 0 15px;
            }
        }

    </style>
</div>

            <style>
                #teamContainer {
                background: url('/img/disaster-C10FC-3Z36q-rY9OA-eLzrB-VYZIH.jpg');
                background-repeat: no-repeat;
                background-size: cover;
                background-position: center;
                background-attachment: fixed;
            }
            </style>
        </section>
<section id="blog">
            <div class="sectionOverlay" id="blogOverlay" style="background: rgba(0, 0, 0, 0)"></div>
            <div id="outerBlog" class="outerSection noCustomElement">
    <div id="blogContainer" class="sectionContainer noCustomElement">
        <div id="blogContent" class="sectionContent container-fluid noCustomElement">
            <div class="row noCustomElement">
                <div id="blogTop" class="col-lg-4 col-lg-offset-4 col-md-6 col-md-offset-3 col-sm-8 col-sm-offset-2 col-xs-12 noCustomElement">
                    <div id="blogTitleWrap"><h2 id="blogTitle" class="blogTitles" altonclick="null" althref="null">Posts</h2></div>
                    <div id="blogTitleHrWrap"><hr id="blogTitleHr"></div>
                </div>
            </div>
            <div id="noPostBlog" class="row noCustomElement" style="display: none;">
                <div id="noPostBlogTitleWrap" class="col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">
                    <h2 id="noPostBlogTitle" altonclick="null" althref="null">There is no content here yet, but check back soon!</h2>
                </div>
            </div>
            <div class="row noCustomElement">
                <div class="col-lg-10 col-lg-offset-1 col-sm-12 col-sm-offset-0 col-xs-12 noCustomElement">
                    <div id="blogRowContainer" class="noCustomElement">
                        <!-- blogTemplate start --><div class="blog3 row"></div><!-- blogTemplate end -->
                    </div>
                </div>
            </div>
        </div>
    </div>
    <style>
        #blog {
            color: black;
            word-break: break-word;
        }

        #blog .blogImageBg {
            color: white;
        }

        #blogContent {
            text-align: center;
        }

        #noPostBlogTitle {
            font-size: 32px;
            margin-top: 80px;
            letter-spacing: .02em;
        }

        #blogTitle {
            font-size: 50px;
        }

        #blog .blogImageBg #noPostBlogTitle,
        #blog .blogImageBg #blogTitle {
            color: white;
        }

        #blogTitleHr {
            border: 3px solid rgb(255,159,78);
            width: 30%;
        }

        #blog .blogImageBg #blogTitleHr {
            border-color: white;
        }

        .posts3 {
            display: flex;
        }

        .postOuter {
            margin-top: 30px;
        }

        .postInner {
            background-color: white;
            padding: 40px 10px;
            box-shadow: 0 0 3px 0 rgb(255,159,78);
            border-radius: 3px;
        }

        #blog .blogImageBg .postInner {
            box-shadow: 0 0 3px 0 white;
        }

        .blogImages {
            width: 220px;
            height: 280px;
            object-fit: cover;
        }

        #blogHr {
            border: 2px solid rgb(255,159,78);
            width: 50%;
        }  

        .postTitle {
            color: black;
            font-size: 20px;
        }

        .blogButtonWrap {
            margin-top: 15px;
        }

        .blogButton {
            color: white;
            padding: 5px;
            border: 2px solid rgb(255,159,78);
            background-color: rgb(255,159,78);
            text-decoration: none;
            border-radius: 2px;
            cursor: pointer;
            transition: 0.3s;
            display: list-item;
            list-style-type: none;
        }

        .blogButton:focus {
            color: white;
        }

        .blogButton:hover {
            color: black;
            background-color: white;
            border: 2px solid rgb(255,159,78);
            text-decoration: none;
        }

        /* * * * * * * * */

        #blog .customTitle {
            font-size: 40px;
            display: block;
        }

        #blog #noPostBlogTitleWrap .customTitle {
            font-size: 32px;
        }

        #blog .customParagraph {
            font-size: 18px;
            display: block;
        }

        #blog .customLink {
            color: black;
            font-size: 18px;
            display: block;
            width: 100%;
        }

        #blog .blogImageBg .customLink {
            color: white;
        }

        #blog .customLink:hover {
            opacity: 0.6;
            text-decoration: none;
        }

        #blog .customIcon {
            font-size: 36px;
        }

        #blog .customTitle,
        #blog .customParagraph,
        #blog .customLink,
        #blog .customIcon,
        #blog .customButton,
        #blog .customImage,
        #blog .customEmbed {
            margin: 10px 0;
        }

        #blog #blogTitleWrap .customTitle,
        #blog #blogTitleWrap .customParagraph,
        #blog #blogTitleWrap .customLink,
        #blog #blogTitleWrap .customIcon,
        #blog #blogTitleHrWrap .customTitle,
        #blog #blogTitleHrWrap .customParagraph,
        #blog #blogTitleHrWrap .customLink,
        #blog #blogTitleHrWrap .customIcon,
        #blog #noPostBlogTitleWrap .customTitle,
        #blog #noPostBlogTitleWrap .customParagraph,
        #blog #noPostBlogTitleWrap .customLink,
        #blog #noPostBlogTitleWrap .customIcon {
            color: rgb(255,159,78);
        }
        
        #blog .blogImageBg #blogTitleWrap .customTitle,
        #blog .blogImageBg #blogTitleWrap .customParagraph,
        #blog .blogImageBg #blogTitleWrap .customLink,
        #blog .blogImageBg #blogTitleWrap .customIcon,
        #blog .blogImageBg #blogTitleHrWrap .customTitle,
        #blog .blogImageBg #blogTitleHrWrap .customParagraph,
        #blog .blogImageBg #blogTitleHrWrap .customLink,
        #blog .blogImageBg #blogTitleHrWrap .customIcon,
        #blog .blogImageBg #noPostBlogTitleWrap .customTitle,
        #blog .blogImageBg #noPostBlogTitleWrap .customParagraph,
        #blog .blogImageBg #noPostBlogTitleWrap .customLink,
        #blog .blogImageBg #noPostBlogTitleWrap .customIcon {
            color: white;
        }

        #blog #blogTitleWrap .customIcon,
        #blog #blogTitleWrap .customButton,
        #blog #blogTitleWrap .customImage,
        #blog #blogTitleHrWrap .customIcon,
        #blog #blogTitleHrWrap .customButton,
        #blog #blogTitleHrWrap .customImage {
            margin: 0;
        }

        @media only screen and (max-width : 800px) {

            .postTitle {
                font-size: 18px;
            }
        }

        @media only screen and (max-width : 767px) {

            #noPostBlogTitle {
                font-size: 25px;
            }

            .posts3 {
                display: initial;
                margin: 0;
            }

            .postOuter {
                margin-left: 0;
                margin-right: 0;
            }
        }
    </style>
</div>
            <style>
                #blogContainer {
                background: rgb(255,255,255);
            }
            </style>
            <script>
                // script start
                $(document).ready(function() {
                    setTimeout(function() {
                        checkBlogStatus();
                    }, 1000);
                });
                
                var checkBlogStatus = function() {
                    if (document.getElementsByClassName('blogPost').length === 0 || (document.getElementsByClassName('blogPost').length === 1 && document.getElementsByClassName('blogPost')[0].innerHTML.trim() === '')) {
                        document.getElementById('noPostBlog').style.display = '';
                    }
                }
                // script end
            </script>
        </section>
<section id="contact">
            <div class="sectionOverlay" id="contactOverlay" style="background: rgba(0 ,0, 0, 0.5)"></div>
            <div id="outerContact" class="outerSection noCustomElement">
    <div id="contactContainer" class="sectionContainer contactImageBg noCustomElement" style="margin-bottom: 0px;">
        <div id="contactContent" class="sectionContent container-fluid noCustomElement">
            <div class="row noCustomElement">
                <div id="contactMainRowWrap" class="col-lg-8 col-lg-offset-2 col-sm-10 col-sm-offset-1 col-xs-12 noCustomElement">
                    <div id="contactMainRow" class="row noCustomElement">
                        <div class="outerGrid col-sm-6 col-xs-12 noCustomElement">
                            <div class="innerGridTable noCustomElement">
                                <div class="innerTableContent noCustomElement">
                                    <div class="row noCustomElement">
                                        <div id="contactTitleWrap" class="col-sm-12 col-xs-12 noCustomElement">
                                            <div id="contactTitleWrap"><h2 id="contactTitle" class="contactTitles" altonclick="null" althref="null">Reach Out</h2></div>
                                            <div id="contactSubtitleWrap"><h4 id="contactSubtitle" class="contactSubtitles" altonclick="null" althref="null"></h4></div>
                                        </div>
                                    </div>
                                    <form id="contactForm"> 
                                        <div id="contactRowContainer" class="noCustomElement">
                                            <!-- inputTemplate start --><div class="input1 row">
                                                <div class="contactInputWrap contactTemplate form-group col-sm-10 col-xs-12 noCustomElement">
                                                    <input id="contactName" type="text" class="contactFormInput form-control" placeholder="Name">
                                                </div>
                                                </div><div class="input1 row">
                                                <div class="contactInputWrap contactTemplate form-group col-sm-10 col-xs-12 noCustomElement">
                                                    <input id="contactEmail" type="text" class="contactFormInput form-control" placeholder="Email">
                                                </div>
                                                </div><div class="input1 row">
                                                <div class="contactInputWrap contactTemplate form-group col-sm-10 col-xs-12 noCustomElement">
                                                    <input id="contactSubject" type="text" class="contactFormInput form-control" placeholder="Subject">
                                                </div>
                                                </div><!-- inputTemplate end -->
                                        </div>
                                        <div class="form-row row noCustomElement">
                                            <div class="contactInputWrap form-group col-sm-10 col-xs-12 noCustomElement">
                                                <textarea placeholder="Message" id="contactMessage" class="contactFormInput form-control"></textarea>
                                            </div>
                                        </div>
                                        <div class="form-row row noCustomElement">
                                            <div class="contactInputWrap form-group col-sm-10 col-xs-12 noCustomElement">
                                                <div id="contactButtons"><a class="contactButton" althref="null" onclick="submitContactForm()">Submit</a></div>
                                            </div>
                                        </div>
                                    </form>
                                </div>
                            </div>
                        </div>
                        <div class="outerGrid col-sm-5 col-sm-offset-1 col-xs-12 noCustomElement">
                            <div class="innerGridTable noCustomElement">
                                <div class="innerTableContent noCustomElement">
                                    <div id="contactEmailWrap">
                                        <p class="contactInfoTextBig" altonclick="null" althref="null">If you have any questions,</p>
                                        <p class="contactInfoTextBig contactInfoInline" altonclick="null" althref="null">Email us at</p>
                                        <a id="contactEmailInner" class="contactInfoTextBig contactInfoInline" altonclick="null" href="mailto:email@example.com">email@example.com</a>
                                    </div>
                                    <div id="contactAddressOuter">
                                        <p class="contactInfoTextBig" altonclick="null" althref="null">Or come by and see us!</p>
                                        <div id="contactAddressWrap" class="noCustomElement"><p id="contactAddress1" class="contactInfoTextBig" altonclick="null" althref="null">123 First St.</p></div>
                                        <div id="‘contactCityWrap’" class="noCustomElement"><p id="contactAddress2" class="contactInfoTextBig" altonclick="null" althref="null">Austin, TX 78700</p></div>
                                    </div>

                                    <div id="contactHoursContainer">
                                        <h4 id="contactHoursTitle" altonclick="null" althref="null">HOURS</h4>
                                        <p id="contactHours1" class="contactInfoHours contactInfoText" altonclick="null" althref="null">Monday: 8am - 8pm</p>
                                        <p id="contactHours2" class="contactInfoHours contactInfoText" altonclick="null" althref="null">Tuesday: CLOSED</p>
                                        <p id="contactHours3" class="contactInfoHours contactInfoText" altonclick="null" althref="null">Wednesday: 8am - 8pm</p>
                                        <p id="contactHours4" class="contactInfoHours contactInfoText" altonclick="null" althref="null">Thursday: 8am - 8pm</p>
                                        <p id="contactHours5" class="contactInfoHours contactInfoText" altonclick="null" althref="null">Friday: 8am - 8pm</p>
                                        <p id="contactHours6" class="contactInfoHours contactInfoText" altonclick="null" althref="null">Saturday: 10am - 6pm</p>
                                        <p id="contactHours7" class="contactInfoHours contactInfoText" altonclick="null" althref="null">Sunday: 10am - 4pm</p>
                                    </div>
                                    <p altonclick="null" althref="null"></p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <style>
        #contact {
            color: black;
        }

        #contact .contactImageBg {
            color: white;
        }

        #contactContent {
            word-wrap: break-word;
        }

        #contactTitle {
            text-transform: uppercase;
            letter-spacing: .03em;
            font-size: 40px;
            margin: 0 0 10px;
        }

        #contactSubtitle {
            font-size: 18px;
            margin-bottom: 40px;
        }

        #contactMainRow,
        #contactInfoRow {
            display: flex;
        }

        #contactRowContainer {
            margin-top: 30px;
        }

        .contactFormInput {
            border: 1px solid black;
            border-radius: 2px;
        }

        #contact .contactImageBg .contactFormInput {
            border-color: white;
        }

        #contactMessage {
            height: 80px;
            resize: none;
        }

        .contactFormInput::placeholder {
            color: black;
            letter-spacing: .04em;
        }

        .contactButton {
            color: white;
            padding: 10px 42px;
            background-color: rgba(255,159,78,0.7);
            border-radius: 1px;
            text-decoration: none;
            text-transform: uppercase;
            margin-top: 20px;
            cursor: pointer;
            transition: 0.5s;
            display: inline-block;
        }

        .contactButton:focus {
            color: white;
        }

        #contact .contactImageBg .contactButton,
        #contact .contactImageBg .contactButton:focus {
            color: black;
            background-color: rgba(255,255,255,0.7);
        }

        .contactButton:hover {
            color: white;
            background-color: rgb(255,159,78);
            text-decoration: none;
        }

        #contact .contactImageBg .contactButton:hover {
            color: black;
            background-color: white;
        }

        #contactEmailWrap {
            margin-bottom: 25px;
        }

        .contactInfoTextBig {
            font-size: 18px;
            margin: 0;
        }

        #contactEmailInner {
            cursor: pointer;
            text-decoration: none;
            color: rgb(255,159,78);
        }

        #contact .contactImageBg #contactEmailInner {
            color: white;
        }

        .contactInfoInline {
            display: inline;
        }

        .contactInfoText {
            font-size: 15px;
            margin: 1px 0;
        }

        #contactAddressOuter {
            margin-bottom: 25px;
        }

        .contactInfoHours {
            display: block;
        }
       
       /* * * * * * * * */

        #contact .customTitle {
            font-size: 40px;
            display: block;
        }

        #contact .customParagraph {
            font-size: 18px;
            display: block;
        }

        #contact .customLink {
            color: black;
            font-size: 18px;
            display: block;
            width: 100%;
        }

        #contact .contactImageBg .customLink {
            color: white;
        }

        #contact .customLink:hover {
            opacity: 0.6;
            text-decoration: none;
        }

        #contact .customIcon {
            font-size: 36px;
        }

        #contact .customTitle,
        #contact .customParagraph,
        #contact .customLink,
        #contact .customIcon,
        #contact .customButton,
        #contact .customImage,
        #contact .customEmbed {
            margin: 10px 0;
        }

        #contact #contactTitleWrap .customIcon,
        #contact #contactTitleWrap .customButton,
        #contact #contactTitleWrap .customImage, 
        #contact #contactSubtitleWrap .customIcon,
        #contact #contactSubtitleWrap .customButton,
        #contact #contactSubtitleWrap .customImage {
            margin: 0 0 10px;
        }

        @media only screen and (max-width : 767px) {

            #contactTitle {
                font-size: 32px;
            }

            #contactMainRow {
                display: initial;
            }

            .contactInfoText {
                letter-spacing: 0;
            }

            #contactButtons {
                margin-bottom: 30px;
            }
        }
    </style>
</div>
            <style>
                #contactContainer {
                background: url('/img/disaster-bKHbg-uONek-t3exP-DStWP-2UsJ5.jpg');
                background-repeat: no-repeat;
                background-size: cover;
                background-position: center;
                background-attachment: fixed;
            }
            </style>
        </section>
<div id="footer">
    <h4 class="pageFooter" id="footerFour" altonclick="null" althref="null">© Ready To Respond</h4>
</div>

<div id="newsletterOuter" delay="20000" enabled="false" style="display:none" class="noCustomElement">
    <div id="newsOverlaySection" class="noCustomElement">
        <div class="row innerTableContent noCustomElement">
            <div id="newsletterBorder" class="col-md-6 col-md-offset-3 col-sm-10 col-sm-offset-1 col-xs-12 noCustomElement">
                <button id="closeNewsletterButton" class="newsletterClose" althref="null" onclick="document.getElementById(&quot;newsletterOuter&quot;).style.display = &quot;none&quot;">
                    <i class="newsletterCloseIcon fa fa-times" aria-hidden="true" altonclick="null" althref="null"></i>
                </button>
                <div id="newsletterTitleWrap"><h4 id="newsletterTitle" class="newsletterTitles" altonclick="null" althref="null">Be the first to know about special offers and the latest updates.</h4></div>
                <hr id="newsletterHr">
                <div id="newsletterSubtitle1Wrap"><h4 id="newsletterSubtitle1" class="newsletterSubtitles1" altonclick="null" althref="null">20% OFF</h4></div>
                <div id="newsletterSubtitle2Wrap"><h4 id="newsletterSubtitle2" class="newsletterSubtitles2" altonclick="null" althref="null">YOUR PURCHASE NOW</h4></div>
                <form id="newsletterForm"> 
                    <div id="newsletterRowContainer"> 
                        <input id="newsletterInput" type="email" class="form-control" placeholder="Enter Email Address">
                        <a id="newsletterButton" class="newsletterButton" althref="null" onclick="submitNewsletter()">SIGN UP FOR EMAILS</a>
                    </div>
                </form>
                <div id="newsletterSubtitle3Wrap"><h4 id="newsletterSubtitle3" class="newsletterSubtitles3" altonclick="null" althref="null">Subscribers will be eligible to receive future promotional emails</h4></div>
            </div>
        </div>
    </div>
    <style>

        #newsLetterOuter {
            word-break: break-word;
        }

        #closeNewsletterButton {
            position: absolute;
            top: 15px;
            right: 15px;
            border: none;
            font-size: 25px;
            background: transparent;
            cursor: pointer;
            color: rgb(0,0,0,0.5);
            transition: 0.4s;
        }

        #closeNewsletterButton:hover {
            color: black;
        } 

        #newsOverlaySection {
            display: table;
            position: fixed;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.7);
            text-align: center;
        }

        #newsletterBorder {
            border: 2px solid rgb(0,0,0,0.5);
            background-color: white;
            padding: 10px 0;
        }

        #newsletterTop {
            margin: 60px 0 0;
        }

        #newsletterTitle {
            font-size: 28px;
            color: rgb(0,0,0,0.5);
            width: 60%;
            margin: 20px auto 0;
            font-weight: normal;
        }

        #newsletterHr {
            border: 1px solid rgb(0,0,0,0.5);
            width: 50%;
            margin: 10px auto;
        }

        #newsletterSubtitle1 {
            font-size: 60px;
            letter-spacing: .1em;
            margin: 0;
        }
        
        #newsletterSubtitle2 {
            color: rgb(0,0,0,0.5);
            font-size: 25px;
            letter-spacing: .1em;
            margin: 0;
        }

        #newsletterInput {
            font-size: 12px;
            width: 70%;
            height: 40px;
            margin: 20px auto 0;
            border: 1px solid rgb(0,0,0,0.5);
            border-radius: 2px;
            color: rgb(0,0,0,0.5);
            text-align: center;
        }

        #newsletterInput::placeholder {
            color: rgb(0,0,0,0.5);
        }
        
        #newsletterInput:focus {
            box-shadow: 0 0 3px rgb(0,0,0,0.5);
            border-color: rgb(0,0,0,0.5);
        }

        #newsletterButton {
            color: white;
            font-size: 18px;
            font-weight: bold;
            padding: 6px 32px;
            margin: 20px 0; 
            text-decoration: none;
            background: rgb(255,159,78);
            border: 1px solid rgb(255,159,78);
            border-radius: 2px;
            cursor: pointer;
            transition: 0.5s;
            display: inline-block;
        }

        #newsletterButton:focus {
            color: white;
        }

        #newsletterButton:hover {
            color: rgb(255,159,78);
            background: white;
        }

        #newsletterSubtitle3 {
            font-size: 12px;
            color: rgb(0,0,0,0.5);
            margin-bottom: 20px;
        }

        /* * * * * * * * */

        #newsletterOuter .customTitle {
            font-size: 40px;
            display: block;
        }

        #newsletterOuter .customParagraph {
            font-size: 18px;
            display: block;
        }

        #newsletterOuter .customLink {
            color: black;
            font-size: 18px;
            display: block;
            width: 100%;
        }

        #newsletterOuter .customLink:hover {
            opacity: 0.6;
            text-decoration: none;
        }

        #newsletterOuter .customIcon {
            font-size: 28px;
        }

        #newsletterOuter .customTitle,
        #newsletterOuter .customParagraph,
        #newsletterOuter .customLink,
        #newsletterOuter .customIcon,
        #newsletterOuter .customButton,
        #newsletterOuter .customImage,
        #newsletterOuter .customEmbed {
            margin: 10px 0;
        }
        
        @media only screen and (max-width : 767px) {

            #newsletterTitle {
                width: 70%;
            }

            #newsletterInput {
                width: 90%;
            }
        }
    </style>
</div>

<script id="generalJS">
    $(document).ready(function() {
        loadLeiaAd();
        initializeSmoothScroll();
        if (window.self !== window.top) {
            if (document.getElementById('menuOverlaySection')) {
                document.getElementById('menuOverlaySection').style.height = window.parent.innerHeight.toString() + 'px';
            }
            
            if (document.getElementById('menuBorder')) {
                document.getElementById('menuBorder').style.maxHeight = window.parent.innerHeight.toString() + 'px';
            }
            
            if (window.orientation !== undefined && document.getElementById('headerBackgroundVideo')) {
                updateBgimageSizes();
                window.addEventListener('orientationchange', function() {
                    updateBgimageSizes();
                });
            }
        } else if (document.getElementById('newsletterOuter') && document.getElementById('newsletterOuter').getAttribute('enabled') === 'true') {
            var time = parseInt(document.getElementById('newsletterOuter').getAttribute('delay'));
            if (time > 0) {
                setTimeout(function() {
                    $('#newsletterOuter').css('opacity', '0');
                    $('#newsletterOuter').css('display', '');
                    $('#newsletterOuter').animate({opacity: '1'}, 1000);
                }, time);
            }
        }
    });
    
    var initializeSmoothScroll = function() {
        $(document).on('click', 'a[href^="#"]', function (event) {
            event.preventDefault();

            $('html, body').animate({
                scrollTop: $($.attr(this, 'href')).offset().top
            }, 1000);
        });
    }
    
    var updateBgimageSizes = function() {
        document.getElementById('headerBackgroundVideo').style.height = document.getElementById('headerContainer').offsetHeight.toString() + 'px';
    }

    var loadLeiaAd = function() {
        /*$.ajax({
            url: 'https://heyleia.com/php/getAdStatus.php',
            type: 'GET',
            data: {'domain': window.location.hostname},
            success: function(type) {
                if (type === 'ad') {
                    addLeiaAd();
                }
            },
            error: function(err) {
                console.log(err);
            }
        });*/
    }
    
    var meetingToken;
    var submitVideoChat = function() {
        var name = document.getElementById('videoName').value;
        var email = document.getElementById('videoEmail').value;

        document.getElementById('launchChatButton').disabled = true;

        var spinner = document.createElement('div');
        var outer = document.createElement('div');

        outer.id = 'spinnerLoading';
        spinner.className = 'spinnerLoading';
        outer.style.background = 'rgba(0,0,0,0.7)';
        outer.style.borderRadius = '20px';
        outer.style.position = 'fixed';
        outer.style.left = ((window.innerWidth - 205) / 2).toString() + 'px';
        outer.style.width = '205px';
        outer.style.top = '30%';
        outer.style.height = '205px';
        outer.style.zIndex = '10000';
        spinner.style.marginLeft = '42.5px';
        spinner.style.marginTop = '42.5px';
        outer.appendChild(spinner);
        document.body.appendChild(outer);

        if (!addedSpinner) {
            addedSpinner = true;
            addSpinnerStyle();
        }

        $.ajax({
            url: 'https://heyleia.com/php/scheduleMeeting.php',
            type: 'POST',
            data: {name: name, email: email, partner: ''},
            success: function(data) {
                meetingToken = data;
                document.getElementById('launchChatButton').disabled = false;
                swal('Meeting Ready', 'Click the "Launch Meeting" button to start your video chat.', 'success');
                document.getElementById('spinnerLoading').parentElement.removeChild(document.getElementById('spinnerLoading'));
            },
            error: function(err) {
                console.log(err);
                swal('Uh Oh', 'There was an error scheduling your live chat. Please try again in a few minutes!', 'error');
                document.getElementById('spinnerLoading').parentElement.removeChild(document.getElementById('spinnerLoading'));
            }
        })
    }

    var launchVideoChat = function() {
        window.open('https://leia-gucu3ir82nuyqjjicjmbg6uuc.braidio.com/meetings/' + meetingToken, '_blank');
    }

    var showVideo = function() {
        document.getElementById('videoChatOverlay').style.display = '';
    }

    var closeVideo = function() {
        document.getElementById('videoChatOverlay').style.display = 'none';
    }
    
    var shownSchedule = false;
    var showSchedule = function() {
        document.getElementById('schedulingOverlay').style.display = '';
        
        if (shownSchedule) {
            var frame = document.getElementById('schedulingOverlay').getElementsByTagName('iframe')[0];
            var src = frame.getAttribute('src').split('&v')[0];
            frame.setAttribute('src', src + '&v=' + new Date().getTime());
        }
        
        shownSchedule = true;
    }
    
    var closeSchedule = function() {
        document.getElementById('schedulingOverlay').style.display = 'none';
    }

    var addLeiaAd = function() {
        var img = document.createElement('img');
        var tag = document.createElement('a');
        img.id = 'leiaAdLogo';
        tag.id = 'leiaAdLogoA';
        img.setAttribute('src', 'https://heyleia.com/images/poweredBy.png');

        if (window.self === window.top && window.location.search !== '?site=live') {
            tag.setAttribute('href', 'https://heyleia.com/direct?src=site');
            tag.setAttribute('target', '_blank');
        } else {
            img.onclick = function() {
                if (window.location.search === '?site=live') {
                    swal('Remove Leia Ad', 'You can remove this ad by upgrading to Leia Pro! This includes hosting and everything else you need for your site.', 'info');
                } else {
                    swal({
                        title: 'Remove Leia Ad',
                        text: 'You can remove this ad by upgrading to Leia Pro! This includes hosting and everything else you need for your site.',
                        type: 'info',
                        icon: 'info',
                        closeOnClickOutside: true,
                        showCancelButton: true,
                        buttons: {
                            cancel: 'Not Now',
                            submit: {
                                text: 'Learn More',
                                value: 'learn',
                            }
                        },
                        closeOnConfirm: true
                    }).then(function(isConfirm) {
                        if (isConfirm == 'learn') {
                            window.open('https://heyleia.com/upgrade', '_blank');
                        } 
                    }); 
                }
            }
        }

        tag.appendChild(img);
        document.body.appendChild(tag);
    }
    
    var mainColor = 'rgb(255,159,78)';
    
    var applyFancyTop = function(top) {
        if (document.getElementById('fancyStyle')) {
            document.getElementById('fancyStyle').parentElement.removeChild(document.getElementById('fancyStyle'));
        }
        
        var style = document.createElement('style');
        style.id = 'fancyStyle';
        var txt = document.createTextNode('#fancybox-wrap {top: ' + top.toString() + 'px !important;}');
        style.appendChild(txt);
        document.body.appendChild(style);
    }
    
    var addedSpinner = false;
    var submitContactForm = function() {
        swal("Are you sure you want to submit this message?", {
            buttons: {
                no: {
                    text: "Cancel",
                    value: "Cancel",
                    className: 'swal-button swal-button--cancel',
                    closeModal: false,
                },
                yes: {
                    text: "Submit",
                    value: "ok"
                },
            },
            title: 'Confirmation',
            type: 'info',
            icon: 'info'
        }).then((value) => {
            if (value === 'Cancel') {
                swal.close();
            } else {
                var spinner = document.createElement('div');
                var outer = document.createElement('div');

                outer.id = 'spinnerLoading';
                spinner.className = 'spinnerLoading';
                outer.style.background = 'rgba(0,0,0,0.7)';
                outer.style.borderRadius = '20px';
                outer.style.position = 'fixed';
                outer.style.left = ((window.innerWidth - 205) / 2).toString() + 'px';
                outer.style.width = '205px';
                outer.style.top = '30%';
                outer.style.height = '205px';
                outer.style.zIndex = '10000';
                spinner.style.marginLeft = '42.5px';
                spinner.style.marginTop = '42.5px';
                outer.appendChild(spinner);
                document.body.appendChild(outer);

                if (!addedSpinner) {
                    addedSpinner = true;
                    addSpinnerStyle();
                }

                var dataObj = {}
                if (document.getElementById('contactName')) {
                    dataObj['name'] = document.getElementById('contactName').value;
                }
                if (document.getElementById('contactEmail')) {
                    dataObj['email'] = document.getElementById('contactEmail').value;
                }
                if (document.getElementById('contactPhone')) {
                    dataObj['phone'] = document.getElementById('contactPhone').value;
                }
                if (document.getElementById('contactCompany')) {
                    dataObj['company'] = document.getElementById('contactCompany').value;
                }
                if (document.getElementById('contactStreet')) {
                    dataObj['street'] = document.getElementById('contactStreet').value;
                }
                if (document.getElementById('contactCity')) {
                    dataObj['city'] = document.getElementById('contactCity').value;
                }
                if (document.getElementById('contactState')) {
                    dataObj['state'] = document.getElementById('contactState').value;
                }
                if (document.getElementById('contactSubject')) {
                    dataObj['subject'] = document.getElementById('contactSubject').value;
                }
                if (document.getElementById('contactMessage')) {
                    dataObj['message'] = document.getElementById('contactMessage').value;
                }

                $.ajax({
                    url: 'https://heyleia.com/php/clientContact.php',
                    data: dataObj,
                    type: 'POST',
                    success: function(data) {
                        document.getElementById('spinnerLoading').parentElement.removeChild(document.getElementById('spinnerLoading'));
                        if (data === 'success') {
                            swal("Success", "You have successfully submitted your message! We will contact you at our earliest convenience.", "success");
                            document.body.className = '';
                        } else {
                            swal("Uh Oh!", data, "error");
                            document.body.className = '';
                        }
                    },
                    error: function(err) {
                        console.log(err);
                        document.getElementById('spinnerLoading').parentElement.removeChild(document.getElementById('spinnerLoading'));
                        swal("Uh Oh!", "There was a problem. Please try again later.", "error");
                        document.body.className = '';
                    }
                });
            }
        });
    }
    
    var submitNewsletter = function() {
        var spinner = document.createElement('div');
        var outer = document.createElement('div');

        outer.id = 'spinnerLoading';
        spinner.className = 'spinnerLoading';
        outer.style.background = 'rgba(0,0,0,0.7)';
        outer.style.borderRadius = '20px';
        outer.style.position = 'fixed';
        outer.style.left = ((window.innerWidth - 205) / 2).toString() + 'px';
        outer.style.width = '205px';
        outer.style.top = '30%';
        outer.style.height = '205px';
        outer.style.zIndex = '10000';
        spinner.style.marginLeft = '42.5px';
        spinner.style.marginTop = '42.5px';
        outer.appendChild(spinner);
        document.body.appendChild(outer);

        if (!addedSpinner) {
            addedSpinner = true;
            addSpinnerStyle();
        }

        var dataObj = {
            email: document.getElementById('newsletterInput').value
        }
        
        $.ajax({
            url: 'https://heyleia.com/php/clientNewsletter.php',
            data: dataObj,
            type: 'POST',
            success: function(data) {
                document.getElementById('spinnerLoading').parentElement.removeChild(document.getElementById('spinnerLoading'));
                if (data === 'success') {
                    swal("Success", "You have successfully subscribed to our mailing list!", "success").then(function() {
                        document.getElementById('newsletterOuter').style.display = 'none';
                    });
                    
                    document.body.className = '';
                } else {
                    swal("Uh Oh!", data, "error");
                    document.body.className = '';
                }
            },
            error: function(err) {
                console.log(err);
                document.getElementById('spinnerLoading').parentElement.removeChild(document.getElementById('spinnerLoading'));
                swal("Uh Oh!", "There was a problem. Please try again later.", "error");
                document.body.className = '';
            }
        });
    }
    
    var addSpinnerStyle = function() {
        var style = document.createElement('style');
        style.appendChild(document.createTextNode(".spinnerLoading {border: 16px solid #f3f3f3; /* Light grey */border-top: 16px solid #3498db; /* Blue */border-radius: 50%;width: 120px;height: 120px;animation: spin 2s linear infinite;}@keyframes spin {0% { transform: rotate(0deg); }100% { transform: rotate(360deg); }}"));
        document.body.appendChild(style);
    };
</script>
</body></html>

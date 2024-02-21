<!DOCTYPE html>
<head>

<!--

    theme 64  by  pirateskinned
    
    please don't:  edit & repost / claim as your own
    please don't:  delete or move the credit
    please don't:  steal bits of coding
    
    ------
    
    image wrapping inspired by iniziare.tumblr.com
    tumblr controls styling by cyantists.tumblr.com
    icon font by saturnicons.suiomi.com
    
    ------
    
    to edit the slide out:
    
    ctrl+f or cmd+f and search for:
    'EDIT SLIDEOUT'
    follow the instructions there
    
    
-->

<title>{Title}</title>

<link rel="shortcut icon" href="{Favicon}">
<link rel="alternate" type="application/rss+xml" href="{RSS}">
{block:Description}<meta name="description" content="{MetaDescription}" />{/block:Description}

<!-- meta tags -->

<meta name="image:background" content=""/>
<meta name="image:social icon" content=""/>
<meta name="image:sidebar" content=""/>
<meta name="image:right icon" content=""/>
<meta name="image:slide out" content=""/>

<meta name="color:background" content="#f5f5f5"/>
<meta name="color:container" content="#f8f8f8"/>
<meta name="color:posts" content="#ffffff"/>
<meta name="color:border" content="#eeeeee"/>
<meta name="color:text" content="#4f4e4e"/>
<meta name="color:link" content="#cad8c1"/>
<meta name="color:accent one" content="#dac7ae"/>
<meta name="color:accent two" content="#b4c390"/>

<meta name="if:background pattern" content="1"/>
<meta name="if:image wrap" content="1"/>
<meta name="if:500px posts" content="0"/>

<meta name="select:fontsize" content="11px" title="11px">
<meta name="select:fontsize" content="12px" title="12px">
<meta name="select:fontsize" content="13px" title="13px">
<meta name="select:fontsize" content="14px" title="14px">
<meta name="select:fontsize" content="15px" title="15px">

<meta name="text:sidebar name" content="name">
<meta name="text:sidebar following" content="123">
<meta name="text:sidebar followers" content="456">
<meta name="text:sidebar posts" content="789">

<meta name="text:tag 1" content="tag">
<meta name="text:tag 2" content="tag">
<meta name="text:tag 3" content="tag">
<meta name="text:tag 4" content="tag">
<meta name="text:tag 5" content="tag">
<meta name="text:tag 6" content="tag">

<!-- scripts -->

<link href="https://static.tumblr.com/qudkd6d/OcDnl99gb/style.css" rel="stylesheet" type="text/css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>

<!-- fonts -->

<link href="https://fonts.googleapis.com/css2?family=Karla:wght@200;300;400;700&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600&display=swap" rel="stylesheet">

<!-- icon font -- https://saturnicons.suiomi.com/ -->

<link href="//solrainha.github.io/saturnicons/saturnicons.css" rel="stylesheet">

<!-- tooltips -->

<script src="https://static.tumblr.com/iuw14ew/VSQma1786/jquery.style-my-tooltips.js"></script>

<script>
    (function($){
        $(document).ready(function(){
            $("a[title], div[title], span[title]").style_my_tooltips({
                tip_follows_cursor:true,
                tip_delay_time:30,
                tip_fade_speed:300,
                attribute:"title"
            });
        });
    })(jQuery);
</script>

<!-- photosets -->

<script src="https://static.tumblr.com/qudkd6d/Az6nkemqr/pxuphotoset.min.js"></script>

<script>
    $(document).ready(function(){
       $('.photo-slideshow').pxuPhotoset({
           lightbox: true,
           rounded: false,
           gutter: '1px',
           borderRadius: '0px',
           photoset: '.photo-slideshow',
           photoWrap: '.photo-data',
           photo: '.pxu-photo'
       });
    });
    
</script>

<!-- time ago script -->

<script src="https://static.tumblr.com/i5s2zks/9Acok8oo2/bct-timeago.min.js"></script>
<script>
$(document).ready(function() {
    $(".permalink a.time-ago").timeAgo({
        time: "short", // can be "letter" "short" or "word"
        spaces: true, // adds spaces between words and numbers
        words: false, // turns numbers to words
        prefix: "", // adds a prefix to the outputted string. could be "~" or "about"
        suffix: "ago", // adds a suffix to the outputted string. could be "ago"
    });
});
</script>

<!-- popups -->

<script>
    $(document).ready(function(){
        $('#trigger').click(function(){
            {block:ifnot500pxposts}
            $('.inner-container').css("left", "-1100px");
            $('.topbar').css("left", "1110px");
            {/block:ifnot500pxposts}
            {block:if500pxposts}
            $('.inner-container').css("left", "-1200px");
            $('.topbar').css("left", "1210px");
            {/block:if500pxposts}
        });
        
        $('.pop-close').click(function(){
            $('.inner-container').css("left", "0px");
            $('.topbar').css("left", "10px");
        })
    })
</script>


<style type="text/css">

/* ---  tumblr controls styling by cyantists
        http://cyantists.tumblr.com/tumblr_controls/hover --- */

iframe.tmblr-iframe {
    z-index:99999999999999!important;
    top:-2px!important;
    right:0!important;
    opacity:0;
    padding-right:38px;
    /* delete invert(1) from here */
        filter:invert(1) contrast(150%);
        -webkit-filter:invert(1) contrast(150%);
        -o-filter:invert(1) contrast(150%);
        -moz-filter:invert(1) contrast(150%);
        -ms-filter:invert(1) contrast(150%);
    /* to here if your blog has a dark background */
    transform:scale(0.65);
    transform-origin:100% 0;
    -webkit-transform:scale(0.65);
    -webkit-transform-origin:100% 0;
    -o-transform:scale(0.65);
    -o-transform-origin:100% 0;
    -moz-transform:scale(0.65);
    -moz-transform-origin:100% 0;
    -ms-transform:scale(0.65);
    -ms-transform-origin:100% 0;}

iframe.tmblr-iframe:hover {
    opacity:0.6!important;}

.hcontrols {
    position:fixed;
    top:0;
    right:0;
    z-index:999999999;}

.hcontrols svg {
    width:14px;
    height:14px;
    padding:9px;}

.hcontrols svg path {
    fill:#888888;/* change this to change the color of the icon */}

/* --- tooltips & scrollbars --- */

#s-m-t-tooltip {
    position:absolute;
    margin-top: 15px;
    z-index:9999;
    padding:3px 7px;
    background:{color:posts};
    color:{color:text};
    font-size:{select:fontsize};
    border:1px solid {color:border};
    border-radius:40px;
}

::-webkit-scrollbar-thumb {background-color:{color:border};}
::-webkit-scrollbar {background-color:transparent; width:1px; height:1px;}

/* --- basics --- */

body {
    background-color:{color:background};
    background-image:url('{image:background}');
    background-attachment:fixed;
    background-position:center center;
    {block:ifnotbackgroundpattern}
    background-repeat:no-repeat;
    background-size:cover;
    {/block:ifnotbackgroundpattern}
    {block:ifbackgroundpattern}
    background-repeat:repeat;
    background-size:auto;
    {/block:ifbackgroundpattern}
    color:{color:text};
    font-family: 'Karla', sans-serif;
    font-size:{select:fontsize};
    line-height:calc({select:fontsize} + 6px);
    font-weight:300;
    text-align:justify;
    margin:0;
}

a {
    color:{color:text};
    text-decoration:none;
    -moz-transition-duration: 0.5s;
    -o-transition-duration: 0.5s;
    -webkit-transition-duration: 0.5s;
    transition-duration: 0.5s;
}

    a:hover {
        color:{color:text};
        text-decoration:none;
    }
    
p a, .side-info-inner a, li a
{box-shadow:{color:border} 0px -1px 0px inset;}
p a:hover, .side-info-inner a:hover, li a:hover
{box-shadow:{color:link} 0px -12px 0px inset;}

img {
    border:none;
    text-decoration:none;
}

b, strong, bold {
    font-weight:800;
}

u {
    text-decoration:none;
}

    .firstletter, u {
        display:block;
        float:left;
        padding:12px 14px;
        background:{color:posts};
        color:{color:text};
        font-weight:800;
        text-transform:uppercase;
        font-size:calc({select:fontsize} + 4px);
        margin:0px 10px 0px 0px;
        border:1px solid {color:border};
        border-radius:10px;
    }

s, strike {
    text-decoration-color:{color:accent one};
}

small, sub, sup, big {
    font-size:{select:fontsize};
    line-height:calc({select:fontsize} + 6px);
    vertical-align:baseline;
}

blockquote {
    padding:0px 5px 0px 15px;
    border-left:1px solid {color:border};
    margin-left:5px;
    margin-right:0px;
}

    blockquote img {
        max-width:360px;
        height:auto;
    }
    
        blockquote blockquote {
            margin-right:0px;
        }
        
            blockquote blockquote img {
                max-width:350px;
                height:auto;
                margin-top:10px;
            }

pre {
    font-family: 'Poppins', sans-serif;
    font-weight:600;
    font-size:calc({select:fontsize} + 2px);
    text-align:center;
    padding:10px;
    margin:0px;
    border:1px solid {color:border};
    border-radius:40px;
}

    pre i, pre em, pre b, pre strong, pre a {
        color:{color:text};
    }

ul {
    padding-left:15px;
}

    ul li {
        list-style-type:none;
    }
    
        ul li:before {
          content: "— ";
          text-indent: -5px;
        }
        
hr {
    border:none;
    border-bottom:1px solid {color:border};
    width:calc(100% - 150px);
    margin:20px auto 20px auto;
}

/* --- header styles --- */

h1 {
    margin:0px 0px 20px 0px;
    font-family: 'Poppins', sans-serif;
    font-weight:600;
    font-size:calc({select:fontsize} + 8px);
}

h2 {
    font-weight:400;
    text-align:left;
    text-transform:uppercase;
    font-size:calc({select:fontsize} + 2px);
    letter-spacing:1px;
    word-spacing:2px;
}

    h2 b, b h2, h2 i, i h2,
    h2 strong, strong h2, h2 em, em h2 {
        color:{color:text};
    }
    
h3 {
    font-size:calc({select:fontsize} + 4px);
    font-weight:400;
    margin:10px 0px;
}
    
/* --- container --- */

.container {
    position:absolute;
    z-index:600;
    top:calc(50% - 300px);
    {block:ifnot500pxposts}
    width:1100px;
    left:calc(50% - 551px);
    {/block:ifnot500pxposts}
    {block:if500pxposts}
    width:1200px;
    left:calc(50% - 601px);
    {/block:if500pxposts}
    height:600px;
    background-color:{color:container};
    border-radius:10px;
    border:1px solid {color:border};
    overflow:hidden;
}

/* --- inner container --- */

.inner-container {
    position:absolute;
    top:0px;
    left:0px;
    {block:ifnot500pxposts}
    width:2200px;
    {/block:ifnot500pxposts}
    {block:if500pxposts}
    width:2400px;
    {/block:if500pxposts}
    height:600px;
    transition:all 1.5s ease;
}

/* --- topbar --- */

.topbar {
    position:absolute;
    z-index:650;
    top:10px;
    left:10px;
    {block:ifnot500pxposts}
    width:1080px;
    {/block:ifnot500pxposts}
    {block:if500pxposts}
    width:1180px;
    {/block:if500pxposts}
    height:40px;
    border-radius:10px;
    background-color:{color:posts};
    border:1px solid {color:border};
    overflow:hidden;
    box-shadow:0px 0px 5px rgba(0,0,0,0.05);
    transition:all 1.5s ease;
}

.topbar-links {
    position:absolute;
    z-index:450;
    top:0px;
    left:0px;
    width:350px;
    height:40px;
    padding-left:20px;
    background-color:{color:accent two};
    border-right:1px solid {color:border};
    display:flex;
    justify-content:flex-start;
    align-items:center;
}

    .topbar-links a {
        margin:0px 10px;
        width:auto;
        height:40px;
        color:{color:posts};
        font-weight:700;
        font-family:'Poppins', sans-serif;
        letter-spacing:1px;
        display:flex;
        align-items:center;
    }
    
        .topbar-links a:hover {
            box-shadow:inset 0px -5px 0px {color:posts}, inset 0px 5px 0px {color:posts};
        }
        
    .topbar-links:after {
        content:'';
        position:absolute;
        top:0px;
        {block:ifnot500pxposts}
        right:-710px;
        {/block:ifnot500pxposts}
        {block:if500pxposts}
        right:-810px;
        {/block:if500pxposts}
        width:200px;
        height:40px;
        background-color:{color:accent one};
        border-left:1px solid {color:border};
    }

/* --- sidebar --- */

.sidebar {
    position:absolute;
    z-index:500;
    top:61px;
    left:10px;
    width:430px;
    height:528px;
}

    .side-social {
        position:absolute;
        z-index:50;
        top:40px;
        left:20px;
        width:200px;
        height:50px;
        padding:10px;
        border-radius:50px;
        background-color:{color:posts};
        border:1px solid {color:border};
        box-shadow:0px 0px 5px rgba(0,0,0,0.05);
        display:flex;
        justify-content:space-between;
        align-items:center;
        transition:all 0.8s ease;
    }
    
        .side-social:hover,
        .side-follows:hover {
            transform:scale(1.1,1.1);
        }
    
        .side-social img {
            width:50px;
            height:50px;
            border:1px solid {color:border};
            border-radius:50px;
        }
        
        .side-social-text {
            width:140px;
            height:50px;
            margin-left:10px;
            display:flex;
            flex-wrap:wrap;
            justify-content:flex-start;
            align-content:center;
        }
        
            .side-social-text b {
                width:100%;
                color:{color:text};
                font-size:calc({select:fontsize} + 4px);
                font-family:'Poppins', sans-serif;
                margin-bottom:2px;
            }
            
            .side-social-text span {
                color:rgba({RGBcolor:text},0.75);
            }
            
        .side-follows {
            position:absolute;
            z-index:48;
            top:120px;
            left:40px;
            width:auto;
            max-width:220px;
            height:auto;
            padding:10px;
            border-radius:20px;
            background-color:{color:posts};
            border:1px solid {color:border};
            box-shadow:0px 0px 5px rgba(0,0,0,0.05);
            text-align:center;
            transition:all 0.8s ease;
        }
        
            .side-follows b {color:{color:text};}

    .side-info {
        position:absolute;
        z-index:10;
        top:0px;
        left:0px;
        width:199px;
        height:308px;
        padding:200px 20px 20px 20px;
        text-align:left;
        color:{color:text};
        border-radius:10px;
        background-color:{color:accent one};
        border:1px solid {color:border};
        box-shadow:0px 0px 5px rgba(0,0,0,0.05);
    }
    
        .side-info-inner {
            position:absolute;
            bottom:0px;
            width:199px;
            height:auto;
            max-height:308px;
            overflow:auto;
            padding-bottom:20px;
        }
        
            .side-info-inner::-webkit-scrollbar {display:none;}
    
        .side-info h1 {
            position:relative;
            margin:0px 0px 35px 0px;
            font-size:calc({select:fontsize} + 14px);
            line-height:calc({select:fontsize} + 12px);
            color:{color:text};
        }
        
        .side-info h1:after {
            content:'';
            position:absolute;
            bottom:-15px;
            left:0px;
            width:40px;
            height:5px;
            background-color:{color:text};
        }
        
        .side-info b, .side-info i, .side-info strong, .side-info em {
            color:{color:text};
        }

    .side-img {
        position:absolute;
        z-index:12;
        top:20px;
        right:10px;
        width:200px;
        height:280px;
        background-image:url('{image:sidebar}');
        background-position:center center;
        background-repeat:no-repeat;
        background-size:cover;
        border:1px solid {color:border};
        box-shadow:0px 0px 5px rgba(0,0,0,0.05);
        border-radius:10px;
    }
    
    .side-tags {
        position:absolute;
        top:320px;
        right:-10px;
        width:180px;
        height:auto;
        display:flex;
        flex-wrap:wrap;
        justify-content:flex-start;
        align-content:flex-start;
    }
    
        .side-tags a {
            width:auto;
            height:auto;
            padding:4px 6px;
            margin:0px 5px 5px 0px;
            border-radius:50px;
            color:{color:text};
            background-color:{color:posts};
            border:1px solid {color:accent two};
        }
        
            .side-tags a:hover {
                color:{color:posts};
                background-color:{color:accent two};
            }
 
/* --- entries --- */

.entries {
    position:absolute;
    z-index:200;
    top:41px;
    left:410px;
    {block:ifnot500pxposts}
    width:440px;
    {/block:ifnot500pxposts}
    {block:if500pxposts}
    width:540px;
    {/block:if500pxposts}
    height:509px;
    overflow:auto;
    padding:50px 180px 0px 70px;
}

/* --- posts --- */

.post {
    {block:ifnot500pxposts}
    width:400px;
    {/block:ifnot500pxposts}
    {block:if500pxposts}
    width:500px;
    {/block:if500pxposts}
    margin-bottom:60px;
    background-color:{color:posts};
    padding:20px;
    overflow:hidden;
    border-radius:10px;
    border:1px solid {color:border};
}

    .post img {
        max-width:100%;
        height:auto;
        display:block;
    }
    
/* --- pinned --- */

.pinned {
    position:absolute;
    top:35px;
    right:165px;
    width:30px;
    height:30px;
    text-align:center;
    line-height:34px;
    border-radius:20px;
    background-color:{color:posts};
    border:1px solid {color:border};
}


/* --- texts --- */

.title {
    font-size:calc({select:fontsize} + 12px);
    line-height:calc({select:fontsize} + 14px);
    text-align:left;
    width:100%;
    font-family: 'Poppins', sans-serif;
    font-weight:600;
    color:{color:text};
    margin-bottom:20px;
}
    
    .title a {
        color:{color:text};
    }

.more a {
    font-size:calc({select:fontsize} + 8px);
    color:{color:text};
}

.txt {
    margin:0px 0px 20px 0px;
}

    .photo .txt {
        margin:20px 0px 20px 0px;
    }
    
    .txt img {
        {block:ifimagewrap}
        max-width:100%;
        height:auto;
        float:left;
        margin-right:10px;
        {/block:ifimagewrap}
    }
    
    .txt blockquote img {
        {block:ifimagewrap}
        float:right;
        margin-left:10px;
        margin-right:0px;
        {/block:ifimagewrap}
    }
    
        .txt blockquote blockquote img {
            {block:ifimagewrap}
            float:left;
            margin-left:0px;
            margin-right:10px;
            margin-top:0px;
            {/block:ifimagewrap}
        }

/* --- photos --- */

.photo-p, .photo-slideshow {
    margin:-20px -20px 0px -20px;
}

    .photo-p img {
        display:block;
    }

    .photo-slideshow img {
        border-radius:0px;
    }

/* --- quotes --- */

.quote-p {
    font-family: 'Poppins', sans-serif;
    font-weight:600;
    text-align:left;
    font-size:calc({select:fontsize} + 8px);
    line-height:calc({select:fontsize} + 12px);
}

.source {
    margin-top:4px;
    text-align:right;
}

/* --- audio --- */

.audio-p {
    float:left;
    width:70px;
    height:70px;
    position:relative;
    overflow:hidden;
}

    .audio-p:hover .play {opacity:1;width:30px;}
    .audio-p:hover img {margin-left:30px;}
 
.cover img {
    width:70px;
    position:absolute;
    transition:0.5s ease;
}
 
.play {
    overflow:hidden;
    width:0px;
    height:30px;
    background:{color:posts};
    position:absolute;
    padding:20px 0px;
    transition:0.5s ease;
}
 
.au b {
    color:{color:accent one};
    font-weight:800;
    margin-right:2px;
}
 
.au {
    height:45px;
    overflow:hidden;
    padding:12px 10px;
    line-height:calc({select:fontsize} + 5px);
    margin-left:70px;
    text-align:left;
}

/* --- asks --- */

.question {
    margin:0px -20px 20px -20px;
    border-bottom:1px solid {color:border};
    padding:0px 20px 20px 20px;
    font-weight:400;
}

    .question img {
        width:40px;
        height:40px;
        border-radius:40px;
        float:left;
        margin:-10px 10px 0px 0px;
    }

    .question h1 {
        margin:10px 0px;
        font-family: 'Poppins', sans-serif;
        font-weight:600;
        text-transform:lowercase;
    }

    .question p {display:inline;}

/* --- chat --- */

.chat .txt {
    padding:0px;
}

.chat .title {
    margin:-20px -20px 20px -20px;
    padding:20px;
    border-bottom:1px solid {color:border};
}
 
.chat ul {
    list-style-type:none;
    padding-left:0px;
    margin:-20px;
}
 
    .chat ul li:before {
        content: none;
        text-indent: 0px;
    }
    
    .chat ul li {
        padding:20px;
        border-bottom:1px solid {color:border};
    }
    
        .chat ul li:nth-of-type(even) {
            background-color:rgba({RGBcolor:text},0.05);
        }
    
        .chat ul li:last-of-type {
            border:none;
        }
   
    .chat .label {
        text-transform:uppercase;
        font-weight:800;
    }

/* --- permalinks --- */

.permalink {
    width:100%;
    margin:0px -20px 0px -20px;
    padding:20px 20px 0px 20px;
    letter-spacing:0px;
    color:{color:text};
    text-align:left;
    border-top:1px solid {color:border};
    display:flex;
    flex-wrap:wrap;
    justify-content:flex-start;
}

    .permalink a {
        color:{color:text};
        margin:0px 5px 0px 0px;
        line-height:calc({select:fontsize} + 6px);
        display:flex;
        flex-wrap:wrap;
        justify-content:flex-start;
        align-items:center;
    }
    
    .permalink a:hover {
        color:{color:accent one};
    }
    
    .permalink .notecount {
        margin:0px 5px;
    }
    
        .permalink a span, .tags span {
            vertical-align:middle;
            line-height:{select:fontsize};
        }
        
    .perma-first {
        margin-right:5px;
        display:flex;
    flex-wrap:wrap;
    justify-content:flex-start;
    align-content:center;
    }
    .perma-first:after {
        content:'/';
    }
    .perma-first a:first-of-type {
        font-weight:700;
    }

/* --- tags --- */

.tags-c {
    position:relative;
    width:100%;
    margin-top:10px;
}

.tags {
    transition-duration: 0.6s;
    font-weight:400;
}
 
    a.tags {
        display:inline;
        text-transform:none;
        line-height:calc({select:fontsize} + 6px);
        padding:4px 6px;
        margin:2px 4px 2px 0px;
        color:{color:text};
        border-radius:40px;
        background-color:{color:border};
    }
    
        a.tags:hover {
            color:{color:text};
            background-color:{color:link};
        }

/* --- notes --- */

.pagenotes {
    {block:IndexPage}
    display: none!important;
    {/block:IndexPage}
    width:{text:post size}px;
    text-align:left;
    margin-bottom:75px;
    padding:20px;
    background-color:{color:posts};
    border:1px solid {color:border};
    border-radius:10px;
}

    .pagenotes img {
        display:none;
    }
    
    .pagenotes a {
        font-weight:800;
    }
    
    .pagenotes ol {
        list-style-type:none;
        margin:0px;
        padding:0px;
    }
    
    .pagenotes ol li {
        margin:5px;
        line-height:20px;
    }

/* --- right sidebar --- */

.right-sidebar {
    position:absolute;
    z-index:700;
    top:90px;
    {block:ifnot500pxposts}
    left:970px;
    {/block:ifnot500pxposts}
    {block:if500pxposts}
    left:1070px;
    {/block:if500pxposts}
    width:100px;
    height:480px;
    border-radius:10px;
    background-color:{color:posts};
    border:1px solid {color:border};
    box-shadow:0px 0px 5px rgba(0,0,0,0.05);
}
    
    /* --- pagination --- */
    
    .pagination {
        position:absolute;
        top:0px;
        left:0px!important;
        width:100px;
        height:70px;
        text-align:center;
        padding:0px!important;
        color:{color:text};
        display:flex;
        flex-wrap:wrap;
        justify-content:center;
        align-content:center;
    }
    
        .pagination a {
            display:table;
            margin:2px 10px;
            color:{color:text};
            line-height:20px;
        }
        
            .pagination a:hover {
                font-weight:600;
            }

    .right-sidebar-icon {
        position:absolute;
        bottom:14px;
        left:14px;
        width:70px;
        height:70px;
        border-radius:40px;
        background-image:url('{image:right icon}');
        background-position:center center;
        background-repeat:no-repeat;
        background-size:cover;
        border:1px solid {color:border};
    }
    
        .right-sidebar-icon:after {
            content:'';
            position:absolute;
            bottom:94px;
            left:30.5px;
            width:10px;
            height:300px;
            border-radius:10px;
            background-color:{color:border};
            background: {color:accent two};
            background: linear-gradient(0deg, {color:accent two} 10%, {color:accent one} 100%);
        }
        
.right-sidebar-button {
    position:absolute;
    z-index:99999;
    top:30px;
    {block:ifnot500pxposts}
    left:910px;
    {/block:ifnot500pxposts}
    {block:if500pxposts}
    left:1010px;
    {/block:if500pxposts}
    width:120px;
    height:30px;
    padding-right:40px;
    text-align:center;
    line-height:30px;
    font-family:'Poppins', sans-serif;
    letter-spacing:1px;
    background-color:{color:posts};
    border-radius:20px;
    border:1px solid {color:border};
    cursor:pointer;
    overflow:hidden;
    transition:all 0.5s ease;
}

    .right-sidebar-button:before {
        content:'\e017';
        font-family:'saturnicons';
        position:absolute;
        top:0px;
        right:0px;
        width:40px;
        height:30px;
        font-size:18px;
        line-height:0px;
        color:{color:posts};
        background-color:{color:accent two};
        border-left:1px solid {color:border};
        display:flex;
        justify-content:center;
        align-items:center;
    }
    
    .right-sidebar-button:hover {
        margin-top:-5px;
    }

/* --- popup --- */

.slide {
    position:absolute;
    top:0px;
    {block:ifnot500pxposts}
    left:1100px;
    width:1100px;
    {/block:ifnot500pxposts}
    {block:if500pxposts}
    left:1200px;
    width:1200px;
    {/block:if500pxposts}
    height:600px;
}

    .pop-close {
        position:absolute;
        z-index:99999;
        top:30px;
        right:30px;
        width:120px;
        height:30px;
        padding-left:40px;
        text-align:center;
        line-height:30px;
        font-family:'Poppins', sans-serif;
        letter-spacing:1px;
        background-color:{color:posts};
        border-radius:20px;
        border:1px solid {color:border};
        cursor:pointer;
        overflow:hidden;
        transition:all 0.5s ease;
    }
    
        .pop-close:before {
            content:'\e016';
            font-family:'saturnicons';
            position:absolute;
            top:0px;
            left:0px;
            width:40px;
            height:30px;
            font-size:18px;
            line-height:0px;
            color:{color:posts};
            background-color:{color:accent two};
            border-right:1px solid {color:border};
            display:flex;
            justify-content:center;
            align-items:center;
        }
        
        .pop-close:hover {
            margin-top:-5px;
        }
    
    .slide-img {
        position:absolute;
        z-index:12;
        bottom:40px;
        left:40px;
        width:290px;
        height:180px;
        background-image:url('{image:slide out}');
        background-position:center center;
        background-repeat:no-repeat;
        background-size:cover;
        border:1px solid {color:border};
        box-shadow:0px 0px 5px rgba(0,0,0,0.05);
        border-radius:10px;
    }
    
    .slide-links {
        position:absolute;
        z-index:10;
        bottom:10px;
        right:10px;
        {block:ifnot500pxposts}
        width:720px;
        {/block:ifnot500pxposts}
        {block:if500pxposts}
        width:820px;
        {/block:if500pxposts}
        height:130px;
        padding:20px 0px 20px 240px;
        background-color:{color:accent one};
        border:1px solid {color:border};
        box-shadow:0px 0px 5px rgba(0,0,0,0.05);
        border-radius:10px;
        display:flex;
        justify-content:flex-start;
        align-items:flex-start;
    }
    
        .slide-links-group {
            margin:0px 20px 0px 0px;
            {block:ifnot500pxposts}
            width:200px;
            {/block:ifnot500pxposts}
            {block:if500pxposts}
            width:220px;
            {/block:if500pxposts}
            height:auto;
            max-height:130px;
            overflow:auto;
            display:flex;
            flex-wrap:wrap;
            justify-content:flex-start;
            align-content:flex-start;
        }
        
            .slide-links-group h1 {
                color:{color:text};
            }
        
            .slide-links-group a {
                width:100%;
            }
            
                .slide-links-group a:hover {
                    font-style:italic;
                    font-weight:600;
                }
    
    .slide-muses {
        position:absolute;
        right:0px;
        top:50px;
        {block:ifnot500pxposts}
        width:1100px;
        {/block:ifnot500pxposts}
        {block:if500pxposts}
        width:1200px;
        {/block:if500pxposts}
        height:310px;
        padding:20px 0px 40px 0px;
        overflow:auto;
        display:flex;
        flex-wrap:wrap;
        justify-content:center;
        align-content:flex-start;
    }
    
        .muse {
            position:relative;
            margin:10px;
            {block:ifnot500pxposts}
            width:344px;
            height:200px;
            {/block:ifnot500pxposts}
            {block:if500pxposts}
            width:374px;
            height:180px;
            {/block:if500pxposts}
            background:{color:posts};
            border-radius:10px;
            border:1px solid {color:border};
            overflow:hidden;
            display:flex;
            flex-wrap:wrap;
            justify-content:flex-start;
            align-content:flex-start;
        }
        
            .muse-row {
                position:absolute;
                top:0px;
                left:100px;
                {block:ifnot500pxposts}
                width:244px;
                {/block:ifnot500pxposts}
                {block:if500pxposts}
                width:274px;
                {/block:if500pxposts}
                height:90px;
                display:flex;
                flex-wrap:wrap;
                justify-content:flex-start;
                align-content:center;
            }
            
                .muse img {
                    position:absolute;
                    top:10px;
                    left:10px;
                    width:70px;
                    height:70px;
                    border-radius:40px;
                    border:1px solid {color:border};
                }
                
                .muse-row .muse-name,
                .muse-row .muse-handle {
                    {block:ifnot500pxposts}
                    width:244px;
                    {/block:ifnot500pxposts}
                    {block:if500pxposts}
                    width:274px;
                    {/block:if500pxposts}
                    height:20px;
                }
                
                .muse-row .muse-name {
                    font-size:calc({select:fontsize} + 4px);
                    font-weight:600;
                    font-family:'Poppins', sans-serif;
                }
                
                .muse-row .muse-handle {
                    color:rgba({RGBcolor:text},0.75);
                }
                
            .muse-links {
                position:absolute;
                top:90px;
                left:0px;
                width:90px;
                {block:ifnot500pxposts}
                height:110px;
                {/block:ifnot500pxposts}
                {block:if500pxposts}
                height:90px;
                {/block:if500pxposts}
                display:flex;
                flex-wrap:wrap;
                justify-content:center;
                align-content:flex-start;
            }
            
                .muse-links a {
                    display:block;
                    width:25px;
                    height:25px;
                    margin:5px;
                    border-radius:20px;
                    color:{color:accent two};
                    background-color:{color:posts};
                    border:1px solid {color:accent two};
                    line-height:0px;
                    display:flex;
                    justify-content:center;
                    align-items:center;
                }
                
                    .muse-links a:hover {
                        color:{color:posts};
                        background-color:{color:accent two};
                    }
                
            .muse-desc {
                position:absolute;
                top:70px;
                left:100px;
                {block:ifnot500pxposts}
                width:224px;
                height:110px;
                {/block:ifnot500pxposts}
                {block:if500pxposts}
                width:254px;
                height:90px;
                {/block:if500pxposts}
                padding:0px 20px 20px 0px;
                overflow:auto;
            }

/* --- credit --- */

.credit a {
    position:fixed;
    font-size:14px;
    right:10px;
    bottom:10px;
    text-align:center;
    width:30px;
    height:30px;
    line-height:34px;
    color:{color:accent one};
    background-color:{color:posts};
    border-radius:40px;
    border:1px solid {color:border};
}

{CustomCSS}

</style>
</head>
<body>

<div class="hcontrols"><svg version="1.1" id="Layer_1" xmlns="https://www.w3.org/2000/svg" xmlns:xlink="https://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 216 216" enable-background="new 0 0 216 216" xml:space="preserve"><path d="M106.6,134c14.3,0,26-11.7,26-26s-11.7-26-26-26s-26,11.7-26,26S92.2,134,106.6,134z M106.6,94c7.7,0,14,6.3,14,14s-6.3,14-14,14s-14-6.3-14-14S98.9,94,106.6,94z M40.4,124.6l7.2,3.3c3,1.4,4.4,4.8,3.3,7.9l-2.8,7.4c-2.1,5.7-1.4,11.8,2.1,16.7c3.4,5,9,7.9,15,7.9c2.2,0,4.4-0.4,6.5-1.2l7.4-2.8c0.7-0.3,1.4-0.4,2.2-0.4c2.4,0,4.7,1.4,5.7,3.7l3.3,7.2c3,6.6,9.4,10.7,16.6,10.7s13.6-4.1,16.6-10.7l3.3-7.2c1-2.2,3.2-3.7,5.7-3.7c0.7,0,1.5,0.1,2.2,0.4l7.4,2.8c2.1,0.8,4.3,1.2,6.5,1.2c0,0,0,0,0,0c5.9,0,11.5-3,15-7.9c3.4-5,4.2-11.1,2.1-16.7l-2.8-7.4c-1.1-3.1,0.3-6.5,3.3-7.9l7.2-3.3c6.6-3,10.7-9.4,10.7-16.6s-4.1-13.6-10.7-16.6l-7.2-3.3c-3-1.4-4.4-4.8-3.3-7.9l2.8-7.4c2.1-5.7,1.4-11.8-2.1-16.7c-3.4-5-9-7.9-15-7.9c-2.2,0-4.4,0.4-6.5,1.2l-7.4,2.8c-0.7,0.3-1.4,0.4-2.2,0.4c-2.4,0-4.7-1.4-5.7-3.7l-3.3-7.2c-3-6.6-9.4-10.7-16.6-10.7S93,35.2,90,41.8l-3.3,7.2c-1,2.2-3.2,3.7-5.7,3.7c-0.7,0-1.5-0.1-2.2-0.4l-7.4-2.8c-2.1-0.8-4.3-1.2-6.5-1.2c-5.9,0-11.5,3-15,7.9c-3.4,5-4.2,11.1-2.1,16.7l2.8,7.4c1.1,3.1-0.3,6.5-3.3,7.9l-7.2,3.3c-6.6,3-10.7,9.4-10.7,16.6S33.8,121.6,40.4,124.6z M45.3,102.3l7.2-3.3c8.7-4,12.9-14.1,9.5-23l-2.8-7.4c-1-2.7,0-4.7,0.7-5.7c1.6-2.4,4.6-3.4,7.4-2.3l7.4,2.8c2.1,0.8,4.2,1.2,6.4,1.2c0,0,0,0,0,0c7.1,0,13.6-4.2,16.6-10.7l3.3-7.2c1.5-3.4,4.7-3.7,5.7-3.7s4.1,0.3,5.7,3.7l3.3,7.2c3,6.5,9.5,10.7,16.6,10.7c2.2,0,4.3-0.4,6.4-1.2l7.4-2.8c2.8-1,5.7,0,7.4,2.3c0.7,1,1.7,3,0.7,5.7l-2.8,7.4c-3.3,8.9,0.8,19,9.5,23l7.2,3.3c3.4,1.5,3.7,4.7,3.7,5.7s-0.3,4.1-3.7,5.7l-7.2,3.3c-8.7,4-12.9,14.1-9.5,23l2.8,7.4c1,2.7,0,4.7-0.7,5.7c-1.6,2.4-4.6,3.4-7.4,2.3l-7.4-2.8c-2.1-0.8-4.2-1.2-6.4-1.2c-7.1,0-13.6,4.2-16.6,10.7l-3.3,7.2c-1.5,3.4-4.7,3.7-5.7,3.7s-4.1-0.3-5.7-3.7l-3.3-7.2c-3-6.5-9.5-10.7-16.6-10.7c-2.2,0-4.3,0.4-6.4,1.2l-7.4,2.8c-2.8,1-5.7,0-7.4-2.3c-0.7-1-1.7-3-0.7-5.7l2.8-7.4c3.3-8.9-0.8-19-9.5-23l-7.2-3.3c-3.4-1.5-3.7-4.7-3.7-5.7S41.9,103.9,45.3,102.3z"/></svg></div>

<div class="container">

<div class="inner-container">

<div class="topbar">
    <div class="topbar-links">
        <a href="/">home</a>
        <a href="/ask">message</a>
        {block:SubmissionsEnabled}
        <a href="/submit">submit</a>
        {/block:SubmissionsEnabled}
        <a href="/archive">archive</a>
    </div>
</div>

<!-- sidebar -->

<div class="sidebar">

    <div class="side-social">
        <img src="{image:social icon}">
        <div class="side-social-text">
            <b>{text:sidebar name}</b>
            <span>@{Name}</span>
        </div>
    </div>
    
    <div class="side-follows">
        <b>{text:sidebar following}</b> following &nbsp; <b>{text:sidebar followers}</b> followers &nbsp; <b>{text:sidebar posts}</b> posts
    </div>

    <div class="side-info">
        <div class="side-info-inner">
            <h1>{Title}</h1>
            {Description}
        </div>
    </div>
    
    <div class="side-img"></div>
    
    <div class="side-tags">
        {block:iftag1}
        <a href="/tagged/{text:tag 1}">#{text:tag 1}</a>
        {/block:iftag1}
        
        {block:iftag2}
        <a href="/tagged/{text:tag 2}">#{text:tag 2}</a>
        {/block:iftag2}
        
        {block:iftag3}
        <a href="/tagged/{text:tag 3}">#{text:tag 3}</a>
        {/block:iftag3}
        
        {block:iftag4}
        <a href="/tagged/{text:tag 4}">#{text:tag 4}</a>
        {/block:iftag4}
        
        {block:iftag5}
        <a href="/tagged/{text:tag 5}">#{text:tag 5}</a>
        {/block:iftag5}
        
        {block:iftag6}
        <a href="/tagged/{text:tag 6}">#{text:tag 6}</a>
        {/block:iftag6}
    </div>
    
</div>

<!-- start of posts -->

<div class="entries">

{block:Posts}
<div class="post {PostType}" id="{PostID}">

{block:PinnedPostLabel}
    <div class="pinned" title="pinned post">
        <span class="sf sf-push-pin"></span>
    </div>
{/block:PinnedPostLabel}

{block:Quote}
    <div class="txt">
        <div class="quote-p">{Quote}</div>
        {block:Source}
            <div class="source"><p>&mdash; {Source}</p></div>
        {/block:Source}
    </div>
{/block:Quote}


{block:Text}
    {block:Title}
        <div class="title">{Title}</div>
    {/block:Title}
        
    {block:Body}
        <div class="txt">
            {Body}
        
            {block:More}
                <div class="more">
                    <a href="{Permalink}">continue reading...</a>
                </div>
            {/block:More}
        </div>
    {/block:Body}
{/block:Text}

{block:Link}
    <div class="title">
        <a href="{URL}">{Name}</a>
    </div>
    
    {block:Description}
        <div class="txt">
        {Description}
        
        {block:More}
            <div class="more">
                <a href="{Permalink}">continue reading...</a>
            </div>
        {/block:More}
    </div>
    {/block:Description}
{/block:Link}

{block:Chat}
    {block:Title}
        <div class="title">{Title}</div>
    {/block:Title}
   
    <div class="chat">
        <div class="txt">
            <ul>
                {block:Lines}<li>{block:Label}<span class="label">{Label}</span>{/block:Label}
        {Line}</li>{/block:Lines}
            </ul>
        </div>
    </div>
{/block:Chat}

{block:Photo}
    <div class="photo-p">
        <img src="{PhotoURL-1280}" alt="{PhotoAlt}">
    </div>
    {block:Caption}
        <div class="txt">
            {Caption}
            
            {block:More}
                <div class="more">
                    <a href="{Permalink}">continue reading...</a>
                </div>
            {/block:More}
        </div>
    {/block:Caption}
{/block:Photo}

{block:Photoset}
    <div class="photo-slideshow" id="photoset_{PostID}" data-layout="{PhotosetLayout}">
        {block:Photos}
            <div class="photo-data">
                <div class="pxu-photo">
                    <img src="{PhotoURL-1280}" width="{PhotoWidth-1280}" height="{PhotoHeight-1280}" data-highres="{PhotoURL-HighRes}" data-width="{PhotoWidth-HighRes}" data-height="{PhotoHeight-HighRes}">
                </div>
                
                <a class="tumblr-box" rel="post-{PostID}" href="{PhotoURL-HighRes}"></a>
            </div>
        {/block:Photos}
    </div>
    {block:Caption}
        <div class="txt">
            {Caption}
            
            {block:More}
                <div class="more">
                    <a href="{Permalink}">continue reading...</a>
                </div>
            {/block:More}
        </div>
    {/block:Caption}
{/block:Photoset}

{block:Video}
    <div class="photo">{Video-500}</div>
    {block:Caption}<div class="txt">{Caption}</div>{/block:Caption}
{/block:Video}

{block:Audio}
    <div class="txt">
        <div class="audio-p">
            {block:AlbumArt}
                <div class="cover">
                    <img src="{AlbumArtURL}">
                </div>
            {/block:AlbumArt}
            
            {block:AudioPlayer}
                <div class="play">{AudioPlayerWhite}</div>
            {/block:AudioPlayer}
        </div>
        
        <div class="au">
            {block:TrackName}<b>Track:</b> {block:TrackName}{TrackName}<br>{/block:TrackName}
            {block:Artist}<b>Artist:</b> {Artist}<br>{/block:Artist}
            <b>Plays:</b> {FormattedPlayCount}
        </div>
        
        {block:Caption}{Caption}{/block:Caption}
    </div>
{/block:Audio}

{block:Answer}
    <div class="txt">
        <div class="question">
            <img src="{AskerPortraitURL-128}">
            <h1>{Asker} said,</h1>
            &ldquo;{Question}&rdquo;
        </div>
        
        {Answer}
        
        {block:More}
            <div class="more">
                <a href="{Permalink}">continue reading...</a>
            </div>
        {/block:More}
    </div>
{/block:Answer}


{block:Date}
    <div style="clear:both;"></div>
    
    <div class="permalink">
        <div class="perma-first">
            <a href="{Permalink}" class="time-ago">
                {TimeStamp}
            </a>
            
            {block:NoteCount}
                &mdash;
                <a href="{Permalink}" class="notecount">
                    {NoteCountWithLabel}
                </a>
            {/block:NoteCount}
        </div>
        
        {block:RebloggedFrom}
            <a href="{ReblogParentURL}">
                via
            </a>
        {/block:RebloggedFrom}
        
        {block:ContentSource}
            <a href="{SourceURL}">
                source
            </a>
        {/block:ContentSource}
        
        <a href="{ReblogURL}">
            reblog
        </a>
        
        
       
        {block:HasTags}
            <div class="tags-c">
                {block:Tags} <a href="{TagURL}" class="tags">#{Tag}</a>{/block:Tags}
            </div>
        {/block:HasTags}
        
    </div>
{/block:Date}


</div> <!-- end of .post -->


{block:PostNotes}
    <div class="pagenotes">
        {PostNotes}
    </div>
{/block:PostNotes}


{/block:Posts}

</div> <!-- end of entries -->

<div id="trigger" class="right-sidebar-button">
    read more
</div>

<div class="right-sidebar">
    {block:Pagination}
        <div class="pagination">
        {block:PreviousPage}
            <a href="{PreviousPage}">previous page</a>
        {/block:PreviousPage}
        
        {block:NextPage}
            <a href="{NextPage}">next page</a>
        {/block:NextPage}
        </div>
    {/block:Pagination}

    <div class="right-sidebar-icon"></div>
</div>

<!-- popup -->

<div class="slide">
    
    <div class="pop-close">return</div>
    
    <div class="slide-img"></div>
    
    <!-- EDIT SLIDEOUT HERE
    
    to add/remove a list of links,
    copy/delete an entire slide-links-group block
    
    if you want a list without a title,
    but want the links to line up, use this as the title:
    <h1>&nbsp;</h1>
    
    -->
    
    <div class="slide-links">
    
        <div class="slide-links-group">
            <h1>navigation</h1>
            <a href="/">link one</a>
            <a href="/">link two</a>
            <a href="/">link three</a>
            <a href="/">link four</a>
            <a href="/">link five</a>
        </div>
        
        <div class="slide-links-group">
            <h1>extra links</h1>
            <a href="/">link one</a>
            <a href="/">link two</a>
            <a href="/">link three</a>
            <a href="/">link four</a>
        </div>
        
        <div class="slide-links-group">
            <h1>&nbsp;</h1>
            <a href="/">link one</a>
            <a href="/">link two</a>
            <a href="/">link three</a>
        </div>
        
    </div>
    
    <!-- EDIT MUSES HERE
    
    copy & paste an entire .muse block:
    
    <div class="muse">
        <img src="IMG_URL">
    
        <div class="muse-row">
            <div class="muse-name">muse name</div>
            <div class="muse-handle">@musehandle</div>
        </div>
        
        <div class="muse-links">
            <a href="/" title="about">
                <span class="sf sf-user"></span>
            </a>
            <a href="/" title="threads">
                <span class="sf sf-bookmark"></span>
            </a>
        </div>
        
        <div class="muse-desc">
            about the muse
        </div>
    </div>
    
    -->
    <div class="slide-muses">
        
        <!-- muse -->
        <div class="muse">
            <!-- icon -->
            <img src="IMG_URL">
        
            <div class="muse-row">
                <div class="muse-name">muse name</div>
                <div class="muse-handle">@musehandle</div>
            </div>
            
            <div class="muse-links">
                <!-- copy an entire a block to add more links
                for more icons, check the icon link
                near the top of the code -->
                <a href="/" title="about">
                    <span class="sf sf-user"></span>
                </a>
                <a href="/" title="threads">
                    <span class="sf sf-bookmark"></span>
                </a>
            </div>
            
            <div class="muse-desc">
                about the muse. basic html works in here
            </div>
        </div>
        <!-- end of muse -->
        
        <!-- paste new muses between here -->
        
        
        
        <!-- and here -->
        
        
        
    </div>
    <!-- end of muses -->
    
</div>

</div> <!-- end of inner container -->

</div> <!-- end of container -->

<div class="credit"><a class="sf sf-code" href="http://pirateskinned.tumblr.com/" title="coded by pirateskinned"></a></div>

</body></html>

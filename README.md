# tip

#Toggle btn

    <div class="home-page">HOME PAGE</div>
    <button class="nav-trigger">TOGGLE NAV</button>


    .home-page {position: absolute; height: 100%; width: 260px; left: -260px; top: 0; background: red}
    .nav-trigger {position: absolute; left: 300px; top: 20px;}


    $('.nav-trigger').on('click', function(){
        var flag = $(this).data('flag');
    
        $('.home-page').animate({left: flag ? -260 : 0});
    
        $(this).data('flag', !flag);
    });

<template>
   <nav>
    <div class="hamburger">
        <span class="wd"></span>
    </div>
    <div class="nav-center">
        <input type="text" id="dan">
        <i class="fa fa-magnifying-glass" id="loupe"></i>
    </div>
    <div class="nav-right">
        <select class="select">
            <option>Commandes</option>
            <option>Livraison</option>
            <option>Reservation</option>
        </select>
        <i class="fa fa-sun" id="lune"></i>

    </div>
   </nav>
   <!----End of the Navbar -->
   <!-------------------- Start Dashboard -------------------------->
   <div class="dash">
     <div class="link">
        <li><a href="#">Home</a></li>
        <li><a href="#">Master</a></li>
        <li><a href="#">Invoice</a></li>
        <li><a href="#">Contact</a></li>
     </div>
     <div class="follow">
        <a href="https://github.com/WiseDanStack/site_de_restauration_USA">
            <div class="image1"></div>
        </a>
        <a href="https://www.linkedin.com/in/daniel-bougnogolo-3b8603244">
            <div class="image2"></div>
        </a>
        <a href="https://gmail.com/">
            <div class="image3"></div>
        </a>
     </div>
   </div>

</template>

<script>
        
        const dan = document.querySelector('.hamburger');
        const dashboard = document.querySelector('.dash');
        const dany = document.getElementById('dan');
        const daniel = document.getElementById('lune');
        dan.addEventListener('click', () => {
            dan.classList.toggle("active");
            dashboard.classList.toggle("active");
        });
        dany.addEventListener('click', () => {
            dany.style.outline = "none";
            dany.style.border = "none";
            dany.style.padding = "10px";
            dany.style.fontWeight = "bold";
            dany.style.color = "black";

        });
        daniel.addEventListener('click', () => {
            document.body.classList.toggle("dark-theme");
        });
        
export default {

}
</script>

<style>
.dark-theme{
    --primary-color: black;
    --icon-color: white;
    transition: all 2s ease-in;
}
/**** Navbar CSS ****************/
nav{
    display: flex;
    height: 70px;
    width: 100%;
    background-color: var(--primary-color);
    position: fixed;
}
.nav-center{
    position: absolute;
    transform: translateX(500px);
}
.nav-center #dan{
    margin-top: 15px;
    padding: 10px;
    width: 350px;
    border-radius: 15px;
    border: none;
    outline: none;
    transform: translateX(-35px);
}
.nav-center #loupe{
    position: absolute;
    margin-left: 8px;
    margin-top: 20px;
    color: white;
    font-size: 30px;
    transform: translateX(-35px);
    cursor: pointer;
    transition: all .3s ease;
}
.nav-center #loupe:hover{
    color: brown;
}
.nav-right #lune {
    color: var(--icon-color);
    transform: translateX(70px);
}
.nav-right .select {
    padding: 10px;
    outline: none;
    border: none;
    background-color: white;

}
.nav-right .select .option{
    position: absolute;
}
@media only screen and (max-width: 400px){
    nav{
        background-color: var(--primary-color);
        width: 100%;
    }
    nav .hamburger{
        height: 5px;
        width: 30px;
        margin: 30px 10px;
        position: relative;
    }
    nav .hamburger .wd {
        position: absolute;
        height: 5px;
        width: 100%;
        background-color:var(--icon-color);
    
        /*display: none;*/
    }
    nav .hamburger::before {
        margin-top: -9px;
        content: '';
        height: 5px;
        position: absolute;
        background-color: var(--icon-color);
        width: 30px;
        transition: all .4s ease;
        /*
        transform: rotate(45deg) translate(-2px, 12px);*/
    
    }
    nav .hamburger::after {
        margin-top: 10px;
        content: '';
        height: 5px;
        position: absolute;
        background-color: var(--icon-color);
        width: 30px;
        transition: all .6s ease;
        /*
        transform: rotate(-45deg) translate(2px, -15px);*/
    }
    nav .nav-center{
        position: absolute;
        margin-left: 75px;
        transform: translateX(15px);
    }
    nav .nav-center #dan{
        margin-top: 15px;
        padding: 10px;
        width: 150px;
        border-radius: 15px;
        border: none;
        outline: none;
        transform: translateX(-35px);
    }
    nav .nav-center #loupe{
        position: absolute;
        margin-left: 6px;
        margin-top: 20px;
        color: white;
        font-size: 25px;
        transform: translateX(-35px);
        cursor: pointer;
        transition: all .3s ease;
    }
    nav .nav-center #loupe:hover{
        color: brown;
    }
    nav .nav-right #lune {
        color: var(--icon-color);
        position: absolute;
        font-size: 20px;
        transform: translateX(-850px);
        margin-top: 5px;

    }
    nav .nav-right .select {
        display: none;
    }
}
    
.dan{
    position: absolute;
    transform: translateX(-15px);
}
.nav-center .dan {
    /***** input **/

}
.nav-right{
    position: absolute;
    margin-top: 20px;
    transform: translate(1100px);
}


/***********Navbar Css ****************/

/***** Start Hamburger *******************/
.hamburger {
    height: 5px;
    width: 40px;
    margin: 30px 50px;
    position: relative;
}
.nav-center{
    position: absolute;
    transform: translateX(500px);
}
.nav-center #dan{
    margin-top: 15px;
    padding: 10px;
    width: 350px;
    border-radius: 15px;
    border: none;
    outline: none;
    transform: translateX(-35px);
}
.nav-center #loupe{
    position: absolute;
    margin-left: 8px;
    margin-top: 20px;
    color: white;
    font-size: 30px;
    transform: translateX(-35px);
    cursor: pointer;
    transition: all .3s ease;
}
.nav-center #loupe:hover{
    color: brown;
}
    .nav-center{
        position: absolute;
        transform: translateX(500px);
    }
    .nav-center #dan{
        margin-top: 15px;
        padding: 10px;
        width: 350px;
        border-radius: 15px;
        border: none;
        outline: none;
        transform: translateX(-35px);
    }
    .nav-center #loupe{
        position: absolute;
        margin-left: 8px;
        margin-top: 20px;
        color: white;
        font-size: 30px;
        transform: translateX(-35px);
        cursor: pointer;
        transition: all .3s ease;
    }
    .nav-center #loupe:hover{
        color: brown;
    }


.hamburger .wd {
    position: absolute;
    height: 5px;
    width: 100%;
    background-color: var(--icon-color);
    transition: all .6s ease;
    display: block;

    /*display: none;*/
}
.hamburger.active .wd{
    display: none;
}
.hamburger::before {
    margin-top: -10px;
    content: '';
    height: 5px;
    position: absolute;
    background-color: var(--icon-color);
    width: 40px;
    transition: all .4s ease;
    /*
    transform: rotate(45deg) translate(-2px, 12px);*/

}
.hamburger.active::before{
    transform: rotate(45deg) translate(-2px, 12px);
}
.hamburger::after {
    margin-top: 10px;
    content: '';
    height: 5px;
    position: absolute;
    background-color: var(--icon-color);
    width: 40px;
    transition: all .6s ease;
    /*
    transform: rotate(-45deg) translate(2px, -15px);*/
}
.hamburger.active::after{
    transform: rotate(-45deg) translate(2px, -15px);
}
/******************** End Hamburger Menu *************/

/********************* Dashboard **************************/

.dash.active .follow .image1{
    height: 20px;
    width: 20px;
    background-image: url("../assets/Login-Logo/github.png");
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
}
.dash.active .follow .image2{
    height: 20px;
    width: 20px;
    background-image: url("../assets/Login-Logo/linkdin.png");
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
}
.dash.active .follow .image3{
    height: 20px;
    width: 20px;
    background-image: url("../assets/Login-Logo/google.png");
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
}

.dash.active{
    position: absolute;
    margin-top: 100px;
    margin-left: 50px;
    display: flex;
    flex-direction: column;
    height: 400px;
    width: 300px;
    border-radius: 15px;
    background-image: url("dashboard.png");
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
}  
.dash.active .link{
    margin: 100px auto;
}

.dash.active .link li{
    list-style: none;
    margin-bottom: 30px;
}
.dash.active .link a{
    color: whitesmoke;
    text-decoration: none;
    font-size: 20px;
    cursor: pointer;
    transition: all .3s ease;

}
.dash.active .link a:hover{
    color: brown;
}

.dash.active .follow{
    margin: -80px auto;
    display: flex;
}
.dash.active .follow a{
    padding: 20px;
}
/**************** End of the Dashboard ********************/
</style>
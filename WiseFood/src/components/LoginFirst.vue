<template>
    <div class="container">
        <div class="card">
            <div class="logo"></div>
            <p class="devine">
                Hello Bienvenu au <span class="content"><span class="wise">W</span>ise<span class="food">F</span>ood</span> <br>
                Quel est votre prenom svp ??
            </p>
            <div class="name">
                <input type="text" id="write" @click="wise()" v-model="prenom">
            </div>
            <p>
                Quel est vôtre tranche d'âge ?  
            </p>
            <div class="old">
                <input type="checkbox">
                <p class="old1">
                    12 - 19 ans
                </p>
            </div>
            <div class="oldone">
                <input type="checkbox">
                <p class="old1">
                    20 - 35 ans
                </p>
            </div>
            <div class="oldtwo">
                <input type="checkbox">
                <p class="old1">
                    36 - 80 ans
                </p>
            </div>
            <button>
                <a href="https://centredecalcul.netlify.app"><span class="go">Venez Svp</span></a> 
            </button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            prenom: '',
        }
    }, 
    methods: {
        wise () {
            document.getElementById("write").style.outline = "none";
            document.getElementById("write").style.border = "none";
            document.getElementById("write").style.padding = "10px";
            document.getElementById("write").style.fontWeight = "bold";
            document.getElementById("write").style.color = "brown";
        }
    }
}
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Tillana:wght@800&display=swap');
.container{
    height: 100vh;
    width: 100%;
    display: flex;
    background-color: white;
}
.card{
    border-radius: 20px;
    height: 400px;
    width: 500px;
    display: flex;
    flex-direction: column;
    margin: auto;
    background-color: white;
    -webkit-box-shadow: 2px 5px 26px 15px rgba(0, 0, 0, .2); 
    box-shadow: 2px 5px 26px 15px rgba(0, 0, 0, .2);
    animation: dan 2s;
    transition: all .2 ease;
}
.logo{
    height: 100px;
    width: 100px;
    border-radius: 60px;
    background-image: url("../assets/Login-Logo/profil.jpeg");
    background-size: cover;
    background-position: center;
    margin: 5px auto;
}
.card p {
    margin: 2px auto;
    overflow-wrap: break-word;
    font-size: 20px;
}
.name {
    margin: 10px auto;
}
.name #write{
    border: none;
    padding: 10px;
    border-radius: 15px;
    background-color: lightblue;
}
/**** first checkbox************* */
.card .old{
    display: inline-block;
    margin: 0px auto;
}
.card .old1{
    margin-top: -22px;
    transform: translateX(30px);
}
.card .oldone{
    display: inline-block;
    margin: 0px auto;
}
.card .oldtwo{
    display: inline-block;
    margin: -5px auto;
}
.card button{
    height: 20px;
    margin: 9px auto;
    width: 300px;
    padding: 20px;
    border-radius: 10px;
    border: none;
    background-color: red;
    
}
.card .go{
    position: absolute;
    font-size: 20px;
    transform: translateY(-10px);
    margin-left: -47px;
    color: white;
}
.content{
    font-family: 'Tillana', cursive;
    color: rgba(0, 0, 0, .6);
}
.wise{
    color: red;
    font-size: 25px;
}
.food{
    color: blue;
    font-size: 25px;
}
@keyframes dan {
    0%{
        transform: translateY(600px);
    }
    100%{
        transform: translateY(0px);
    }
    
}

@media only screen and (max-width:500px){
    .card{
        width: 300px;
    }
    .card button{
        height: 20px;
        margin: 7px auto;
        width: 170px;
        padding: 20px;
        background-color: red;
        
    }
    .logo{
        height: 70px;
        width: 70px;
        border-radius: 60px;
        background-image: url("../assets/Login-Logo/profil.jpeg");
        background-size: cover;
        background-position: center;
        margin: 5px auto;
    }
    .name input{
        border: none;
        padding: 5px;
    }
}
@media only screen and (max-width:400px){
    .card{
        width: 250px;
        left: 3px;
        right: 3px;
    }
    .card button{
        height: 20px;
        margin: auto;
        width: 170px;
        padding: 20px;
        background-color: red;
        
    }
    .logo{
        height: 70px;
        width: 70px;
        border-radius: 60px;
        background-image: url("../assets/Login-Logo/profil.jpeg");
        background-size: cover;
        background-position: center;
        margin: 5px auto;
    }
    .name input{
        border: none;
        padding: 5px;
    }
    .card p {
    margin: 2px auto;
    overflow-wrap: break-word;
    font-size: 15px;
    }
    .card .oldtwo{
    display: inline-block;
    margin: -5px auto 15px;
    }
    .card .oldone{
    display: inline-block;
    margin: auto;
    margin-top: 10px;
    }
    .card .old1{
    margin-top: -20px;
    transform: translateX(30px);
    }
    @keyframes dan {
    0%{
        transform: translateY(600px);
    }
    100%{
        margin-top: 2px;
        transform: translateY(0px);
    }}

}

button:hover
{
    background-color: red;
    color: white;
    font-weight: bold;
    /*transition: all 2s ease;*/
}
button a{
    text-decoration: none;
    color: white;
}
</style>
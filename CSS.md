* {
    background-color: burlywood;
    /* position: relative; */
}

.container h1 {
    font-size: 40px;
    color: rgb(112, 26, 26);
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    text-align: center;
    margin: 40px;
    padding: 20px;
    position: relative;
}

.opr {
    font-size: 25px;
    text-align: center;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    margin-bottom: 20px;
}

.btn {
    margin-bottom: 90px;
}

.btn button {

  margin: 4px;
    padding: 6px;
    font-size: 16px;
    background-color: rgb(170, 93, 78);
    border: none;
    border-radius: 5px;
    filter: drop-shadow(6px 9px 2px rgba(107, 102, 102, 0.277));
    cursor: pointer;
}
.btn button:hover{
    background-color: rgba(112, 26, 26, 0.8);
    zoom: 104%;

}

.card {
    display: flex;
    justify-content: space-around;
}

.mainbox {
    border: 3px solid black;
    min-height: 6vh;
    min-width: 20vw;
}
.box1{
    font-size: 40px;
    text-align: center;
    border: 2px solid burlywood;
    background-color: rgb(170, 93, 78);
    color: white;
    /* animation: all 5s top; */
}
/* .pushAnimation{
    animation: addbox 5s linear
}

@keyframes addbox {
    from{
        transform: scaleY(0);
        font-size: 0px;
        opacity: 0.1;
    }

  to{
        transform: scaleY(1);
        font-size: 40px;
        opacity: 1;
    }
} */
 .boxAnimation{
    animation: movebox 5s linear(0.39 26.47%, 1 100%);
 }

 @keyframes movebox {
    from{
        transform: scale(0.8);
        font-size: 40px;
        opacity: 0.5;
    }

   to{
        transform: scale(0);
        font-size: 10px;
        opacity: 1;
    }
 }

 .footer{
    position:fixed;
    bottom: 1px;
    background-color: rgb(112, 26, 26);
    width: 99%;
    color: white;
    text-align: center;
    font-size: 24px;
 }

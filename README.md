<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title></title>
  <style>
      body {
        background-color: lightblue;
        text-align: center;
      }

  .lds-ellipsis {
  display: inline-block;
  position: relative;
  width: 80px;
  height: 80px;
}
.lds-ellipsis div {
  position: absolute;
  top: 33px;
  width: 13px;
  height: 13px;
  border-radius: 50%;
  background: #fff;
  animation-timing-function: cubic-bezier(0, 1, 1, 0);
}
.lds-ellipsis div:nth-child(1) {
  left: 8px;
  animation: lds-ellipsis1 0.6s infinite;
}
.lds-ellipsis div:nth-child(2) {
  left: 8px;
  animation: lds-ellipsis2 0.6s infinite;
}
.lds-ellipsis div:nth-child(3) {
  left: 32px;
  animation: lds-ellipsis2 0.6s infinite;
}
.lds-ellipsis div:nth-child(4) {
  left: 56px;
  animation: lds-ellipsis3 0.6s infinite;
}
@keyframes lds-ellipsis1 {
  0% {
    transform: scale(0);
  }
  100% {
    transform: scale(1);
  }
}
@keyframes lds-ellipsis3 {
  0% {
    transform: scale(1);
  }
  100% {
    transform: scale(0);
  }
}
@keyframes lds-ellipsis2 {
  0% {
    transform: translate(0, 0);
  }
  100% {
    transform: translate(24px, 0);
  }
}
@keyframes lds-roller {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

  </style>
  </head>
  <body>
    <script>
      const AS_URL_BASE = "https://script.google.com/macros/s/AKfycbwy9zUKVIoh9boXNkn2P7jIjcch3bUvitPL4Vh13nMlRq4-eKgKOe8WmOMMn0ys6ZVkdQ/exec";

    var url = document.location.href;
      var k = url.substr(url.lastIndexOf("k=")+2);

    if(k){
      fetch(AS_URL_BASE+'?k='+k)
      .then(r => r.text())
      .then((r) => {
        console.log(r);
        //document.write(r);
        if(r){
          document.location.replace(r);
        }
      })
      .catch(err => console.log(err))
    }
      
    </script>

    <div class="lds-ellipsis"><div></div><div></div><div></div><div></div></div>

  </body>
</html>

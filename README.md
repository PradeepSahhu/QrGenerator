# QrGenerator
Here is a Qr code generator which can generate QR CODE of any text or link that is dynamic and flexible.

<a href="https://pradeepsahhu.github.io/QrGenerator/">link</a>

<p>Gradient Background </p>
<img width="1470" alt="image" src="https://github.com/PradeepSahhu/QrGenerator/assets/94203408/e08ded5e-5190-4357-be13-fa0924858dd5">

```js
let image = document.getElementById("generatedImg");
        let userIn = document.getElementsByName("userInput")[0];
        let imageContainer = document.getElementById("ImgContain");
        let Qrbtn = document.getElementsByTagName("button")[0];
        let Resetbtn = document.getElementsByTagName("button")[1];
        console.log(Qrbtn);

    function QrGenerate(){
        
        if(userIn.value.length>0){
            
            image.src = "https://api.qrserver.com/v1/create-qr-code/?size=150x150&data="+ userIn.value;
            imageContainer.classList.add("img-show");
            Qrbtn.textContent = "Generated";
            Resetbtn.style.display = "inline-block";
        }else{
            userIn.classList.add("error");
            setTimeout(()=>{
                userIn.classList.remove("error")
            },1000);

        }
    }
    function resetQr(){
        userIn.value = "";
        imageContainer.classList.remove("img-show");
        Qrbtn.textContent = "Generate QR Code";
        Resetbtn.style.display = "none";
    }
```

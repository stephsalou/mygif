### front element
https://freefrontend.com/
### gif 
https://giphy.com/
### preloader
https://preloaders.net/


# STEP TO ADD THE PRELOADER 
- STEP1 
  add css to your head tag 
```html
  <style>
        /* loader css start */
        .loader {
            position: fixed;
            z-index: 99;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: white;
            display: flex;
            justify-content: center;
            align-items: center;
        }
    
        .loader > img {
            width: 100px;
        }
    
        .loader.hidden {
            animation: fadeOut 1s;
            animation-fill-mode: forwards;
        }
    
        @keyframes fadeOut {
            100% {
                opacity: 0;
                visibility: hidden;
            }
        }
    
        .thumb {
            height: 100px;
            border: 1px solid black;
            margin: 10px;
        }
        /* loader css end */
        </style>
```

- Step2 add loader script to yout head tag again

```html
    <script>
        window.addEventListener("load", function () {
            const loader = document.querySelector(".loader");
            loader.className += " hidden"; // class "loader hidden"

        });
   </script>
```
- step 3 add html loader tag to your body tag

```html
      <div class="loader">
          <img src="/static/gif/807.gif" alt="Loading..." />
      </div>
```



## Another Pure Css Loader code
```html
  <div id="loading"><div class="loader"></div></div>
```

```css
  #loading {
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      position: fixed;
      display: block;
      opacity: 0.7;
      background-color: #000000;
      z-index: 9999;
      text-align: center;
  }
  .loader {
      background: #000000;
      /* margin: 0px auto; */
      font-size: 10px;
      position: absolute;
      top: 45%;
      left: 45%;
      text-indent: -9999em;
      border-top: 1.1em solid rgba(255, 255, 255, 1);
      border-right: 1.1em solid rgba(255, 255, 255, 1);
      border-bottom: 1.1em solid rgba(255, 255, 255, 1);
      border-left: 1.1em solid #f16e00;
      -webkit-transform: translateZ(0);
      -ms-transform: translateZ(0);
      transform: translateZ(0);
      -webkit-animation: load8 1.1s infinite linear;
      animation: load8 1.1s infinite linear;
  }
  .loader, .loader:after {
      border-radius: 50%;
      width: 10em;
      height: 10em;
  }
```

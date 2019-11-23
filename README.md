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
- Step2
  add loader script to yout head tag again
    ```html

          <script>
              window.addEventListener("load", function () {
                  const loader = document.querySelector(".loader");
                  loader.className += " hidden"; // class "loader hidden"

              });
         </script>

```
- step 3 
  add html loader tag to your body tag
  ```html

        <div class="loader">
            <img src="/static/gif/807.gif" alt="Loading..." />
        </div>

```

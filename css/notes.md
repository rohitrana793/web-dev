1.  CSS intro and uses

2.  Types of CSS
    1.inline css
    2.internal css
    3.external css
       <!doctype html>
    <html lang="en">
      <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>CSS</title>
        <!-- external css link -->
        <link rel="stylesheet" href="style.css" />
        <!-- internal css -->
        <style>
          h1 {
            color: blueviolet;
          }
        </style>
      </head>
      <body>
        <!-- inline css -->
        <!-- <h1 style="color: red">hello jee</h1> -->
        <h1>hello jee</h1>
      </body>
    </html>

3.  Selectors in css
    1.  Tag selector
    2.  Class selector
    3.  Id selector
    4.  Combine selector
    5.  Universal selector
    6.  child selector
    7.  attrribute selector
    8.  before and after (::)

        examples:
        <!doctype html>
        <html lang="en">
          <head>
            <meta charset="UTF-8" />
            <meta name="viewport" content="width=device-width, initial-scale=1.0" />
            <title>CSS</title>
            <!-- <link rel="stylesheet" href="style.css" /> -->
            <style>

        ----->combine selector<--------
        .box1 h1,
        .box1 p {
        color: green;
        }

        ----->universal selector<--------
        \*{
        color:red;
        }

        ----->class selector<--------
        .box1 {
        color: purple;
        }
        .box1 p {
        color: red;
        }
        .box2 h1 {
        color: red;
        }

            </style>

          </head>
          <body>
            <!-- inline css -->
            <!-- <h1 style="color: red">hello jee</h1> -->
            <div class="box1">
              <h1>hello jee</h1>
              <p>
                Lorem ipsum dolor, sit amet consectetur adipisicing elit. Optio
                reprehenderit, hic ratione vitae provident ipsa veniam voluptate.
                Reiciendis recusandae suscipit, provident illo quasi voluptate,
                cupiditate a earum harum voluptatibus facere.
              </p>
            </div>
            <hr />
            <div class="box2">
              <h1>sello jee</h1>
              <p>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Optio, amet?
                Nemo similique officia eos iste tempore unde consequatur magnam
                reprehenderit a, impedit, ducimus explicabo nisi eius modi debitis,
                delectus ea.
              </p>
            </div>
          </body>
        </html>

// child selector examples

<!doctype html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>CSS</title>
<!-- <link rel="stylesheet" href="style.css" /> -->
<style>
.box > h1 {
color: red;
}
          .box .c-box h1 {
            color: purple;
          }
        </style>

      </head>
      <body>
        <div class="box">
          <h1>hello jee</h1>
          <div class="c-box">
            <h1>sello jee</h1>
          </div>
        </div>
      </body>
    </html>

// nth child selector examples

<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CSS</title>
    <style>
      li:first-child {
        color: #ff0000;
      }
      li: nth-child(2n+1){
        color: #ff0000;
      }
      li: nth-child(even){
        color: #ff0000;
      }
      li: nth-child(odd){
        color: #ff0000;
      }
      li:nth-child(2n) {
        color: #ff0000;
      }
    </style>
  </head>
  <body>
    <ol>
      <li>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Mollitia
      </li>
      <li>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Mollitia
      </li>
      <li>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Mollitia
      </li>
      <li>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Mollitia
      </li>
      <li>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Mollitia
      </li>
      <li>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Mollitia
      </li>
    </ol>
  </body>
</html>

// attribute selector selector examples

<style>
_ {
}
img[alt="image1"] {
height: 200px;
}
input[type="email"]:focus {
background-color: aqua;
}
input[type="checkbox"]:checked {
/_ color: red; \*/
accent-color: red;
}
</style>
  <body>
    <input type="text" placeholder="username" />
    <input type="email" placeholder="email" />
    <input type="checkbox" />
    <br />
    <br />
    <img
      src="https://images.unsplash.com/photo-1772289935663-80aa987be656?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHwzfHx8ZW58MHx8fHx8"
      alt="image1"
    />
    <br />
    <img
      src="https://images.unsplash.com/photo-1772289935663-80aa987be656?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHwzfHx8ZW58MHx8fHx8"
      alt="image2"
    />
  </body>

// before and after examples

before and after (::)--> we have to use two colon.
It is used to insert content before or after an element.
examples:

<!doctype html>

   <html lang="en">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <title>CSS</title>
       <style>
         p::before {
           content: "hello jee";
           color: red;
         }
         p::after {
           content: "world";
           color: green;
         }
         .c {
           color: red;
         }
       </style>
     </head>
     <body>
       <p>
         Lorem ipsum dolor sit amet <span class="c">consectetur </span>adipisicing
         elit. Ipsa quasi non tenetur libero dolores accusantium, quibusdam
         corporis quae ratione vero consequatur officiis error eaque provident
         earum harum excepturi deserunt adipisci!
       </p>
     </body>
   </html>

4.  Text styling in CSS
    1. color for text
       p {
       color: rgb(50, 100, 150); // rgb
       color: rgba(50, 100, 150, 0.5); // rgba
       color: #9cee69; //hex code
       }
    2. text-align for text
       p{
       text-align: center;
       text-align: left;
       text-align: right;
       text-align: justify;
       }
    3. text-transform for text
       p{
       text-transform: uppercase;
       text-transform: lowercase;
       text-transform: capitalize;
       }
    4. text-decoration for text
       p{
       text-decoration: overline 2px red;
       text-decoration: line-through 2px red;
       text-decoration: underline 2px red;
       text-underline-offset: 10px;
       }
    5. text-indent for text
       P{
       text-indent: 50px;
       // give space at the begining of the text.
       }
    6. text-shadow for text
       h1{
       text-shadow: 0px 10px 2px red;
       text-shadow: 0px 10px 2px rgba(50, 100, 150, 0.5);
       }

       // we can also add extra layer  
       h1 {
       0px 5px 2px rgba(250, 170, 50, 0.5),
       0px 5px 2px rgba(200, 70, 150, 0.3);
       }

    7. font-family for text
         <style>
         @import url("https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,400;0,700;0,900;1,400;1,700;1,900&family=Lora:ital,wght@0,400..700;1,400..700&family=Montserrat:ital,wght@0,100..900;1,100..900&family=Mukta:wght@200;300;400;500;600;700;800&family=Nunito+Sans:ital,opsz,wght@0,6..12,200..1000;1,6..12,200..1000&family=Outfit:wght@100..900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap");
         * {
           font-family: "Lato", serif;
         }
       </style>

       body {
       font-family: "Lato", serif;
       }
       p {
       font-family: Verdana, Geneva, Tahoma, sans-serif;
       }

5.  Box Model Concepts in CSS

// box height, widht, margin, padding, box-border, border-radius , overflow:hidden , overflow:auto, word-wrap and word-break

 <style>
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }
      .bx {
        height: 200px;
        width: 200px;
        background-color: red;
        margin-left: 20px;
        margin-right: 20px;
        margin-top: 20px;
        margin-bottom: 20px;
        margin: 10px;
        margin: 10px 20px;
        margin: 10px 20px 5px 20px;
        padding: 10px;
        border: 2px solid black;
        border-top: 2px solid black;
        border-bottom: 2px solid black; 
        border-radius: 50%; 
        border-radius: 10px 20px;
        border-radius: 10px 20px 40px 30px;
        border-radius: 10px;
        overflow: hidden;
        word-break: break-all;
        word-wrap: break-word;
      }
    </style>
<body>
    <div class="bx">
      <!-- <p>
        Lorem ipsum dolor, sitssssssss amet consectetur asss
        ssdsdssssadipisicing elit. Nisi in ad cumque voluptate, doloremque vero
        optio error nihil. Facilis consectetur a laborum doloremque repudiandae
        architecto alias quaerat beatae aspernatur esse! Lorem ipsum dolor sit
        amet, consectetur adipisicing elit. Corporis unde vel hic officiis ullam
        commodi architecto porro corrupti rerum possimus. Quos totam repudiandae
        molestias harum enim at. Impedit, porro consectetur.
      </p> -->
      <p>
        Lorem ipsum, dolor sit ametsssss consectetur adipisicing elit. Aliquam
        sssssss beatae, libero deleniti, aperiam praesentium ab illo, possimus
        sequi tempore fugit iusto pariatur fugiat. Atque debitis deleniti amet?
        Suscipit, sunt ea?
      </p>
    </div>
</body>

6.  CSS Positions
    1.position-absolute example
    <style> \* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    }
    .bx {
    height: 200px;
    width: 200px;
    background-color: red;
    position: absolute;
    }
    .bx1 {
    height: 200px;
    width: 200px;
    background-color: purple;
    position: absolute;
    top: 200px;
    left: 200px;
    }
    .bx2 {
    height: 200px;
    width: 200px;
    background-color: green;
    position: absolute;
    top: 400px;
    left: 400px;
    }
    </style>
    <body>
    <div class="bx"></div>
    <div class="bx1"></div>
    <div class="bx2"></div>
    </body>

    2.position-relative example
    <style> \* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    }
    .bx {
    height: 200px;
    width: 200px;
    background-color: red;
    position: relative;
    }
    .cbx1 {
    height: 50px;
    width: 50px;
    background-color: purple;
    position: absolute;
    top: 0;
    }
    .cbx2 {
    height: 50px;
    width: 50px;
    background-color: black;
    position: absolute;
    top: 50px;
    left: 50px;
    }
    .cbx3 {
    height: 50px;
    width: 50px;
    background-color: green;
    position: absolute;
    top: 100px;
    left: 100px;
    }
    .cbx4 {
    height: 50px;
    width: 50px;
    background-color: yellow;
    position: absolute;
    top: 150px;
    left: 150px;
    }
    </style>

        <body>
        <div class="bx">
        <div class="cbx1"></div>
        <div class="cbx2"></div>
        <div class="cbx3"></div>
        <div class="cbx4"></div>
        </div>
        </body>

    3.postion-fixed and position-sticky example
      <style>
      {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      }
      .bx {
      height: 100px;
      width: 800px;
      background-color: red;
      position: fixed;
      position: sticky;
      top: 0;
      }
      </style>
      <body>
      <div class="bx"></div>
      <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab voluptate quod
      quidem, ut, dolor veritatis sed, suscipit aperiam sit vel porro saepe fuga
      facere expedita deserunt corporis? Laudantium maiores error necessitatibus
      ipsa reprehenderit quo debitis adipisci exercitationem, accusamus laborum
      molestiae, ea eius dicta vero fugiat pariatur quidem dolorem voluptatibus
      asperiores et vel fugit animi magnam! Quam nam quibusdam officia quis odit
      eveniet magnam esse corporis iste eligendi suscipit, quidem illum
      perferendis a eos ipsa autem fugit molestias accusantium sit sunt sequi.
      Nemo, odit esse. Quia, commodi inventore dolor voluptatibus non similique
      quis adipisci asperiores eaque error molestiae quidem laboriosam
      voluptatum qui ab. Tempora, deserunt, ea delectus odit consectetur,
      voluptatem tempore vel dicta nihil quaerat quibusdam explicabo voluptas
      perferendis veniam dolorum asperiores autem sit ipsam! Nobis repellat
      ratione numquam quaerat, id vero aliquid placeat corrupti ut, asperiores
      nam accusamus sint dignissimos unde rem ex non deserunt in beatae
      adipisci? A obcaecati ut cum nobis vitae vel quaerat aut, excepturi minus
      porro provident nisi, dolor eaque assumenda deleniti totam nam nihil
      similique expedita distinctio accusamus! Eum illo repudiandae, tenetur
      magnam ipsa, dolore nisi ullam officia qui aspernatur dicta consequatur
      cum consequuntur enim illum sunt similique reiciendis. Ullam ipsa Lorem
      ipsum dolor sit amet consectetur adipisicing elit. Praesentium labore at,
      nemo nisi repellendus soluta quibusdam dolorem dicta facere tempore
      consectetur provident deserunt quisquam fugit, quidem ratione debitis nam
      aperiam? Lorem ipsum, dolor sit amet consectetur adipisicing elit.
      Quibusdam aut eum, magni natus sunt dolores harum molestias deserunt
      praesentium, corporis consequatur culpa ad, veritatis recusandae officiis
      et. Omnis, repellendus! Laudantium. In vel, magnam sit adipisci esse
      repudiandae temporibus doloremque atque illo excepturi architecto fugiat
      vero amet asperiores beatae! Maxime rerum quam ab veniam, nobis velit sit
      molestiae praesentium explicabo beatae! Eveniet deserunt nostrum id eius
      unde earum quos, expedita, veritatis mollitia voluptate numquam aliquam!
      Animi, odit amet reprehenderit quidem illum impedit quis. Tempore atque
      repudiandae pariatur tenetur commodi, similique provident? Officia animi
      unde neque dolorum aperiam earum, voluptas in aspernatur veritatis
      consequuntur sed facere, assumenda ab. Beatae odit, maxime tempora fugit
      aliquid fugiat odio qui quae fuga ea repudiandae illo? Impedit dolorem
      facilis expedita nisi. Laborum in est, consequuntur ratione odit, corrupti
      sapiente iste, quia eaque maxime pariatur rerum ducimus eius? Voluptatum
      reiciendis odio corrupti libero repudiandae nulla laborum harum. Vel cum
      dolorum fugiat totam veniam corporis odit, pariatur repudiandae a quis
      voluptates sed quia distinctio tenetur? Quisquam temporibus delectus,
      veritatis asperiores aliquid magni odio distinctio quia voluptatum impedit
      voluptatibus! Iure ducimus incidunt id dolorem porro, maxime vero ipsum
      libero vitae fuga numquam fugiat debitis doloribus corrupti culpa
      veritatis placeat quibusdam et fugit qui atque. Eum quasi minus quae
      laborum. Dolor, aliquid, corporis nulla deserunt dolore facere asperiores,
      </p>
    </body>

7.  Pixel and Percentage
    Pixel is fixed unit and Percentage is relative unit and it takes width according to the device width.
    pixel and percentage example:
    <style> 
    * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    }
    .bx {
    height: 300px;
    width: 700px;
    width: 100%;
    background-color: red;
    }
    </style>
    <body>
      <div class="bx">
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Velit, iste?
          Rerum doloremque, quae nemo, nam saepe accusantium ipsa recusandae vel
          minus distinctio ipsam ea odio repellat iusto quis, voluptatem fugiat.
        </p>
      </div>
    </body>

8.max-width and min-width
examples:

<style>
*{
margin: 0;
padding: 0;
box-sizing: border-box;
}
.bx {
height: 300px;
min-width: 500px;
background-color: red;
}
</style>

  <body>
    <div class="bx">

    </div>

  </body>

9.  viewport width and viewport height
    1vw = 1% of the viewport width
    Viewport = the visible area of the browser window
    examples:
    <style>
     * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    }
    .bx {
    height: 300px;
    max-width: 500px;
    background-color: red;
    }
    .cbx {
    height: 100px;
    width: 50vw;
    background-color: black;
    }
    </style>
      <body>
        <div class="bx">
          <div class="cbx"></div>
        </div>
      </body>
    </html>

10. Using images in box, using image property and also using box-shadow
    examples:
    <style>
    _ {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    }
    body {
    padding: 10px;
    }
    .bx {
    height: 200px;
    width: 200px;
    border: 1px solid black;
    /_ box-shadow:
    10px 10px 10px 3px red,
    15px 15px 15px 3px purple; _/
    box-shadow:
    rgba(240, 46, 170, 0.4) 5px 5px,
    rgba(240, 46, 170, 0.3) 10px 10px,
    rgba(240, 46, 170, 0.2) 15px 15px,
    rgba(240, 46, 170, 0.1) 20px 20px,
    rgba(240, 46, 170, 0.05) 25px 25px;
    }
    img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    /_ filter: brightness(50%) grayscale(50%) contrast(5px); _/
    /_ border-radius: 50%; _/
    /_ clip-path: circle(); _/
    /_ clip-path: polygon(
    50% 0%,
    61% 35%,
    98% 35%,
    68% 57%,
    79% 91%,
    50% 70%,
    21% 91%,
    32% 57%,
    2% 35%,
    39% 35%
    ); \*/
    }
    </style>
    <body>
    <div class="bx">
    <img
                src="https://images.unsplash.com/photo-1771845630625-43c6b807ffb5?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHwxMnx8fGVufDB8fHx8fA%3D%3D"
                alt=""
              />
    </div>
    </body>

11. Background Image
    examples:

<style>
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }
      body {
        padding: 10px;
      }
      .bx {
        height: 300px;
        width: 300px;
        border: 1px solid black;
        background-image: url(https://images.unsplash.com/photo-1761850648640-2ee5870ee883?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDF8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw4NXx8fGVufDB8fHx8fA%3D%3D);
        background-repeat: no-repeat;
        background-size: cover;
        /* background-position: right top; */
        /* background-color: red;
        background-blend-mode: darken; */
      }
      .tb {
        backdrop-filter: blur(5px);
      }
    </style>

    <body>
       <div class="bx">
        <div class="tb">
        <h1 style="color: white">hello jee</h1>
       </div>
      </div>
     </body>

12. Covert block to inline and vice versa.
    h1 is block element and span is inline element.
    we cannot give hight and width to inline element but we can give to block element.
    examples:
    <style>
    *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    }
    body {
    padding: 10px;
    }
    h1 {
    background-color: red;
    display: inline;
    }
    span {
    background-color: purple;
    display: block;
    } 
    span {
    background-color: purple;
    display: inline-block; 
    // makes the element inline and block and we can also give hight and width when we make display inline-block.
    height: 50px;
    }
    </style>

13. Animations in CSS
    1. usiing transition property
       example:
       <style>
         *{
           margin: 0;
           padding: 0;
           box-sizing: border-box;
           }
           body {
           padding: 10px;
           }
           .bx {
           height: 200px;
           width: 200px;
           background-color: red;
           transition: all 200ms cubic-bezier(0.075, 0.82, 0.165, 1) 0s;
           }
           .bx:hover {
           width: 400px;
           transform: translate(50px) scale(2) rotate(360deg);
           }
         </style>
         <body>
         <div class="bx"></div>
         </body>
    2. animation using @keyframes
       examples:
        <style>
         * {
           margin: 0;
           padding: 0;
           box-sizing: border-box;
         }
         body {
           padding: 10px;
         }
         .bx {
           height: 200px;
           width: 200px;
           background-color: red;
           /* animation: name duration timing-function delay iteration-count direction
             fill-mode; */
           animation: any 5s cubic-bezier(0.075, 0.82, 0.165, 1) 0s infinite
             reverse;
         }
         /*
          @keyframes any {
           0% {
           }
           10% {
             transform: rotate(45deg);
           }
           20% {
           }
           50% {
             background-color: purple;
             transform: scale(2);
           }
           60% {
             background-color: brown;
             transform: rotate(360deg);
           }
           100% {
             margin-left: 50px;
           }
         } */
         @keyframes any {
           0% {
           }
           50% {
             background-color: green;
             transform: translateX(100px);
           }
           80% {
             transform: rotate(360deg);
           }
           100% {
           }
         }
       </style>
       <body>
       <div class="bx"></div>
       </body>

14. Flex and Grid in CSS
    Flex is used for one dimensional layout.
    Grid is used for two dimensional layout.
    flex example 1:
      <style>
        * {
          margin: 0;
          padding: 0;
          box-sizing: border-box;
        }
        body {
          padding: 10px;
        }
        .bx {
          max-width: 600px;
          /* height: 500px; */
          border: 1px solid black;
        }
      
        .bx {
          display: flex;
          /* gap: 20px; */
          /* justify-content: end;  horizonatal move huncha*/
          /* justify-content: center; */
          /* align-items: center; vertical move huncha*/
          /* align-items: center; */
        }
      
        .item1 {
          background-color: red;
        }
        .item2 {
          background-color: purple;
        }
        .item3 {
          background-color: yellow;
        }
        .item4 {
          background-color: violet;
        }
        .item5 {
          background-color: thistle;
        }
      </style>

// flex direction column examples:

<style> \* {
margin: 0;
padding: 0;
box-sizing: border-box;
}
body {
padding: 10px;
}

      /*
      Notes: if flex direction is column then justify-content moves vertical and align-items moves horizontal
      */

      .bx {
        max-width: 600px;
        height: 500px;
        border: 1px solid black;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 20px;
      }
  
      .item1 {
        background-color: red;
      }
      .item2 {
        background-color: purple;
      }
      .item3 {
        background-color: yellow;
      }
      .item4 {
        background-color: violet;
      }
      .item5 {
        background-color: thistle;
      }
    </style>

      <body>
      <div class="bx">
        <div class="item item1">
          <h3>box1</h3>
        </div>
        <div class="item item2">
          <h3>box2</h3>
        </div>
        <div class="item item3">
          <h3>box3</h3>
        </div>
        <div class="item item4">
          <h3>box4</h3>
        </div>
        <div class="item item5">
          <h3>box5</h3>
        </div>
      </div>
    </body>

// flex important properties

1. flex grow
2. flex shrink
3. flex basis

examples:

<style>
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }
      body {
        padding: 10px;
      }

      /* flex-grow flex basis flex shrink*/
      /* flex-wrap */

      .bx {
        max-width: 600px;
        /* height: 500px; */
        border: 1px solid black;
        display: flex;
        /* flex-wrap: wrap;  */
        /*by default flex-wrap:nowrap */
      }

      .item {
        flex-basis: 100px;
        flex-grow: 1; /*sab box le baki vako space equally occupy garcha */
      }

      .item1 {
        background-color: red;
        /* flex-grow: 1; by default flex grow 0 */
        flex-shrink: 0; /*by default 1 */
      }
      .item2 {
        background-color: purple;
        /* flex-grow: 2; */
      }
      .item3 {
        background-color: yellow;
      }
      .item4 {
        background-color: violet;
      }
      .item5 {
        background-color: thistle;
      }
    </style>

      <body>
    <div class="bx">
      <div class="item item1">
        <h3>box1</h3>
      </div>
      <div class="item item2">
        <h3>box2</h3>
      </div>
      <div class="item item3">
        <h3>box3</h3>
      </div>
      <div class="item item4">
        <h3>box4</h3>
      </div>
      <div class="item item5">
        <h3>box5</h3>
      </div>
    </div>

15. Grid in CSS
    examples:
      <style> 
      *{
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      }
      body {
      padding: 10px;
      }
      
            .bx {
              max-width: 600px;
              height: 300px;
              border: 1px solid black;
              display: grid;
      
              /* grid-templete-colums width size increase garcha*/
              grid-template-columns: 100px 200px;
              /* grid-template-columns: repeat(5, 1fr); */
      
              /* grid-template-rows height size increase garcha */
              /* grid-template-rows: 100px 50px; */
              /* grid-template-rows: 50px 50px 50px; */
              /* grid-template-rows: repeat(3, 100px); */
      
              /* justify-content is used to move the content horizonatally */
              /* justify-content: end; */
      
              /* align-content: center; */
              /* align-content is used to move the content vertically */
      
              /* justify-items: center; */
              /*difference between justify-content and justify-items*/
      
              /* place-items: center; */
              /* all grid items will be centered vertically and horizontally inside their grid cells. */
      
              /* place-content: center; */
              /* The whole grid content moves to the center of the container. */
            }
      
            .item1 {
              /* place-self: center; */
              /* it means the item will be centered both horizontally and vertically inside its grid cell. */
              /* justify-self: end; */
              /* used to move individual content in horizontal direction */
              background-color: red;
            }
            .item2 {
              background-color: blue;
            }
            .item3 {
              background-color: yellowgreen;
            }
            .item4 {
              background-color: turquoise;
            }
            .item5 {
              background-color: tomato;
            }
          </style>

           <body>

      <div class="bx">
        <div class="item item1">
          <h3>box1</h3>
        </div>
        <div class="item item2">
          <h3>box2</h3>
        </div>
        <div class="item item3">
          <h3>box3</h3>
        </div>
        <div class="item item4">
          <h3>box4</h3>
        </div>
        <div class="item item5">
          <h3>box5</h3>
        </div>
      </div>
    </body>

16. Grid Position
    examples:
    <style> 
    * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    }
    body {
    padding: 10px;
    }
        .bx {
          max-width: 600px;
          /* height: 300px; */
          border: 1px solid black;
          display: grid;
          grid-template-columns: 100px 200px;
          grid-template-rows: repeat(3, 100px);
        }
    
        .item1 {
          background-color: red;
          /* moving box1 to box4 postion */
          /* grid-column: 2/3;
          grid-row: 2/3; */
    
          /* grid-column: span 2; */
          /* grid-row: span 2; */
        }
        .item2 {
          background-color: blue;
        }
        .item3 {
          background-color: yellowgreen;
        }
        .item4 {
          background-color: turquoise;
          grid-row: span 2;
        }
        .item5 {
          background-color: tomato;
          /* moving box5 to box3 postion */
          /* grid-column: 1/2;
          grid-row: 2/3; */
        }
      </style>

        <body>

      <div class="bx">
        <div class="item item1">
          <h3>box1</h3>
        </div>
        <div class="item item2">
          <h3>box2</h3>
        </div>
        <div class="item item3">
          <h3>box3</h3>
        </div>
        <div class="item item4">
          <h3>box4</h3>
        </div>
        <div class="item item5">
          <h3>box5</h3>
        </div>
      </div>
    </body>

17. Responsive cheat code in grid
    example:
      <style>
        * {
          margin: 0;
          padding: 0;
          box-sizing: border-box;
        }
        body {
          padding: 10px;
        }
        .grid-box {
          display: grid;
          grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
          gap: 20px;
        }
        img {
          width: 100%;
        }
      </style>
       <body>
      <div class="grid-box">
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>

        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>
        <div>
          <img
            src="https://images.unsplash.com/photo-1772752021241-2d922cadbab1?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
            alt=""
          />
        </div>

      </div>
    </body>

18. Naming
    examples:
       <style>
        * {
          margin: 0;
          padding: 0;
          box-sizing: border-box;
        }
        body {
          padding: 10px;
        }
      
        main {
          display: grid;
          grid-template-areas:
            "header header header header header"
            "leftNav topArticle topArticle topArticle topArticle"
            "leftNav leftArticle leftArticle rightArticle rightArticle"
            "footer footer footer footer footer";
          grid-template-rows: repeat(4, 150px);
        }
      
        /* Naming */
        header {
          grid-area: header;
          background-color: skyblue;
        }
        .left-nav {
          grid-area: leftNav;
          background-color: yellow;
        }
        .top-article {
          grid-area: topArticle;
          background-color: pink;
        }
        .left-article {
          grid-area: leftArticle;
          background-color: blue;
        }
        .right-article {
          grid-area: rightArticle;
          background-color: silver;
        }
        footer {
          grid-area: footer;
          background-color: red;
        }
      </style>
       <body>
      <main>
        <header>
          <h1>Header</h1>
        </header>
        <div class="left-nav">
          <h1>Left Nav</h1>
        </div>
        <div class="top-article">
          <h1>Top Article</h1>
        </div>
        <div class="left-article">
          <h1>Left Article</h1>
        </div>
        <div class="right-article">
          <h1>Right Article</h1>
        </div>
        <footer><h1>Footer</h1></footer>
      </main>
    </body>

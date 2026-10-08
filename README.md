<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>MORTALITY — Skate Apparel</title>

<style>
:root{
  color-scheme:dark;
  --bg:#000;
  --panel:#0a0a0a;
  --text:#fff;
  --muted:#9a9a9a;
  --line:#242424;
  --accent:#fff;
  --danger:#555
}

*{box-sizing:border-box}

html{scroll-behavior:smooth}

body{
  margin:0;
  font-family:"Trebuchet MS",Arial,Helvetica,sans-serif;
  background:var(--bg);
  color:var(--text)
}

#app{
  min-height:100vh;
  background:var(--bg)
}

header{
  position:sticky;
  top:0;
  z-index:20;
  background:color-mix(in srgb,var(--bg) 90%,transparent);
  backdrop-filter:blur(12px);
  border-bottom:1px solid var(--line)
}

.nav{
  max-width:1280px;
  margin:auto;
  height:76px;
  padding:0 28px;
  display:flex;
  align-items:center;
  justify-content:space-between
}

.logo{
  font-size:27px;
  font-weight:950;
  letter-spacing:-1.8px
}

.logo span{color:var(--accent)}

nav{
  display:flex;
  gap:32px
}

nav a{
  color:var(--text);
  text-decoration:none;
  font-size:11px;
  font-weight:800;
  text-transform:uppercase;
  letter-spacing:1.6px
}

nav a:hover{color:var(--accent)}

nav a.active{color:var(--accent)}

.cart{
  border:1px solid var(--line);
  background:var(--panel);
  color:var(--text);
  padding:11px 15px;
  font-weight:900;
  cursor:pointer
}

.hero{
  max-width:none;
  margin:auto;
  padding:105px 28px 90px;
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:40px;
  align-items:stretch
}

.hero h1{
  font-size:clamp(58px,7vw,110px);
  line-height:.76;
  margin:0 0 34px;
  letter-spacing:-6px;
  font-weight:1000;
  font-family:Georgia,"Times New Roman",serif
}

.eyebrow{
  font-size:10px;
  font-weight:900;
  letter-spacing:3.5px;
  color:var(--accent);
  margin-bottom:20px
}

.hero p{
  max-width:540px;
  color:var(--muted);
  font-size:16px;
  line-height:1.7
}

.buttons{
  display:flex;
  gap:12px;
  margin-top:30px
}

.btn{
  display:inline-block;
  padding:16px 22px;
  text-decoration:none;
  font-size:11px;
  font-weight:950;
  text-transform:uppercase;
  letter-spacing:1.4px;
  border:1px solid var(--text);
  cursor:pointer
}

.primary{
  background:var(--accent);
  color:#000;
  border-color:var(--accent)
}

.secondary{
  color:var(--text);
  background:transparent
}

.poster{
  aspect-ratio:4/5;
  min-height:100%;
  background:#050505;
  border:1px solid #333;
  position:relative;
  overflow:hidden;
  display:grid;
  place-items:center
}

.poster:before{
  content:"MORTALITY";
  position:absolute;
  font-size:64px;
  font-weight:1000;
  letter-spacing:-5px;
  transform:rotate(-90deg);
  opacity:.08
}

.poster:after{
  content:"01";
  position:absolute;
  top:18px;
  right:20px;
  font-size:10px;
  letter-spacing:2px;
  color:#777
}

.skull{
  font-size:150px;
  line-height:1;
  filter:grayscale(1)
}

.poster .stamp{
  position:absolute;
  bottom:20px;
  left:20px;
  font-size:10px;
  font-weight:900;
  letter-spacing:2px;
  background:var(--accent);
  color:#000;
  padding:9px 11px
}

.section{
  max-width:1280px;
  margin:auto;
  padding:90px 28px
}

.section-head{
  display:flex;
  justify-content:space-between;
  align-items:end;
  margin-bottom:34px
}

.section h2{
  font-size:46px;
  letter-spacing:-2.5px;
  margin:0;
  font-family:Georgia,"Times New Roman",serif
}

.section-head p{
  color:var(--muted);
  font-size:11px;
  letter-spacing:1.5px
}

.grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:20px
}

.product{
  background:var(--panel);
  border:1px solid var(--line);
  padding:12px
}

.product-art{
  aspect-ratio:1/1.05;
  background:#000;
  display:grid;
  place-items:center;
  position:relative;
  overflow:hidden
}

.product-art:after{
  content:"MORTALITY / DROP 01";
  position:absolute;
  bottom:15px;
  right:15px;
  font-size:8px;
  letter-spacing:2px;
  color:#555
}

.shirt{
  width:58%;
  height:67%;
  background:#fff!important;
  clip-path:polygon(
    20% 0,
    35% 8%,
    65% 8%,
    80% 0,
    100% 20%,
    82% 34%,
    77% 100%,
    23% 100%,
    18% 34%,
    0 20%
  );
  position:relative
}

.shirt:after{
  content:"MORTALITY";
  position:absolute;
  top:42%;
  left:12%;
  right:12%;
  text-align:center;
  color:#111!important;
  font-weight:1000;
  font-size:15px;
  letter-spacing:2px;
  transform:rotate(-8deg)
}

.shirt.two{
  background:#fff
}

.shirt.two:after{
  content:"MAKE YOUR MARK";
  color:#111;
  font-size:12px
}

.tag{
  position:absolute;
  top:12px;
  left:12px;
  background:var(--accent);
  color:#000;
  font-size:9px;
  font-weight:1000;
  padding:7px 9px;
  letter-spacing:1px
}

.product-info{
  padding:19px 5px 6px;
  display:flex;
  justify-content:space-between;
  gap:15px
}

.product h3{
  margin:0 0 7px;
  font-size:17px;
  letter-spacing:.2px
}

.product small{
  color:var(--muted)
}

.price{
  font-weight:1000;
  font-size:17px
}

.buy{
  margin-top:15px;
  width:100%;
  padding:14px;
  background:#111;
  color:#fff;
  border:0;
  font-weight:900;
  cursor:pointer;
  text-transform:uppercase;
  letter-spacing:1px
}

.buy:hover{
  background:var(--danger)
}

.size-label{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:12px;
  margin:8px 5px 0;
  font-size:9px;
  font-weight:900;
  letter-spacing:1.5px;
  color:#9a9a9a
}

.size{
  flex:1;
  appearance:none;
  background:#000;
  color:#fff;
  border:1px solid #333;
  border-radius:0;
  padding:13px 36px 13px 14px;
  font:900 11px "Trebuchet MS",Arial,sans-serif;
  letter-spacing:1px;
  cursor:pointer;
  background-image:
    linear-gradient(45deg,transparent 50%,#fff 50%),
    linear-gradient(135deg,#fff 50%,transparent 50%);
  background-position:
    calc(100% - 18px) 17px,
    calc(100% - 13px) 17px;
  background-size:5px 5px,5px 5px;
  background-repeat:no-repeat
}

.size:hover,
.size:focus{
  border-color:#fff;
  outline:none
}

.story{
  border-top:1px solid var(--line);
  border-bottom:1px solid var(--line);
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:90px
}

.story h2{
  font-size:56px;
  line-height:.9;
  font-family:Georgia,"Times New Roman",serif
}

.story p{
  color:var(--muted);
  line-height:1.9;
  font-size:15px
}

.manifesto{
  font-size:32px;
  font-weight:900;
  line-height:1.05
}

.manifesto span{color:var(--accent)}

.news{
  background:#050505;
  color:#fff;
  border-top:1px solid var(--line)
}

.news-inner{
  max-width:1280px;
  margin:auto;
  padding:65px 28px;
  display:flex;
  justify-content:space-between;
  gap:30px;
  align-items:center
}

.news h2{
  margin:0;
  font-size:38px;
  letter-spacing:-1.5px
}

.email{
  display:flex
}

.email input{
  background:#fff;
  color:#111;
  border:0;
  padding:16px;
  width:280px
}

.email button{
  border:0;
  background:var(--accent);
  color:#000;
  font-weight:1000;
  padding:0 20px;
  cursor:pointer
}

footer{
  max-width:1200px;
  margin:auto;
  padding:35px 24px;
  display:flex;
  justify-content:space-between;
  color:var(--muted);
  font-size:11px;
  text-transform:uppercase;
  letter-spacing:1px
}

.page-view{
  display:none
}

.page-view.active{
  display:block
}

.toast{
  position:fixed;
  bottom:22px;
  right:22px;
  background:var(--accent);
  color:#000;
  padding:14px 18px;
  font-weight:900;
  transform:translateY(100px);
  transition:.25s;
  z-index:50
}

.toast.show{
  transform:translateY(0)
}

.bag-panel{
  position:fixed;
  inset:0 0 0 auto;
  width:min(430px,100%);
  background:#050505;
  border-left:1px solid var(--line);
  z-index:40;
  transform:translateX(100%);
  transition:.25s;
  padding:28px;
  overflow:auto
}

.bag-panel.open{
  transform:translateX(0)
}

.bag-head{
  display:flex;
  justify-content:space-between;
  align-items:center;
  border-bottom:1px solid var(--line);
  padding-bottom:18px
}

.bag-head h3{
  margin:0;
  font-size:24px
}

.close{
  background:none;
  border:0;
  color:#fff;
  font-size:22px;
  cursor:pointer
}

.bag-item{
  display:flex;
  justify-content:space-between;
  gap:18px;
  padding:18px 0;
  border-bottom:1px solid var(--line);
  font-size:13px
}

.bag-total{
  display:flex;
  justify-content:space-between;
  font-weight:1000;
  font-size:18px;
  padding:22px 0
}

.checkout{
  display:block;
  width:100%;
  padding:16px;
  background:#fff;
  color:#000;
  text-align:center;
  text-decoration:none;
  border:0;
  font-weight:1000;
  text-transform:uppercase;
  letter-spacing:1.3px;
  cursor:pointer
}

.checkout-note{
  color:var(--muted);
  font-size:11px;
  line-height:1.6;
  margin-top:12px
}

.page-label{
  font-size:11px;
  font-weight:900;
  letter-spacing:2px;
  text-transform:uppercase;
  color:var(--muted)
}

.help-grid{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:16px
}

.help-card{
  border:1px solid var(--line);
  padding:25px;
  background:var(--panel)
}

.help-card h3{
  margin:0 0 10px;
  font-size:18px
}

.help-card p{
  color:var(--muted);
  line-height:1.6;
  font-size:14px
}

.faq{
  border-top:1px solid var(--line);
  margin-top:25px
}

.faq details{
  border-bottom:1px solid var(--line);
  padding:18px 0
}

.faq summary{
  font-weight:900;
  cursor:pointer
}

.faq p{
  color:var(--muted);
  line-height:1.6
}

.page-hero{
  max-width:1200px;
  margin:auto;
  padding:70px 24px 30px
}

.page-hero h2{
  font-size:clamp(48px,8vw,92px);
  letter-spacing:-5px;
  line-height:.85;
  margin:10px 0 20px
}

.about-copy{
  max-width:760px;
  color:var(--muted);
  font-size:18px;
  line-height:1.8
}

.contact-box{
  border:1px solid var(--line);
  padding:25px;
  margin-top:30px
}

@media(max-width:760px){
  nav{display:none}

  .hero{
    grid-template-columns:1fr;
    padding-top:55px
  }

  .hero h1{
    font-size:78px
  }

  .poster{
    max-width:480px
  }

  .grid,
  .story,
  .help-grid{
    grid-template-columns:1fr
  }

  .story{
    gap:20px
  }

  .news-inner{
    display:block
  }

  .email{
    margin-top:20px
  }

  .email input{
    width:100%
  }

  .section h2{
    font-size:35px
  }
}
</style>
</head>

<body>

<div id="app">

<header>
  <div class="nav">

    <div class="logo">
      MORTAL<span>ITY</span>
    </div>

    <nav>
      <a href="#home">Home</a>
      <a href="#apparel">Apparel</a>
      <a href="#about">About</a>
      <a href="#help">Help</a>
    </nav>

    <button class="cart" onclick="showCart()">
      BAG <span id="count">0</span>
    </button>

  </div>
</header>

<main>

<!-- HOME -->

<section class="hero page-view" id="home">

  <div>

    <h1>
      SHOP<br>
      "DROP 001"<br>
      NOW AVAILABLE<br>
      FOR PRE-ORDER
    </h1>

    <div class="buttons">
      <a class="btn primary" href="#apparel">
        SHOP NOW
      </a>
    </div>

  </div>

  <div class="poster">
    <div class="skull">☠</div>
    <div class="stamp">
      DROP 001 / PRE-ORDER
    </div>
  </div>

</section>


<!-- APPAREL -->

<section class="section page-view" id="apparel">

  <div class="section-head">

    <div>
      <div class="eyebrow">
        DROP 01 / THE STORE
      </div>

      <h2>APPAREL</h2>
    </div>

    <p>
      3 PIECES / LIMITED RUN
    </p>

  </div>

  <div class="grid">

    <!-- SHIRT 1 -->

    <article class="product">

      <div class="product-art">

        <div class="tag">
          DESIGN 01
        </div>

        <div class="shirt"></div>

      </div>

      <div class="product-info">

        <div>
          <h3>
            Mortality Core Tee
          </h3>

          <small>
            White / front graphic
          </small>
        </div>

        <div class="price">
          $30
        </div>

      </div>

      <label class="size-label">

        SIZE

        <select class="size">
          <option>Small</option>
          <option>Medium</option>
          <option>Large</option>
          <option>X Large</option>
        </select>

      </label>

      <button
        class="buy"
        onclick="add('Mortality Core Tee')">
        Add to bag
      </button>

    </article>


    <!-- SHIRT 2 -->

    <article class="product">

      <div class="product-art">

        <div class="tag">
          DESIGN 02
        </div>

        <div class="shirt two"></div>

      </div>

      <div class="product-info">

        <div>
          <h3>
            "MAKE YOUR MARK" Tee
          </h3>

          <small>
            White / graphic print
          </small>
        </div>

        <div class="price">
          $30
        </div>

      </div>

      <label class="size-label">

        SIZE

        <select class="size">
          <option>Small</option>
          <option>Medium</option>
          <option>Large</option>
          <option>X Large</option>
        </select>

      </label>

      <button
        class="buy"
        onclick="add('"MAKE YOUR MARK" Tee')">
        Add to bag
      </button>

    </article>


    <!-- STICKER PACK -->

    <article class="product">

      <div class="product-art">

        <div class="tag">
          ACCESSORY 01
        </div>

        <div style="font-size:86px;line-height:1">
          ☠
        </div>

      </div>

      <div class="product-info">

        <div>
          <h3>
            Mortality Sticker Pack
          </h3>

          <small>
            Sticker pack / assorted graphics
          </small>
        </div>

        <div class="price">
          $6
        </div>

      </div>

      <button
        class="buy"
        onclick="add('Mortality Sticker Pack')">
        Add to bag
      </button>

    </article>

  </div>

</section>


<!-- ABOUT -->

<section class="section story page-view" id="about">

  <div>

    <div class="eyebrow">
      THE BRAND
    </div>

    <h2>
      What is<br>
      mortality?
    </h2>

  </div>

  <div>

    <p class="manifesto">

      Founded by Enzo Battiato and Neev Bindra, the two were Driven by a desire to bring fresh, authentic designs to the skating community, the two friends combined their creative talents and relentless work ethic to build the brand Mortality skateboards from scratch.

      Through Mortality, Enzo and Neev continue to push boundaries, crafting high-quality decks and apparel that capture the raw, expressive spirit of modern skate culture.

    </p>

  </div>

</section>


<!-- HELP -->

<section class="section page-view" id="help">

  <div class="page-hero">

    <div class="eyebrow">
      NEED A HAND?
    </div>

    <h2>
      HELP
    </h2>

    <p class="about-copy">
      Questions about orders, sizing, shipping, or the next drop?
      Start here.
    </p>

  </div>


  <div class="help-grid">

    <div class="help-card">
      <h3>Orders</h3>
      <p>
        Need help with an order?
        Keep your order number handy and contact us for support.
      </p>
    </div>

    <div class="help-card">
      <h3>Sizing</h3>
      <p>
        Our tees are designed with a skate-inspired fit.
        A full size chart can be added here before launch.
      </p>
    </div>

    <div class="help-card">
      <h3>Shipping</h3>
      <p>
        Shipping details, delivery estimates, and tracking information
        will be listed here.
      </p>
    </div>

  </div>


  <div class="faq">

    <details>
      <summary>
        When will Drop 01 ship?
      </summary>

      <p>
        Shipping timing will be announced when the first production run is ready.
      </p>
    </details>


    <details>
      <summary>
        Can I return a shirt?
      </summary>

      <p>
        Return and exchange rules will be posted here before the store goes live.
      </p>
    </details>


    <details>
      <summary>
        How can I contact Mortality?
      </summary>

      <p>
        Use the contact information below and we'll get back to you.
      </p>
    </details>

  </div>


  <div class="contact-box">

    <strong>
      CONTACT
    </strong>

    <p>
      Questions, collaborations, or general help?
      Add your official Mortality email here before launch.
    </p>

  </div>

</section>


<!-- NEWSLETTER -->

<section class="news" id="newsletter">

  <div class="news-inner">

    <div>

      <div class="eyebrow">
        STAY IN THE LOOP
      </div>

      <h2>
        First to know. First to cop.
      </h2>

    </div>

    <form
      class="email"
      onsubmit="subscribe(event)">

      <input
        id="email"
        type="email"
        placeholder="your@email.com"
        required>

      <button>
        JOIN
      </button>

    </form>

  </div>

</section>

</main>


<!-- FOOTER -->

<footer>

  <span>
    © 2026 Mortality
  </span>

  <span>
    Independent skate apparel
  </span>

</footer>


<!-- BAG -->

<aside
  class="bag-panel"
  id="bagPanel">

  <div class="bag-head">

    <h3>
      YOUR BAG
    </h3>

    <button
      class="close"
      onclick="closeCart()">
      ×
    </button>

  </div>

  <div id="bagItems"></div>

  <div class="bag-total">

    <span>
      TOTAL
    </span>

    <span id="bagTotal">
      $0
    </span>

  </div>

  <a
    class="checkout"
    id="checkoutLink"
    href="#"
    onclick="startCheckout(event)">

    CHECKOUT

  </a>

  <div class="checkout-note">

    Drop 001 is a pre-order.
    Checkout can be connected to a $0-upfront payment link;
    payment providers charge transaction fees when an order is paid.

  </div>

</aside>


<div
  class="toast"
  id="toast">
</div>

</div>


<script>

let n = 0;

let bag = [];


/* PAGE NAVIGATION */

function setPage(page){

  document
    .querySelectorAll('.page-view')
    .forEach(el =>
      el.classList.remove('active')
    );

  const target =
    document.getElementById(page);

  if(target)
    target.classList.add('active');

  document
    .querySelectorAll('nav a')
    .forEach(a =>
      a.classList.toggle(
        'active',
        a.getAttribute('href') === '#' + page
      )
    );

  window.scrollTo(0,0);
}


function handlePage(){

  const page =
    location.hash.replace('#','') || 'home';

  setPage(
    ['home','apparel','about','help'].includes(page)
      ? page
      : 'home'
  );
}


window.addEventListener(
  'hashchange',
  handlePage
);

window.addEventListener(
  'DOMContentLoaded',
  handlePage
);


/* ADD TO BAG */

function add(name){

  const product = {

    name,

    price:
      name === 'Mortality Sticker Pack'
        ? 6
        : 30

  };


  let size = null;


  if(
    name.includes('Tee') ||
    name.includes('MARK')
  ){

    const selects =
      document.querySelectorAll('.size');

    size =
      selects[
        name.includes('MARK') ? 1 : 0
      ].value;

  }


  bag.push({
    ...product,
    size
  });


  n = bag.length;

  document.getElementById(
    'count'
  ).textContent = n;


  renderBag();

  document
    .getElementById('bagPanel')
    .classList.add('open');


  toast(
    name + ' added to bag'
  );

}


/* BAG */

function showCart(){

  renderBag();

  document
    .getElementById('bagPanel')
    .classList.add('open');

}


function closeCart(){

  document
    .getElementById('bagPanel')
    .classList.remove('open');

}


function renderBag(){

  const el =
    document.getElementById('bagItems');


  el.innerHTML = bag.length

    ? bag.map((item,i) =>

        '<div class="bag-item">' +

          '<div>' +

            '<strong>' +
              item.name +
            '</strong>' +

            (
              item.size
              ? '<br><small>Size: ' +
                item.size +
                '</small>'
              : ''
            ) +

          '</div>' +

          '<strong>$' +
            item.price +
          '</strong>' +

        '</div>'

      ).join('')

    : '<p style="color:var(--muted)">Your bag is empty.</p>';


  document.getElementById(
    'bagTotal'
  ).textContent =
    '$' +
    bag.reduce(
      (sum,item) =>
        sum + item.price,
      0
    );

}


/* CHECKOUT */

function startCheckout(e){

  e.preventDefault();


  if(!bag.length){

    toast(
      'Your bag is empty'
    );

    return;

  }


  const summary =
    bag.map(item =>
      item.name +
      (item.size
        ? ' / ' + item.size
        : '')
    ).join(', ');


  const total =
    bag.reduce(
      (sum,item) =>
        sum + item.price,
      0
    );


  /*
    PUT YOUR PAYMENT LINK HERE.

    Example:

    const checkoutUrl =
      'YOUR_PAYMENT_LINK';

  */

  const checkoutUrl =
    'YOUR_PAYMENT_LINK_HERE';


  if(
    checkoutUrl ===
    'YOUR_PAYMENT_LINK_HERE'
  ){

    toast(
      'Payment link needs to be connected'
    );

    return;

  }


  window.location.href =
    checkoutUrl;

}


/* EMAIL */

function subscribe(e){

  e.preventDefault();

  toast(
    "You're on the Mortality list."
  );

  e.target.reset();

}


/* NOTIFICATION */

function toast(msg){

  const t =
    document.getElementById('toast');

  t.textContent = msg;

  t.classList.add('show');

  setTimeout(
    () =>
      t.classList.remove('show'),
    2200
  );

}

</script>

</body>
</html>

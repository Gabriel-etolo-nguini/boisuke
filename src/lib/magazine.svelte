<script>
  import Cover from '../assets/1.png'

 import Logo from '../assets/logo.png'



	

</script>






  <div class="nav">

    <img src={Logo} class="logo" alt="Boisuke Logo" />
    
   
      
       <ul class="code">
    <li tabindex="0" class="digit">
      <span><a href="/">ABOUT.</a></span>
    </li>
    <li tabindex="0" class="digit">
      <span><a href="/">GALLERIE.</a></span>
    </li>
    <li tabindex="0" class="digit">
      <span><a href="/">CONTACT.</a></span>
    </li>
    
  </ul>

    </div>
   
 
  









<style>

.menu{
  display:flex;
}
.menu div{
  margin:20px;
  
}
.menu div a{
color:black;
}






  
  .nav{
    width: 100%;
    
    display:flex;
        align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  

  .navList{
    display:flex;
    color:black;
font-family:"kenyanReg";
font-size: x-large;
    align-items: flex-end;
  }
  h1, h2{
    margin:0;
  }

 
  
  

  .logo{
    height: 30rem !important;
    margin-top: 5rem;
  }












.code {
  font-size: 1rem;
  display: flex;
  flex-wrap: nowrap;
  color: black;
 
  justify-content: center;

}
@media (max-width: 768px) {

  .code {
  font-size: 1rem;
  display: flex;
  flex-wrap: nowrap;
  color: black;
  flex-direction: row;
 
  justify-content: center;

}
.digit {
  display: flex;
  height: 100%;
  padding: 3rem 1rem !important;
}

.digit span {
  scale: none !important;
  filter: drop-shadow(2px 4px 6px rgba(0,0,0,0.09)) !important;
  transition: none;
}




}

.code:hover {
  cursor: grab;
}

.digit {
  display: flex;
  height: 100%;
  padding: 5.5rem 3rem;
}

.digit:focus-visible {
  outline-color: hsl(0 0% 50% / 0.25);
  outline-offset: 1rem;
}

.digit span {
  scale: calc(var(--active, 0) + 0.5);
  filter: blur(calc((1 - var(--active, 0)) * 1rem));
  transition: scale calc(((1 - var(--active, 0)) + 0.2) * 1s), filter calc(((1 - var(--active, 0)) + 0.2) * 1s);
}
.digit span a{
  color:#c92e2a;
}

ul {
  padding: 0;
  margin: 0;
}



:root {
  --lerp-0: 1; /* === sin(90deg) */
  --lerp-1: calc(sin(50deg));
  --lerp-2: calc(sin(45deg));
  --lerp-3: calc(sin(35deg));
  --lerp-4: calc(sin(25deg));
  --lerp-5: calc(sin(15deg));
}

.digit:is(:hover, :focus-visible) {
  --active: var(--lerp-0);
}
.digit:is(:hover, :focus-visible) + .digit,
.digit:has(+ .digit:is(:hover, :focus-visible)) {
  --active: var(--lerp-1);
}
.digit:is(:hover, :focus-visible) + .digit + .digit,
.digit:has(+ .digit + .digit:is(:hover, :focus-visible)) {
  --active: var(--lerp-2);
}


 
</style>
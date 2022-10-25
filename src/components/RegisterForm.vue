<template>
  <div class="register-container box-shadow">
    <div class="register-wrapper ">
      <div class="register-header">
        <h3>Start your journey here.</h3>

      </div>
      <div class="register-content">
        <form class="register-input">
          <h3 class="underline">Hello there.</h3>
          <input type="text" class="input-txt" placeholder="EMAIL">
          <input type="password" class="input-txt" placeholder="PASSWORD">
          <input type="password" class="input-txt" placeholder="CONFIRM PASSWORD">
          <div class="input-group">
            <button type="submit" class="input-btn"><h3 style="width: auto;">Register</h3></button>
            <a class="a-cta" href="#"><h4>Terms and Conditions</h4></a>
          </div>

        </form>
        <div class="register-logo">
          <svg viewBox="0 0 61 61" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M27.6067 18.2707L25.1957 21.3649L38.4565 26.5219V25.4905V23.4277L37.251 21.3649L36.0455 19.3021L32.4289 17.2393L27.6067 18.2707Z" fill="#0ACF84"/>
            <path d="M24.4683 60.9964L28.1619 56.421C29.6227 56.3971 31.2023 56.2541 32.4968 55.6345C37.1168 53.4183 37.0574 48.259 37.0455 48.0326C37.0336 47.4368 36.9505 47.5083 33.6132 43.5762H43.0075C42.9837 49.5458 42.1405 51.7382 41.7961 52.5961C40.6797 55.4201 36.5823 60.079 30.4897 60.8654C29.4564 60.9964 26.5942 61.0084 24.4683 60.9964ZM48.2688 41.0144C52.8531 41.0144 55.2165 39.394 57.0217 37.3326L36.1785 37.2969L34.112 41.0264L48.2688 41.0144ZM43.0906 14.336V34.3895H34.3614L30.4778 41.0025H29.7058C23.4944 41.0025 22.8056 34.2704 22.7818 33.9844C22.6393 32.4116 20.2521 32.6022 20.3947 34.1989C20.5609 36.0815 21.4398 38.965 23.5301 41.0025H12.7225C9.69395 41.0025 -0.436694 37.8092 0.014612 27.4191V2.00366C0.014612 0.0972109 1.16663 0.025719 1.79608 0.00188831H11.5348C11.5586 0.00188831 11.5704 0.0138036 11.5942 0.0138036C12.1049 -0.0338577 17.5443 -0.236419 17.5443 5.2208C17.5443 6.80554 19.9434 6.81745 19.9434 5.2208C19.9434 3.05221 19.2901 1.31257 18.0669 0.0138036H28.0669C40.9766 -0.0338577 43.0906 9.47457 43.0906 14.336ZM27.3543 21.0086L34.9552 24.4998C36.5348 19.0783 29.9434 15.9565 27.3543 21.0086Z" fill="#1B1B1B"/>
          </svg>




        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RegisterForm',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>



.register-container {
  background: hsl(var(--con));
  border: 5px solid hsl(var(--txt));

  font-size: calc(var(--_size));
}


.register-wrapper > *{
  padding: 2rem;
}

.register-header{
  background: hsl(var(--accent));

  border-bottom: 5px solid hsl(var(--txt));
}

.register-input{
  display: flex;
  flex-direction: column;
  gap: 2em;
  padding-right: calc(var(--_size));
  border-right: 5px solid hsl(var(--txt));
}

.register-content{
  display: grid;
  grid-template-columns: 2fr 1fr;

}

.register-logo{
  padding-left: calc(var(--_size));
}

form{
  display: grid;
  gap: .8em;

  text-align: left;
  padding-block: .5em;

}



.input-btn{

}



.input-txt:-webkit-autofill{
  -webkit-text-fill-color: hsl(var(--accent-tertiary)) !important;
  font-size: calc(var(--_size))!important;
  font-family: 'JetBrains Mono', monospace !important;
}

.input-txt:-webkit-autofill::first-line{
  -webkit-box-shadow: 0 0 0 100vmax white inset !important;
  font-family: 'JetBrains Mono', monospace !important;
  text-transform: uppercase;
  font-size: calc(var(--_size)) !important;

 }


h3{
  width: fit-content;
}


#triangle{
  fill: hsl(var(--accent-secondary));
}

@media screen and (max-width: 700px) {


  .register-content {
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
    grid-auto-flow: row;
  }

  .register-logo * {
    display: none;
  }

  .register-input {
    padding-right: 0;
    border-right: none;
  }

  @media screen and (max-width: 420px){
    .input-group{
      grid-template-columns: 1fr;
      grid-template-rows: 1fr 1fr;

    }
  }
}


</style>

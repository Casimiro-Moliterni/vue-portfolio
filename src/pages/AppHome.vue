
  <script>
import Headers from '../components/Headers.vue';

  export default {
    name:"AppHome",
    components:{
        Headers
    },
    data() {
      return {
         social:[
          {
            name:'GitHub',
            url:'https://github.com/Casimiro-Moliterni',
            class:'fa-brands fa-github'

          },
          {
            name:'Linkedin',
            url:'https://www.linkedin.com/in/casimiro-moliterni-9a7322281/',
            class:'fa-brands fa-linkedin'
          },
         ]
      };
    },
    methods: {
    
    },
  };
  </script>
<template >
  <Headers></Headers>
 <section id="AppHome" class="pages" > 
   <div class="home-content container">
      <h1>Ciao, sono Casimiro Moliterni</h1>
      <h3>Junior Full Stack Web Developer</h3>
      <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sint porro illo non dolores molestias autem dicta! Numquam cumque vero corporis. Unde, fugiat. Iure voluptatem doloribus id ut omnis assumenda dignissimos!</p>
    
      <!-- container button  -->
      <div class="btn-box">
        <button>test 1</button>
        <button>test 2</button>
      </div>
      <!-- container social  -->
       <div class="home-social">
          <ul>
            <template v-for="link in social">
              <li>
                <a v-bind:href="link.url" target="_blank" >
                  <i :class="link.class"></i>
                </a>
              </li>
            </template>
          </ul>
       </div>
    </div>
 </section>
</template>
  
  <style scoped lang="scss">
     :root {
      --bg-color: #081b29;
      --second-bg-color: #112e42;
      --text-color: #ededed;
      --main-color: #00abf0;
  }
   .pages{
    height: 100vh;
   }
   #AppHome{
    background: #081b29;
    color: var(--text-color);
    height: 100vh;
    display: flex;
    align-items: center;
  /* inizio home content  */

    .home-content{
     color: white;
 
     h1{
       font-size: 56px;
       font-weight: 700;
       line-height: 1.2;
     }
     h3{
       font-size: 32px;
       font-weight: 700;
       color: #00abf0;
     }
     p{
       font-size: 16px;
       margin: 20px 0 40px;
     }
     
     /* btn  */
 
     .btn-box{
       width: 345px;
       height: 50px;
       display: flex;
       justify-content: space-between;
 
       button{
         position: relative;
         width: 150px;
         height: 100%;
         background-color:#00abf0 ;
         border: 2px solid #00abf0;
         border-radius: 8px;
         font-size: 19px;
         letter-spacing: 1px;
         font-weight: 600;
         color:#081b29;
         z-index: 1;
         overflow: hidden;
 
          &::before{
           content: '';
           position: absolute;
           height: 100%;
           width: 0;
           top: 0;
           left: 0;
           z-index: -1;
           background-color: #081b29;
           transition: 0.5s;
         }
         &:nth-child(2){
           background-color: transparent;
           color: #00abf0;
           &::before{
          background-color: #00abf0;
          }
          &:hover{
           color: #081b29;
          }
         }
 
         &:hover::before{
           width: 100%;
         }
         &:hover{
           color: #00abf0;
         }
       }
     }
    }
  /* fine home content  */

  /* inizio home social  */
   }
  </style>
  
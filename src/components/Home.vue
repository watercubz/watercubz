<template>
  <div class="header">
    <h1 class="title">Hi.</h1>
    <h3 class="name line anim-typewriter">
      My name is {{ name }} <span class="nick-name">{{ nickname }}.</span>
    </h3>

    <div class="description-div">
      <p class="description">
        I am a software developer with an interest in web development and with
        knowledge in
        <span v-for="(lang, index) in data.Langs" :key="index" class="text-highlight">
          {{ lang }} 
        </span>
        experience in frameworks
        <span v-for="(framework, index) in data.Frameworks" :key="index" class="text-highlight">
          {{ framework }} 
        
        </span>
      </p>
    </div>

    <div class="contact-me">
      <div class="logo-card">
        <a v-for="(social, index) in data.Socials" :key="index" class="social" target="_blank" :href="social.url" rel="noopener">
          {{ social.name }}
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {

  data() {
    return {
      data: {
        Socials: [
          { name: "Github", url: "https://github.com/watercubz" },
          { name: "Instagram", url: "https://www.instagram.com/watercubz" },
          { name: "Twitter", url: "https://twitter.com/watercubz" },
        ],
        Langs: ["Javascript"],
        Frameworks: ["Express", "Vue", "Firebase", "Nodejs"],
      },
      name: 'Eury Sosa Garcia',
      nickname: 'dev'
    };
  }
};
</script>
<style>
  @import url("https://fonts.googleapis.com/css2?family=Maven+Pro&display=swap");

  .header {
    display: flex;
    margin: 3rem;
    flex-direction: column;
  }

  .title {
   color:  #111827 ;
    font-size: 5rem;
  }

  .name {
    color:#454545;
    font-size: 2rem;
  }

  .nick-name {
    color: #454545;
  }

  .description-div {
    max-width: 900px;
  }

  .description {
    color: #454545;
    font-size: 1.5rem;
  }

  .text-highlight {
    color: #454545;
    font-size: 1.3rem;
    margin-right: 0.2rem;
    font-weight: 500;
  }

  .contact-me {
    margin-top: 30px;
  }

  .social {
    color: #8a817c;
    text-decoration: none;
    font-weight: 500;
    margin: 5px;
  }

  .social:hover {
    color: #ca9787;
    animation: ease-in 1s linear;
  }

  * {
    font-family: "Maven Pro", sans-serif;
    overflow-x: hidden;
  }

  .line {
    position: relative;
    top: 50%;
    width: 16em;
    border-right: 2px solid rgba(255, 255, 255, 0.75);
    font-size: 180%;
    text-align: left;
    white-space: nowrap;
    overflow: hidden;
    transform: translateY(-50%);
  }

  .anim-typewriter {
    animation: typewriter 4s steps(43) 1s 1 normal both,
      blinkTextCursor 700ms steps(43) infinite normal;
  }

  @keyframes typewriter {
    from {
      width: 0;
    }
    to {
      width: 15.3em;
    }
  }

  @keyframes blinkTextCursor {
    from {
      border-right-color: rgba(255, 255, 255, 0.75);
    }
    to {
      border-right-color: transparent;
    }
  }


  @media screen and (max-width: 667px ) {
    .header {
      margin: 0.5rem;
    }
    .title {
      font-size: 2rem;
    }
    .name {
      font-size: 1.5rem;
    }
    .description {
      font-size: 1rem;
    }
    .text-highlight {
      font-size: 1rem;
    }
  }
</style>

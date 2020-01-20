<template>
  <v-container>
    <v-layout
      text-center
      wrap
    >
      <v-flex xs12>
        <v-img
          :src="require('../assets/0.jpg')"
          class="my-3"
          contain
          height="200"
        ></v-img>
      </v-flex>

      <v-flex mb-4>
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to Yoni's website
        </h1>
        <p class="subheading font-weight-regular">
          Here's where I'll be sharing my latest completed work and keep you posted on my current projects
        </p>
      </v-flex>

      <v-flex
        mb-5
        xs12
      >
        <h2 class="headline font-weight-bold mb-3">I've recently completed 4 apps in Vue:</h2>

        <v-layout justify-center>
          <a
            v-for="(next, i) in completedVueProjects"
            :key="i"
            :href="next.href"
            class="subheading mx-4"
            target="_blank"
          >
            {{ next.text }}
          </a>
        </v-layout>
      </v-flex>
      <v-flex
        mb-5
        xs12
      >

      <h2 class="headline font-weight-bold mb-3">Several in React:</h2>

        <v-layout justify-center>
          <a
            v-for="(next, i) in completedReactProjects"
            :key="i"
            :href="next.href"
            class="subheading mx-4"
            target="_blank"
          >
            {{ next.text }}
          </a>
        </v-layout>
      </v-flex>
      <v-flex
        mb-5
        xs12
      >
        <h2 class="headline font-weight-bold mb-3">My Vanilla JS games</h2>

        <v-layout justify-center>
          <a
            v-for="(next, i) in completedJSProjects"
            :key="i"
            :href="next.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ next.text }}
          </a>
        </v-layout>
      </v-flex>

      <v-flex
        xs12
        mb-5
      >
        <h2 class="headline font-weight-bold mb-3">Important Links</h2>

        <v-layout justify-center>
          <a
            v-for="(link, i) in importantLinks"
            :key="i"
            :href="link.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ link.text }}
          </a>
        </v-layout>
      </v-flex>

      <v-flex
        xs12
        mb-5
      >
        <h2 class="headline font-weight-bold mb-3">Courrent Project</h2>
        <p>I'm currently developing a Full Stack project. Vue.js in the Front End and Express.js in the Back End</p>

        <v-layout justify-center>
          <a
            v-for="(eco, i) in currentProjects"
            :key="i"
            :href="eco.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ eco.text }}
          </a>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'HelloWorld',

  data: () => ({
    importantLinks: [
      {
        text: 'My LinkedIn Account',
        href: 'https://linkedin.com/in/jonathan-hirshowitz',
      },
      {
        text: 'My Github Account',
        href: 'https://github.com/yoniwitz',
      }
      ,
      {
        text: 'My Oracle Certified Associate, Java SE8 Programmer',
        href: 'https://www.youracclaim.com/badges/aa48e7ef-b267-4327-99e8-0f20bcc527b2',
      }
    ],
    completedVueProjects: [
      {
        text: 'Yoni\'s Waffles',
        href: 'https://yonis-waffles.firebaseapp.com/',
      },
      {
        text: 'Yoni Chat',
        href: 'https://yoni-chat.firebaseapp.com/',
      },
      {
        text: 'Programmers World Wide',
        href: 'https://ww-programmers.firebaseapp.com/',
      },
      {
        text: 'Expense Tracker (deployed on Heroku)',
        href: 'http://yw-expense-tracker.herokuapp.com/',
      },
    ],  
    completedReactProjects: [
      {
        text: 'Meme Generator',
        href: 'https://yoniwitz.github.io/Meme-Generator/',
      },
      {
        text: 'Expense Tracker (deployed on Heroku)',
        href: 'http://yw-expense-tracker-react.herokuapp.com/',
      }
    ],   
    completedJSProjects: [
      {
        text: 'Snake Game',
        href: 'https://yoniwitz.github.io/JS-Snake/',
      },
      {
        text: 'Tetris',
        href: 'https://yoniwitz.github.io/JS-Tetris/',
      },
    ]
  })
};
</script>

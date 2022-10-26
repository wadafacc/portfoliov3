<template>
  <div class="card">
    <div class="contents">
      <h2 class="title">hey {{ greeting() }}</h2>
      <div class="text">
        What you see here is probably the 6th attempt at actually finishing a
        portfolio page. And as you might've guessed, this one isn't finished
        either.
      </div>
      <div class="text">Here's some "useful" info about me:</div>
      <div class="stats">
        <ul>
          <li><i>"Fullstack"</i> dev</li>
          <li>
            Work @
            <a
              href="https://github.com/seiemens"
              target="_blank"
              rel="noopener noreferrer"
              >siemens</a
            >
          </li>
          <li>
            <a
              href="https://github.com/wadafacc"
              target="_blank"
              rel="noopener noreferrer"
              >Github maybe?</a
            >
          </li>
          <li>
            <a
              href="https://discord.com/users/286888695879958530"
              target="_blank"
              rel="noopener noreferrer"
              >Discord, why?</a
            >
          </li>
        </ul>
      </div>
      <div class="footer">
        jokes on you, an actual portfolio is in progress!
      </div>
    </div>
  </div>
</template>

<style src="~/assets/styles/hello.css">
</style>

<script>
export default {
  methods: {
    greeting() {
      const words = [
        "dipshit",
        "cunt",
        "lad",
        "mate",
        "%#*!",
        "friendly person",
      ];
      return words[Math.floor(Math.random() * words.length)];
    },
  },
};
</script>
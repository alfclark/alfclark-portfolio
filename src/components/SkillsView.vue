<template>
  <!-- Skills Section -->
  <div style="margin-top: -50px; position: absolute" id="skills"></div>
  <section class="container">
    <div class="skills">
      <h1 class="subtitle">
        My Top Skills
        <hr class="divider" />
      </h1>
      <div class="skills-wrapper">
        <img
          src="@/assets/javascript.svg"
          alt=""
          loading="lazy"
          class="icon icon-card"
        />
        <img
          src="@/assets/html5.svg"
          alt=""
          loading="lazy"
          class="icon icon-card"
        />
        <img
          src="@/assets/css3.svg"
          alt=""
          loading="lazy"
          class="icon icon-card"
        />
        <img
          src="@/assets/vue.svg"
          alt=""
          loading="lazy"
          class="icon icon-card"
        />
        <!--         <img
          src="@/assets/python.svg"
          alt=""
          loading="lazy"
          class="icon icon-card"
        /> -->
        <img
          src="@/assets/git.svg"
          alt=""
          loading="lazy"
          class="icon icon-card"
        />
        <img
          src="@/assets/bootstrap.svg"
          alt=""
          loading="lazy"
          class="icon icon-card"
        />
        <img
          src="@/assets/figma.svg"
          alt=""
          loading="lazy"
          class="icon icon-card"
        />
        <img
          src="@/assets/adobe_xd.svg"
          alt=""
          loading="lazy"
          class="icon icon-card"
        />
        <img
          src="@/assets/photoshop.svg"
          alt=""
          loading="lazy"
          class="icon icon-card"
        />
      </div>
    </div>
  </section>
</template>

<script></script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  width: 90vw;
  display: flex;
  align-items: center;
  justify-content: center;
}
.skills {
  width: 70vw;
  margin: 4rem 0;
  text-align: center;
}
.skill-header {
  margin-bottom: 1rem;
}
.skills-wrapper {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
.skills-wrapper img {
  padding: 1.25rem;
}
.icon {
  width: 10rem;
  height: 10rem;
}
.icon-card {
  background-color: #fff;
  border-radius: 11px;
  box-shadow: 0 10px 10px #783ad6;
  margin: 1rem;
  transition: 0.5s;
}
.icon-card:hover {
  animation: shake1 2s ease 0s 1 normal forwards;
  box-shadow: 0 0;
  border-color: #783ad6;
  border-style: solid;
  border-width: 5px;
  cursor: pointer;
}
@media screen and (max-width: 900px) {
  .icon {
    width: 5rem;
    height: 5rem;
  }
  .icon-card {
    margin: 0.5rem;
  }
  .skills-wrapper {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    padding: 0;
  }
}
</style>

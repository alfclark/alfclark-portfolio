<template>
  <div style="margin-top: -80px; position: absolute" id="projects"></div>
  <section class="container">
    <h1 class="subtitle">
      My Recent Projects
      <hr class="divider" />
    </h1>
    <div class="projects">
      <div class="projects-wrapper">
        <div
          class="project project-tile"
          :class="project.cardStatus"
          v-for="project in projects"
          :key="project.id"
          @click="toggle(project)"
        >
          <!-- Project Image -->
          <div class="img">
            <img
              class="project-image"
              :class="project.imgStatus"
              :src="project.img"
              :alt="project.name"
            />
            <div class="links" :class="project.linkStatus">
              <a class="link" target="blank" :href="project.live"
                ><i class="fa-solid fa-up-right-from-square _link"></i
              ></a>
              |
              <a class="link" target="blank" :href="project.git"
                ><i class="fa-brands fa-github _link"></i
              ></a>
            </div>
          </div>
          <div class="card-title">
            <p class="project-title">
              <span class="code">&lt;</span>
              {{ project.name }}
              <span class="code">&#47;&gt;</span>
            </p>
            <div class="technologies">
              <i
                class="fa-brands"
                v-for="technology in technologies"
                :key="technology.id"
                :class="technology.code"
              ></i>
              <i class="fa-brands api">{{ project.api }}</i>
            </div>
          </div>
        </div>
        <!-- Recycle -->
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      technologies: [
        { id: 0, name: "vue", code: "fa-brands fa-vuejs" },
        { id: 1, name: "js", code: "fa-brands fa-js" },
        { id: 2, name: "html", code: "fa-html5" },
        { id: 3, name: "css", code: "fa-brands fa-css3-alt" },
        { id: 4, name: "bootstrap", code: "fa-brands fa-bootstrap" },
      ],
      projects: [
        {
          id: 0,
          name: "E-Commerce Website",
          img: "/projects/GeekCave.png",
          state: false,
          cardStatus: "",
          imgStatus: "",
          linkStatus: "",
          git: "https://github.com/alfclark/ecommerce-site",
          live: "https://vueecommerce-site.netlify.app/",
        },
        {
          id: 1,
          name: "MovieZone",
          img: "/projects/movieZone.png",
          state: false,
          cardStatus: "",
          imgStatus: "",
          linkStatus: "",
          git: "https://github.com/alfclark/movie-app",
          live: "https://is-the-movie-zone.netlify.app/",
          api: "API",
        },
        {
          id: 2,
          name: "GameZone",
          img: "/projects/GameZone.png",
          state: false,
          cardStatus: "",
          imgStatus: "",
          linkStatus: "",
          git: "https://github.com/alfclark/game-zone",
          live: "https://alfclark-gamezone.netlify.app/",
        },
        {
          id: 3,
          name: "Etch-a-Sketch",
          img: "/projects/etchASketch.png",
          state: false,
          cardStatus: "",
          imgStatus: "",
          linkStatus: "",
          git: "https://github.com/alfclark/Etch-a-Sketch",
          live: "https://beautiful-elf-1f56ad.netlify.app/",
        },
        {
          id: 4,
          name: "Text Encryption",
          img: "/projects/encryptionPage.png",
          state: false,
          cardStatus: "",
          imgStatus: "",
          linkStatus: "",
          git: "https://github.com/alfclark/alura-challenge1",
          live: "https://alura-challenge1.netlify.app/",
          api: "API",
        },
        {
          id: 5,
          name: "To-Do List",
          img: "/projects/toDoList.png",
          state: false,
          cardStatus: "",
          imgStatus: "",
          linkStatus: "",
          git: "https://github.com/alfclark/todo-list-VueJS",
          live: "https://teal-unicorn-7b0316.netlify.app/",
        },
      ],
    };
  },
  methods: {
    toggle(project) {
      project.state = !project.state;
      if (project.state === true) {
        project.cardStatus = "cardSelected";
        project.imgStatus = "imgSelected";
        project.linkStatus = "linkShow";
      } else {
        project.cardStatus = "";
        project.imgStatus = "";
        project.linkStatus = "";
      }
    },
  },
};
</script>

<style scoped>
.container {
  width: 90vw;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 4rem;
}
.projects {
  width: 80vw;
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: center;
}
.projects-wrapper {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  width: 80vw;
}
.container {
  width: 90vw;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 4rem;
}
.projects {
  width: 80vw;
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: center;
}
.projects-wrapper {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  width: 80vw;
}
.project {
  background: #783ad6;
  border-radius: 11px;
  transition: 0.3s;
  text-decoration: none;
  width: 20rem;
  height: 25rem;
  cursor: pointer;
  margin: 2rem;
}
.project:hover {
  background-color: #141c3a;
}
.img {
  height: 90%;
  margin: 0;
  padding: 0;
}
.project-image {
  object-fit: cover;
  width: 100%;
  border-radius: 11px 11px 0 0;
  height: 90%;
}
.links {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  display: flex;
  width: 5rem;
  justify-content: space-around;
  gap: 2rem;
  font-size: 2rem;
  display: none;
}
.link {
  color: white;
}
.link:hover {
  color: var(--dark);
  transition: 0.4s;
}
.card-title {
  margin-top: -1.2rem;
  padding: 0;
}
.project-title {
  font-size: 1rem;
  font-weight: 400;
  text-decoration: none;
  margin: 0;
}
.code {
  color: transparent;
  transition: color 0.3s ease-out;
}
.project:hover .code {
  color: #ff7f50;
  text-decoration: underline;
}
.technologies {
  display: flex;
  gap: 0.5rem;
  align-items: center;
  justify-content: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
.technologies .fa-brands {
  margin-top: 0.5rem;
  color: white;
  font-size: 1.3rem;
}
.project:hover .project-title {
  color: #ff7f50;
  text-decoration: underline;
}
.project:hover .technologies .fa-brands {
  color: #ff7f50;
}
.api {
  font-family: Roboto, Helvetica, Arial, sans-serif;
}
.cardSelected {
  transform: scale(1.05);
}
.imgSelected {
  opacity: 30%;
  transition: 0.4s;
}
.linkShow {
  display: flex;
  transition: 0.4s;
}
@media screen and (max-width: 900px) {
  .projects {
    width: 95vw;
  }
  .projects-wrapper {
    width: 95vw;
  }
  .project {
    width: 10rem;
    height: 15rem;
    margin: 0.7rem;
  }
  .project-title {
    font-size: 0.7rem;
  }
  .technologies .fa-brands {
    font-size: 0.7rem;
  }
  ._link {
    font-size: 1.3rem;
  }
}
</style>

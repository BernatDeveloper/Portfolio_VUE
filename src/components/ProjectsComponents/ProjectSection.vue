<template>
  <section id="projects" class="projects">
      <h2>My Projects</h2>
      <div class="container project-list d-flex flex-wrap justify-content-center">
        <ProjectCard 
          v-for="project in projects" 
          :key="project.id" 
          :title="project.title" 
          :description="project.description" 
          :img="project.img"
          :url="project.url"
        />
      </div>
    </section>
  </template>
  
  <script setup>
  import ProjectCard from './ProjectCard.vue';
  import { ref } from 'vue';
  
  const projects = ref([
    {
      id: 1,
      title: "Events App",
      description: "EventsApp es una plataforma web para la gestión completa de eventos, permitiendo invitar a otros usuarios y organizar todos los detalles desde un solo lugar. El proyecto está construido con React, Laravel, React Toolkit, Tailwind CSS y Leaflet para la integración de mapas.",
      img: require("@/assets/images/EventsApp.jpg"),
      url: "https://eventos-app.vercel.app/"
    },
    {
      id: 2,
      title: "React components",
      description: "Explora una colección de componentes personalizables para React. Cada componente incluye ejemplos interactivos, código JSX y estilos CSS, diseñados para facilitar el desarrollo de tus aplicaciones web.",
      img: require("@/assets/images/ReactComponentsImg.avif"),
      url: "https://components-react-storage.vercel.app/"
    },
    {
      id: 3,
      title: "Mis Notas",
      description: "Esta es una aplicación web donde los usuarios pueden registrarse, crear notas, gestionarlas y organizarlas según su estado. Además, cuenta con un perfil donde los ususrios pueden manejar diferentes ajusted personalizados.",
      img: require("@/assets/images/MisNotasImg.avif"),
      url: "https://github.com/BernatDev6/Todo_React_Laravel"
    },
    {
      id: 4,
      title: "Comming soon...",
      description: "This is the third project, featuring a responsive layout.",
      img: "https://picsum.photos/id/36/300",
      url: "#"
    }
  ]);
  </script>
  
  <style scoped lang="scss">
  .projects {
    color: var(--text-color);
    background-color: var(--bg-secondary-color);
    padding: var(--large-spacing) 0;

    .project-list {
      display: flex;
      flex-wrap: wrap;
      gap: calc(var(--large-spacing) * 1.5);
    }
  }
  </style>
  
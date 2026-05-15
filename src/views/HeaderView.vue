<template>
  <header>
    <div class="title">
      <h1>SkillForge</h1>
    </div>

    <nav>
      <RouterLink to="/">Início</RouterLink>
      <RouterLink to="/">Recursos</RouterLink>
      <RouterLink to="/">Projetos</RouterLink>
      <RouterLink to="/">Preços</RouterLink>
      <RouterLink to="/">Depoimentos</RouterLink>
      <RouterLink to="/">FAQ</RouterLink>
    </nav>

    <button class="buttons">Começar agora</button>
  </header>
</template>

<style>
header {
  /* max-width: 80rem; */
  width: 100%;
  padding: 1rem 2rem;
  margin-inline: auto;

  display: flex;
  align-items: center;
  justify-content: space-between;

  background-color: rgba(8, 20, 37, 0.8);
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
  box-shadow: 0px 4px 20px rgba(109, 59, 215, 0.15);
  backdrop-filter: blur(6px);

  & h1 {
    font-family: "Inter", sans-serif;
    font-size: 2rem;
    font-weight: 700;
    color: #d0bcff;
    line-height: 2.625rem;
    letter-spacing: -0.08px;
  }

  & nav {
    display: flex;
    align-items: center;
    gap: 2rem;

    & a {
      font-family: "Inter", sans-serif;
      font-size: 1rem;
      line-height: 25.6px;
      text-decoration: none;
      color: #cbc3d7;

      width: fit-content;
      position: relative;

      transition:
        transform 200ms ease,
        color 200ms ease;

      &:hover {
        color: #d0bcff;
        /* font-weight: 700; */
        transform: scale(1.08);
      }

      &:hover::after {
        opacity: 1;
        transform: scaleX(1);
      }
    }

    & a::after {
      content: "";
      width: 100%;
      height: 2px;
      background-color: #d0bcff;

      position: absolute;
      bottom: 0;
      left: 0;
      opacity: 0;
      transform: scaleX(0);
      transition: transform 200ms linear;
    }
  }

  & .buttons {
    display: flex;
    align-items: center;
    justify-content: center;

    padding: 0.625rem 1.5rem;
    border-radius: 9999px;

    font-family: "Inter", sans-serif;
    font-size: 1rem;
    font-weight: 700;
    line-height: 24px;
    color: #340080;

    background: linear-gradient(90deg, #a078ff 0%, #6d3bd7 100%);
    /* box-shadow: X  Y  blur  spread  cor; */
    box-shadow: 0px 0px 20px rgba(208, 188, 255, 0.2);

    border: none;
    cursor: pointer;
  }
}

/* @media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
} */
</style>

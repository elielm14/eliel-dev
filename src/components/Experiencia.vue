<template>
  <div class="sectionInicial">

    <section class="conteudoInicial">

      <img src="https://avatars.githubusercontent.com/u/79880373?v=4" alt="Foto de Perfil" class="fotoPerfil">

      <div class="linhaCor">

        <p class="textoFront">Desenvolvedor Front End</p>

        <p class="textoLocalizacao">Localizado em Ananindeu-PA</p>

      </div>

    </section>

    <section class="textoExperiencia">

      <h2 id="experincia" class="experincia">Experiência</h2>

      <p class="textoP">Desenvolvo projetos utlizando <strong>Vue.Js,</strong> <strong>React.Js</strong> e
        utlizando apenas
        <strong>HTML, CSS e JavaScript</strong>. Sólida experiência com consumo de <strong>API REST</strong>,
        responsividade mobile first e versionamento de código com <strong>Git e GitHub</strong>.
      </p>

    </section>

    <section class="containerProjeto">
      <Projeto />
    </section>
  </div>

</template>

<script>
import Projeto from './Projeto.vue';

export default {
  name: "ExperienciaSection",
  components: { Projeto }
}
</script>

<style scoped>
.sectionInicial {
  background: var(--cor-branco-gelo);
}

.conteudoInicial {
  display: grid;
  grid-template-columns: 2fr 3fr;
  gap: 10px;
  margin: 0 1em 2em 1em;
}

.fotoPerfil {
  border-radius: 50%;
  display: block;
  padding: 1em 0;
  width: 8em;
}

.linhaCor {
  border-left: 5px solid var(--cor-linhas);
  padding-left: 0.3em;
}

.textoFront {
  font-size: 1.4rem;
  font-weight: bold;
}

.textoLocalizacao {
  font-size: 1.22rem;
}

.textoExperiencia {
  margin: 1em 1.5em;
  font-size: 1.12rem;
  line-height: normal;
}

.experincia {
  font-size: 2em;
  font-weight: bold;
  padding: .5em 0;
}

.textoP {
  line-height: 1.5;
  border-left: 5px solid var(--cor-linhas);
  padding-left: 0.3em;
}

.containerProjeto {
  max-width: 1200px;
  padding: 40px 20px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr;
  gap: 30px;
}

@media only screen and (min-width: 1024px) {
  .conteudoInicial {
    padding-top: 2em;
    margin: 0 auto;
    max-width: var(--margem);
    grid-template-columns: 1fr 2fr;
  }

  .linhaCor {
    margin-left: 0;
  }

  .experincia, .textoP {
    max-width: var(--margem);
  }
  .containerProjeto{
    max-width: 50%;
  }
}
</style>
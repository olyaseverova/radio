<template>
  <div id="app" class="home">
    <h1 class="main-h1 up">Дубрава-радио онлайн</h1>
    <h3 class="main-h3">Приветствуем Вас на портале «Дубрава-радио онлайн».</h3>
    <p class="main-text">
      Ежедневно и круглосуточно здесь звучит музыка, которую мы создаём и
      исполняем для Вас, ценителей живого и настоящего искусства. Русская
      современная авторская музыка, обработки шедевров русской и мировой
      классики, современный фольклор и классический джаз.
    </p>
    <img class="home__img" src="@/img/main.jpg" alt="Логотип" />
    <ul class="audios-list list">
      <li class="audios-list__item" v-for="audio in audios" :key="audio.id">
        <p class="audios-list__title">{{ audio.title }}</p>
        <audio controls :src="audio.src"></audio>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      audios: [
        {
          src: "http://89.22.156.37:8000/mpd.128",
          title: "Arimoia Trio - ГђВ§ГђВµГђВ»ГђВѕГђВІГђВµГђВє",
        },
        {
          src: "http://89.22.156.37:8000/mpd.320",
          title: "Arimoia Trio - Ð§ÐµÐ»Ð¾Ð²ÐµÐº",
        },
        {
          src: "http://89.22.156.37:8000/mpd.64",
          title: "Arimoia Trio - ├Р┬з├Р┬╡├Р┬╗├Р┬╛├Р┬▓├Р┬╡├Р┬║",
        },
        {
          src: "http://89.22.156.37:8000/mpd.ogg",
          title: "Arimoia Trio - Человек",
        },
      ],
    };
  },
};
</script>


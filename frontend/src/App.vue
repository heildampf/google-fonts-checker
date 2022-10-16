<template>

<div class="top">
    <router-view/>
    <header role="navigation">
      <div><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAIAAAACACAMAAAD04JH5AAACWFBMVEX///8AAAAaFxsjnNOl1+0/qdn+/v7My8z6+vo4Njn///+Bf4H///9ycHP9/f38/PzGxcawr7HIx8gfHCD5+fl/fX+tq63///////////////8yLzP////4+PiHhojx8fHc3Nz///8bGBw0MjX09PTu7e5KR0pRT1L7+/scGR24t7j///////8dGh7R0dFFQ0ZYVlmcm53Y2NlPTVB6eXtiYGKenZ8kISX29vZ9e33l5eXs7Ozv7++NjI6TkZP///////9fXWD////////j4+P///////////////9oZmlIRUkmIye9vL3///9APkHm5uYoJSk7OTwhHiJDQUR0cnSVk5XX1tfo6OhlY2YzMDRvbW94dnlcWl2ZmJre3d7y8vJraWu6ubrg3+B1c3YlndOXlpdMSk2rqqvT0tMiHyMwLTD////V1NXq6urd7/g+Oz6ura/KysulpKaysbLBwMHa2drz8/NaV1q/vr////9VU1bm8/q1tbbCwsNUUVQ3NDi0s7Qpn9SJiIrJyMnPzs////+npqj////////////////////////////Nzc6PjY/////x+fz///8xotb///////////+joaMtKi7///+MiowtodVDqtns9/v3+/2Fg4WRkJLh4eGAfoCg1OwtKy8rKCuDgYNIrdrFxMXK5/Rsam2pqKlQsNyp2O7X7fegn6G43/HN6PW/4vJkueBzwOOTz+pXs92EyObR6vY8p9iIyedguN9qvOFdtt+NzOjF5fPi8vl/xeay3PCZ0epxvuNNr9s1pdd6w+RKCp0GAAAAyHRSTlP/AP///////////v8C/////////////xH7mNT/4P////+c////////////VlP////////////////////////O5v/xCP81KAr2/////8H//////////////////////////////////////y7/////////////////oP//////////////ef+yT14f2r5t///r/zr/D2MV//+1/////////////////////////////////////////////////////////////6U+CEMAAA4tSURBVHiczZuHXxNJG8eH4W4JLUESgigphIQeogQ0FMEoigjSBaUX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" alt="Logo Sartoris Datenschutz"> Google Fonts Checker </div>
      <div class="right">
        <SwitchLanguage/>
        <a href="https://github.com/54GradSoftware/google-fonts-checker/" target="_blank" rel="noreferrer" class="github" :aria-label="$t('header.linkToGithubAlt')">
          <img src="./assets/GitHub-Mark-Light-64px.png" alt="Logo GitHub">
        </a>
      </div>
    </header>
  </div>
  <footer>
    {{ $t('footer.poweredby', {icon: '&#9874;'}) }} |
    <a href="https://www.dsb-datenschutz.de/impressum.html" target="_blank" rel="noreferrer">{{ $t('footer.imprint') }}</a> |
    <a href="https://www.dsb-datenschutz.de/datenschutzerklaerung.html" target="_blank" rel="noreferrer">{{ $t('footer.privacyNotice') }}</a> |
    {{ $t('footer.madeWithLove', {icon: '&#9829;'}) }}
    <a href="https://54gradsoftware.de" target="_blank" rel="noreferrer">54 Grad Software</a>
  </footer>
</template>

<script setup>
import SwitchLanguage from '@/components/SwitchLanguage.vue';
import { watch } from 'vue';
import { useRoute } from 'vue-router';
import { useI18n } from 'vue-i18n';

const route = useRoute();
const i18n = useI18n();

watch(() => route.params.locale, locale => {
  i18n.locale._setter(locale.toString());
});

</script>

<style lang="scss">
html, body{
  height: 100%;
  margin: 0;
}
#app {
  display: flex;
  flex-flow: column;
  justify-content: space-between;
  min-height: 100%;
  font-family: system-ui, sans-serif;
  line-height: 1.4;
  .top{
    header{
      padding: 1rem;
      box-sizing: border-box;
      background-color: #0E57AA;
      color: #fff;
      font-weight: bold;
      font-size: 1.2rem;
      position: fixed;
      top: 0;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      min-height: 4rem;
      .right{
        display: flex;
        flex-flow: row;
        align-items: center;
        .github{
          width: 2rem;
          height: 2rem;
          display: flex;
          margin-left: 1rem;
        }
      }
    }
  }
  footer{
    padding: 1rem;
    background-color: #222;
    color: #fff;
    a{
      color: #fff;
    }
  }
  .button{
    padding: 1rem;
    background-color: #0E57AA;
    border: 1px #0E57AA solid;
    color: #fff;
    border-radius: 0.5rem;
    width: fit-content;
    cursor: pointer;
    display: block;
    text-decoration: none;
    margin: auto;
  }
}
.visually-hidden {
  position: absolute !important;
  width: 1px !important;
  height: 1px !important;
  padding: 0 !important;
  margin: -1px !important; // Fix for https://github.com/twbs/bootstrap/issues/25686
  overflow: hidden !important;
  clip: rect(0, 0, 0, 0) !important;
  white-space: nowrap !important;
  border: 0 !important;
}
</style>

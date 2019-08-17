<style src="./AppFooter.scss" module lang="scss"></style>
<script src="./AppFooter.js"></script>

<template>
  <div :class="[$style.appFooter, 'wrapper', 'skewed-section', 'reversed', scrollId]">
    <div :class="['background']">
      <div :class="['background-inner']"
           :style="{backgroundColor: $colors.colorGreen}"
           ref="background">
      </div>
    </div>
      <div :class="[$style.navigation, 'content-wrapper']">
          <span :class="$style.logo" v-html="require('~/assets/svg/logo.svg')"></span>
          
          <div :class="$style.footerItems">
            <h2 class="heading-02">Exploreren</h2>
            <nuxt-link class="copy-01" :to="{name: 'index'}">Home</nuxt-link>
            <nuxt-link class="copy-01" :to="{name: 'about-us'}">Over Ons</nuxt-link>
            <nuxt-link class="copy-01" :to="{name: 'terms'}">Actievoorwaarden</nuxt-link>
          </div>

          <div :class="$style.footerItems">
            <h2 class="heading-02">Doe mee</h2>
            <nuxt-link class="copy-01" :to="{name: 'submission'}">Doe mee</nuxt-link>
          </div>

          <div :class="$style.footerItems">
            <h2 class="heading-02">Contactgegevens</h2>
            <a class="copy-01" :href="item.url" v-for="(item, index) in contactUs" :key="index">{{item.name}}</a>
          </div>
          
          <div :class="$style.footerItems">
            <h2 class="heading-02">Volg ons</h2>
              <a class="copy-01" href="#" v-for="(item, index) in followUs" :key="index">{{item.name}}</a>
          </div>
        </div>
        
      </div>
  </div>
</template>

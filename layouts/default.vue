<template>
  <div>
    <nav
      class="navbar header has-shadow is-primary"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="navbar-brand">
        <a class="navbar-item" href="/">
          <img src="~assets/buefy.png" alt="Buefy" height="28" />
        </a>

        <div class="navbar-burger">
          <span />
          <span />
          <span />
        </div>
      </div>
    </nav>

    <section class="main-content columns">
      <aside class="column is-2 section">
        <p class="menu-label is-hidden-touch">General</p>
        <ul class="menu-list">
          <li v-for="(item, key) of items" :key="key">
            <nuxt-link :to="item.to" exact-active-class="is-active">
              <b-icon :icon="item.icon" />
              {{ item.title }}
            </nuxt-link>
          </li>
        </ul>
      </aside>

      <div class="container column is-10">
        <nuxt />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        }
      ]
    }
  },
  head() {
    return {
      meta: [
        {
          hid: 'og:image',
          property: 'og:image',
          content: 'https://ellanskii.github.io/Rabota.ru-sandbox/ogimage2.png'
        },
        {
          hid: 'vk:image',
          property: 'vk:image',
          content: 'https://ellanskii.github.io/Rabota.ru-sandbox/vkimage2.png'
        },
        {
          hid: 'tw:image',
          property: 'tw:image',
          content: 'https://ellanskii.github.io/Rabota.ru-sandbox/twimage2.png'
        },
        {
          hid: 'og:image:width',
          property: 'og:image:width',
          content: '1200'
        },
        {
          hid: 'og:image:height',
          property: 'og:image:height',
          content: '624'
        }
      ]
    }
  }
}
</script>

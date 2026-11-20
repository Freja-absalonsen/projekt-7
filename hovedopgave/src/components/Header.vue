<!--Inspiration fra sidste eksamensprojekt-->
<!--Samtale med chat: https://chatgpt.com/share/6a15622f-58c8-83eb-b9bd-aff5afed1a52 -->

<script setup>
import { ref } from 'vue'

const open = ref(false)
const openItem = ref(null)

const toggle = () => {
  open.value = !open.value
  openItem.value = null
}

const toggleItem = (name) => {
  openItem.value = openItem.value === name ? null : name
}
</script>

<template>
  <header class="header">
    <div class="header__logo">
      <RouterLink :to="{ name: 'home' }">
        <img src="../assets/logo.png" alt="Logo." height="50" width="auto">
      </RouterLink>
    </div>

    <button
      class="header__button"
      :aria-expanded="open.toString()"
      :aria-label="open ? 'Luk menu' : 'Åben menu'"
      aria-controls="header__primary-navigation"
      @click="toggle"
    >
      <span class="header__burger-line" :class="{ open }"></span>
      <span class="header__burger-line" :class="{ open }"></span>
      <span class="header__burger-line" :class="{ open }"></span>
    </button>

    <div class="header__menu-wrapper">
      <nav id="header__primary-navigation" class="header__menu" :class="{ open }">
        <ul>
          <li>
            <button class="header__item" :aria-expanded="openItem === 'elev'" @click="toggleItem('elev')">Bliv elev</button>
            <ul v-show="openItem === 'elev'" class="header__submenu">
                <li>
                    <span class="header__heading">Nye elever</span>
                    <ul>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Ledige pladser</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Brochure</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">En dag på Broby</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Pakkeliste</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Videorundvisning</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Besøgsdage - Få en rundvisning mm.</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Efterskolernes dag - Åbent hus</RouterLink></li>
                    </ul>
                </li>
                <li>
                    <span class="header__heading">For forældre</span>
                    <ul>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Økonomi</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Ikke "bare" lærere</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Bestyrelse</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Karakterer</RouterLink></li>
                    </ul>
                </li>
            </ul>
          </li>

          <li>
            <button class="header__item" :aria-expanded="openItem === 'sport'" @click="toggleItem('sport')">Sportsfag</button>
            <ul v-show="openItem === 'sport'" class="header__submenu">
              <li><RouterLink :to="{ name: '' }" @click="toggle">Drengefodbold</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Pigefodbold</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Håndbold</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Spinning</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Fitness</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Styrketræning</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Svømning</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Beachvolley</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Surf & Kite</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Gymnastik</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Mountainbike</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Spring</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Dans</RouterLink></li>
            </ul>
          </li>

          <li>
            <button class="header__item" :aria-expanded="openItem === 'livet'" @click="toggleItem('livet')">Livet på Broby</button>
            <ul v-show="openItem === 'livet'" class="header__submenu">
                <li>
                    <span class="header__heading">Dagligdagen</span>
                    <ul>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Sådan bor vi</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Fritid</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Aftenfester</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Maden på Broby</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Ikke "bare" lærere</RouterLink></li>
                    </ul>
                </li>
                <li>
                    <span class="header__heading">Undervisning</span>
                    <ul>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Valgfag</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Kursusfag</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Fællesfag</RouterLink></li>
                    </ul>
                </li>
                <li>
                    <span class="header__heading">Årets gang</span>
                    <ul>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Studieture</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Årets aktiviteter</RouterLink></li>
                    </ul>
                </li>
            </ul>
          </li>

          <li>
            <button class="header__item" :aria-expanded="openItem === 'undervisning'" @click="toggleItem('undervisning')">Undervisning</button>
            <ul v-show="openItem === 'undervisning'" class="header__submenu">
              <li><RouterLink :to="{ name: '' }" @click="toggle">Valgfag</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Kursusfag</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Fællesfag</RouterLink></li>
            </ul>
          </li>

          <li>
            <button class="header__item" :aria-expanded="openItem === 'skolen'" @click="toggleItem('skolen')">Om skolen</button>
            <ul v-show="openItem === 'skolen'" class="header__submenu">
                <li>
                    <span class="header__heading">Om Broby Sportsefterskole</span>
                    <ul>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Bestyrelse</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Lærerne</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Værdigrundlag</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Vedtægter</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Skolekredsen</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Nyhedsbrev</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Årsplan</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Indholdsplan</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Undervisningsmiljø</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Evaluering</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Fødevarekontrol</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Persondatapolitik</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Politik om brug af sociale medier</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Skoletal</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Trivsels og mobbestrategi</RouterLink></li>
                    </ul>
                </li>
                <li>
                    <span class="header__heading">Gamle elever</span>
                    <ul>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Gammel elevdag</RouterLink></li>
                        <li><RouterLink :to="{ name: '' }" @click="toggle">Elevforeningen</RouterLink></li>
                    </ul>
                </li>
            </ul>
          </li>

          <li>
            <button class="header__item" :aria-expanded="openItem === 'kontakt'" @click="toggleItem('kontakt')">Kontakt</button>
            <ul v-show="openItem === 'kontakt'" class="header__submenu">
              <li><RouterLink :to="{ name: '' }" @click="toggle">Stillingsopslag</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Lærerne</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Kontor</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Køkken</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Teknisk personale</RouterLink></li>
              <li><RouterLink :to="{ name: '' }" @click="toggle">Presse</RouterLink></li>
            </ul>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>
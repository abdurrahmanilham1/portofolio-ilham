<template>
  <b-container fluid>
    <b-row>
      <b-button @click="showMenu = !showMenu" class="tombol-menu" size="sm"
        >toggle menu</b-button
      >
      <b-col cols="3" class="side-menu" :class="showMenu ? 'show' : 'hidden'">
        <img class="foto-profil mt-4" src="../assets/ilham2.jpeg" alt="" />
        <div class="nama mt-3">M Abdurrahman Ilham</div>
        <div id="ikon-sosmed" class="mt-3 mb-5">
          <a
            href="https://twitter.com/jokowi?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor"
          >
            <b-avatar icon="twitter" class="sosmed"></b-avatar>
          </a>
          <a href="https://id-id.facebook.com/ahmad.ilham.7587">
            <b-avatar icon="facebook" class="sosmed"></b-avatar>
          </a>
          <a href="https://www.instagram.com/iam.bedur17/?hl=id">
            <b-avatar icon="instagram" class="sosmed"></b-avatar>
          </a>
          <a
            href="https://id.linkedin.com/?trk=guest_homepage-basic_nav-header-logo"
          >
            <b-avatar icon="linkedin" class="sosmed"></b-avatar>
          </a>
          <a href="https://www.youtube.com/watch?v=l-GVTRXT9GA">
            <b-avatar icon="youtube" class="sosmed"></b-avatar>
          </a>
        </div>
        <b-container class="bungkus-navigasi mb-5">
          <div
            @click="index = 0"
            :class="index === 0 ? 'item-navigasi selected' : 'item-navigasi'"
          >
            <b-icon-house /> home
          </div>
          <div
            @click="index = 1"
            :class="index === 1 ? 'item-navigasi selected' : 'item-navigasi'"
          >
            <b-icon-person /> about
          </div>
          <div
            @click="index = 2"
            :class="index === 2 ? 'item-navigasi selected' : 'item-navigasi'"
          >
            <b-icon-file-earmark /> resume
          </div>
          <div
            @click="index = 3"
            :class="index === 3 ? 'item-navigasi selected' : 'item-navigasi'"
          >
            <b-icon-envelope /> contact
          </div>
        </b-container>
      </b-col>
      <b-col v-if="index === 0" cols="9" class="main-menu">
        <div class="intro">
          Hello semua!, saya ilham dan saya adalah seorang web developer!!
        </div>
      </b-col>
      <b-col v-else-if="index === 1" cols="9" class="intro2">
        <div class="pintro2">
          <h1 class="h1">about</h1>
          <p>
            perkenalkan nama saya Muhammad Abdurrahman Ilham saya berumur 18
            tahun , saya dibimbing oleh pak andrawan erlangga, saya belajar
            frontend, saya belajar pemrograman menggunakan sistem operasi
            windows,pada awalnya saya hanya menggunakann web jsfiddle, sampai
            saya benar benar bisa mengoding lalu pindah ke aplikasi seperti:
            vueJs , nodeJs ,dan visual studio code. impian saya setelah bisa
            belajar pemrograman dan diterima oleh perusahaan ini, lalu saya bisa
            lanjut pendidikan saya ke jenjang yg lebih tinggi.
          </p>
        </div>
      </b-col>
      <b-col v-else-if="index === 2" cols="12" sm="9" class="intro3">
        <div class="pintro3">
          <h1 class="data-pribadi">data pribadi</h1>
          <ul>
            <li>nama : muhammad abdurrahman ilham</li>
            <li>alamat : villa bekasi indah 2 blok j11 no9</li>

            <li>TTL : bekasi,22 maret,2005</li>

            <li>no tlp : 088211911963</li>
            <li>jenis kelamin : laki-laki</li>
            <li>agama : islam</li>
            <li>kewarganegaraan : indonesia</li>
            <li>Email: ilhamabdurrahmanahmaf@gmail.com</li>
            <li>kewarganegaraan : indonesia</li>
            <li>status : belum menikah</li>
          </ul>
          <ul>
            <h1 class="pengalaman">pengalaman</h1>
            <li>anggota osis smk 10 november</li>
            <li>anggota marawis smpn 13 tambun selatan</li>
            <li>prakerin di pt sumber sinar sejahtera</li>
          </ul>
          <h1 class="hobi">hobi</h1>
          <ul>
            <li>bermain badminton</li>
            <li>bermain gitar</li>
            <li>joging</li>
          </ul>
        </div>
      </b-col>
      <b-col v-else-if="index === 3" cols="9" class="intro4">
        <div class="pintro4">
          <h1 class="hubungiKami">hubungi kami</h1>

          <div id="ikon-sosmed" class="mt-4 mb-5">
            <div>
              <a href="https://id-id.facebook.com/ahmad.ilham.7587">
                <b-avatar icon="facebook" class="contact-me"></b-avatar>
              </a>

              <a
                href="https://id.linkedin.com/?trk=guest_homepage-basic_nav-header-logo"
              >
                <b-avatar icon="linkedin" class="contact-me"></b-avatar>
              </a>

              <a href="">
                <b-avatar icon="whatsapp" class="contact-me"></b-avatar>
              </a>
              <a href="">
                <b-avatar icon="envelope" class="contact-me"></b-avatar>
              </a>
            </div>
          </div>
        </div>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: "MenuUtama",
  data: function () {
    return {
      index: 0,
      showMenu: true,
    };
  },
};
</script>


<style scoped>
.side-menu {
  background-color: #0082fbf7;
  min-height: 100vh;
}
.main-menu {
  background-image: url("../assets/background-ilham.jpeg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
.foto-profil {
  border-radius: 50%;
  width: 150px;
  height: 150px;
  margin-top: 50px;
  border: #24185ef7 7px solid;
  object-position: center;
}
.nama {
  color: white;
  font-size: 25px;
  font-weight: bolder;
}
.sosmed {
  background-color: #24185ef7;
  color: white;
  margin-right: 7px;
  margin-left: 7px;
  padding: 3px;
}
.sosmed2 {
  background-color: #24185ef7;
  color: white;
  margin-right: 7px;
  margin-left: 20px;
  padding: 3px;
  margin-top: 20px;
}
.sosmed:hover {
  color: #0082fbf7;
  padding: 0px;
}
.bungkus-navigasi {
  text-align: left;
  color: white;
  font-size: 25px;
  font-weight: 500px;
  margin-top: 60px;
}
.item-navigasi {
  padding-top: 20px;
  padding-bottom: 20px;
  padding-left: 50px;
}
.item-navigasi:hover {
  background-color: #18325ef7;
  font-weight: 700;
  transition: 1s;
}
.selected {
  background-color: rgb(28, 72, 132);
}
.intro {
  color: white;
  font-size: 30px;
  margin-top: 300px;
  font-style: italic;
}
.intro2 {
  background-image: url("../assets/about-bckgrnd.jpg");
  background-repeat: no-repeat repeat;
  background-size: cover;
  background-position: center;
}
.intro3 {
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
.h1 {
  text-decoration: underline;
}
.pintro2 {
  font-size: 25px;
  color: white;
  font-weight: bold italic;
  font-style: Monospace;
  text-shadow: 2px 2px #ff00e6;
  margin-top: 200px;
}
.pintro3 {
  font-size: 25px;
  color: black;
  font-weight: bold italic;
  font-style: Monospace;
  text-align: left;
  margin-top: 15px;
}
.pintro4 {
  font-size: 25px;
  color: black;
  font-weight: bolder;
  font-style: Monospace;

  padding: 10px;
  margin-top: 25px;
}
.contact-me {
  margin-left: 100px;
  margin-top: 28px;
}

.intro4 {
  background-repeat: no-repeat;
  background-size: 100%;
  background-position: center;
  background-color: white;
}
.tombol-menu {
  position: absolute;
  top: 7px;
  left: 5px;
  max-width: 100px;
  z-index: 3;
  display: none;
}
.hubungiKami {
  position: center;
  margin-right: solid;
  margin-top: 25px;
}

.show {
  display: block;
}
.hidden {
  display: none;
}

@media (max-width: 500px) {
  .side-menu {
    position: absolute;
    width: 300px;
    z-index: 2;
  }
  .main-menu {
    min-height: 800px;
    min-width: 100%;
  }
  .tombol-menu {
    display: block;
  }
  .intro2 {
    width: 100%;
  }
  .intro3 {
    margin: 10px;
  }
  .contact-me {
    margin-left: 0px;
  }
}
</style>

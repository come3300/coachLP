<template>
  <header>
      <div class="header-title">
        <h1>eatra.inc</h1>
      </div>
      <ul class="header-list">
        <li><a href="#">home</a></li>
        <li><a href="#">about</a></li>
        <li><a href="#">service</a></li>
        <li><a href="#">work</a></li>
        <li><a href="#">price</a></li>
        <li><a href="#">contact</a></li>
      </ul>

      <div id="hamburger" @click="hamburger()" :class="{'active':isClass}">
        <span></span>
        <span></span>
        <span></span>
      </div>
  

  <!-- ここを追加していく -->
      <nav class="menu-content" :class="{'open':isClass}">
      <p class="menu-title">estra inc.</p>
      <ul class="menu-content_inner">
        <li>
          <a href="#">home</a>
        </li>
        <li>
          <a href="#">about</a>
        </li>
        <li>
          <a href="#">service</a>
        </li>
        <li>
          <a href="#">works</a>
        </li>
        <li>
          <a href="#">price</a>
        </li>
        <li>
          <a href="#">contact</a>
        </li>
      </ul>
    </nav>

    </header>
</template>

<script>
// ここを追加
export default {
  data() {
    return {
      isClass: false
    };
  },
  methods: {
    hamburger() {
      this.isClass = !this.isClass; //trueとfalseを切り替え
    }
  }
};
</script>


<style scoped>
header {
  background: black;
  color: white;
  height: 50px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 40px;
}

.header-title {
  font-size: 18px;
}

.header-list {
  display: flex;
  justify-content: space-between;
  list-style: none;
}

.header-list li {
  padding: 20px;
  font-size: 14px;
}

.header-list a {
  color: white;
  text-decoration: none;
}
@media screen and (max-width: 480px) {
  #hamburger {
    width: 40px;
    height: 40px;
    position: absolute;
    cursor: pointer;
    z-index: 100;
    top: 15px;
    right: 20px;
    transition: 0.4s;
  }

  #hamburger span {
    position: absolute;
    left: 2px;
    display: block;
    width: 35px;
    height: 2px;
    background-color: #fff;
    transition: 0.8s;
  }

  #hamburger span:nth-of-type(1) {
    top: 10px; /* ハンバーガーメニューの1本目の棒 */
  }

  #hamburger span:nth-of-type(2) {
    top: 20px; /* ハンバーガーメニューの2本目の棒 */
  }

  #hamburger span:nth-of-type(3) {
    top: 30px; /* ハンバーガーメニューの3本目の棒 */
  }

  .header-list {
    display: none;
  }
}
</style>
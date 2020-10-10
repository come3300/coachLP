<template>
<footer>
      <p>Copyright2019 estra inc.All Right Resereved.</p>
    </footer>
</template>

<style scoped>

footer {
  background-color: black;
  height: 200px;
  color: white;
  position: relative;
  font-size: 10px;
}

footer p {
  position: absolute;
  bottom: 0%;
  left: 40%;
}

@media screen and (max-width: 480px){
  footer {
    height: 50px;

    font-size: 100%;

    position: relative;
  }

  footer p {
    position: absolute;
    left: 5%;
    white-space: nowrap;
  }
}
</style>
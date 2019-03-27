<template>
  <nav>
    <ul>
      <li v-for="(link, key) in links" :key="key">{{ link }}</li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "rainbow-nav",

  data() {
    return {
      links: "MARTIN!"
    };
  }
};
</script>

<style lang="scss" scoped>
$rainbow: #FF0000 #FF7F00 #FFFF00 #00FF00 #0000FF #4B0082 #9400D3;
ul {
  display: flex;
  list-style-type: none;
  margin: 0;
  padding: 0;
  li {
    width: 100%;
    font-size: 1rem;
    font-weight: 700;
    padding: 0;
    margin: 0;
    display: inline-block;
    text-shadow: 0px 0px 1px #fff;
    @each $colour in $rainbow {
      $i: index($rainbow, $colour);
      &:nth-of-type(#{$i}) {
        background-color: $colour;
      }
    }
  }
}
</style>

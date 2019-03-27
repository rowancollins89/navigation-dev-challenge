<template>
  <nav>
    <ul>
      <li v-for="(link, key) in links" :key="key">{{ link }}</li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "gradient-nav",

  data() {
    return {
      links: "MARTIN!"
    };
  }
};
</script>

<style lang="scss" scoped>
$beginning: #dd9900;
$end: #00aaff;
$count: 7;

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
    @for $j from 1 through $count {
      $percentage: $j * (100 / ($count - 1)) - (100 / ($count - 1));
      &:nth-of-type(#{$j}) {
        background-color: mix($end, $beginning, $percentage);
      }
    }
  }
}
</style>

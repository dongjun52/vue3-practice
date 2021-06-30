<template>
  <div class="hello">
    <p ref="user">my name :</p>
  </div>
</template>

<script>
import { onMounted, ref } from "vue";

export default {
  name: "CompositionAPI",

  setup() {
    const user = ref < String > "foo";
    user.value = "andy";

    onMounted(() => {
      console.log(user.value);
    });
    return {
      user,
    };
  },
};
</script>

<style scoped></style>

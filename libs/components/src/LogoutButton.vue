<template>
  <div class="logout-button" @click="logout">
    <slot>
      <Button icon="pi pi-sign-out" class="p-button-outlined p-button-rounded"/>
    </slot>
  </div>
</template>

<script lang="ts">
import {defineComponent} from "vue";
import {useSolidSession} from "solid-b2b-showcase-libs/composables";

export default defineComponent({
  name: "LoginButton",
  setup() {
    const {logout} = useSolidSession();
    return {logout};
  },
});
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>

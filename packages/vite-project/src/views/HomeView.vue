<script>
import TheWelcome from "../components/TheWelcome.vue";
import request from "@sxtech/api";
import Button from "@sxtech/components";

export default {
  components: {
    TheWelcome,
    Button,
  },
  async created() {
    const res = await request({
      method: "get",
      url: "http://49.4.85.96/farm-jdcx/crop/getCropList",
    });

    console.log(res);
  },
};
</script>

<template>
  <main>
    <TheWelcome />
    <Button></Button>
  </main>
</template>


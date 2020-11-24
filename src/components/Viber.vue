<template>
  <span @click="viberLink(url)">
    <icon name="brands/viber" color="#583eb5" :scale="scale"></icon>
  </span>
</template>

<script>
import objectToGetParams from "../utils/objectToGetParams";
import "vue-awesome/icons/brands/viber";
import Icon from "vue-awesome/components/Icon";
export default {
  name: "twitter",
  methods: {
    viberLink(url) {
      window.open(
        "viber://forward" +
          objectToGetParams({
            url: url,
            text: url,
          }),
        "__blank"
      );
    },
  },
  components: {
    Icon,
  },
  props: {
    url: {
      required: true,
      type: String,
    },
    scale: {
      required: false,
      type: String,
    },
  },
};
</script>

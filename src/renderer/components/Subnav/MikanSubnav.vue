<template>
  <nav class="subnav-inner">
    <h3>{{ title }}</h3>
    <ul>
      <li
        @click="() => nav('basic')"
        :class="[current === 'basic' ? 'active' : '']"
      >
        <i class="subnav-icon">
          <mo-icon name="preference-basic" width="20" height="20" />
        </i>
        <span>{{ $t("mikan.bangumi-search") }}</span>
      </li>
    </ul>
  </nav>
</template>

<script>
import "@/components/Icons/preference-basic";

export default {
  name: "mo-mikan-subnav",
  props: {
    current: {
      type: String,
      default: "basic"
    }
  },
  computed: {
    title() {
      return this.$t("subnav.mikan");
    }
  },
  methods: {
    nav(category = "basic") {
      this.$router
        .push({
          path: `/mikan/${category}`
        })
        .catch(err => {
          console.log(err);
        });
    }
  }
};
</script>

<template>
    <div>
        <h1>{{ parts.title }}</h1>
        <div>
            {{ parts.description }}
        </div>
    </div>
</template>
<script>
import parts from '../data/parts';

export default {
  name: 'PartInfo',
  computed: {
    parts() {
      const { partType, id } = this.$route.params;
      return parts[partType].find((part) => part.id === +id);
    },
  },
};
</script>

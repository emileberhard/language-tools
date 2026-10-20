<script setup lang="ts" generic="T">
defineProps<{ item: T }>();
defineSlots<{ default?(props: { value: T }): any }>();
</script>

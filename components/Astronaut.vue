<script lang="ts" setup>
const spaceManRef = ref();
const { scene, animations } = await useGLTF("/spaceManFalling.glb");

onMounted(async () => {
  console.log("asdasd", spaceManRef.value);
  if (!spaceManRef.value) return;
  const { actions } = await useAnimations(animations, spaceManRef);
  console.log(actions);
  actions["Idle"].play();
});
// const { onLoop } = useRenderLoop();
// onLoop(async () => {
//   if (!spaceManRef.value) return;
//   const { actions } = await useAnimations(animations, spaceManRef);

//   actions["Idle"].play();
// });
</script>

<template>
  <primitive :object="scene" ref="spaceManRef" />
</template>

<style scoped></style>

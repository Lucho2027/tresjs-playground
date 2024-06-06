<script lang="ts" setup>
// const spaceManRef = ref();
// const {
//   scene: scenes,
//   animations,
//   scene,
// } = await useGLTF("/spaceManFalling.glb");

// onMounted(async () => {
//   if (!spaceManRef.value) return;
//   const { actions } = await useAnimations(animations, spaceManRef);
//   actions["Idle"].play();
// });
</script>
<template>
  <TresCanvas window-size clear-color="black" :alpha="true">
    <TresPerspectiveCamera :position="[1, 1, 5]" :look-at="[0, 0, 0]" />

    <OrbitControls />
    <!-- <MouseParallax
      :factor="1"
      :ease="3"
    /> -->
    <Precipitation
      :speed="0.05"
      :count="5"
      :randomness="0"
      color="#4285f4"
      :size="0.02"
    />
    <Precipitation
      :speed="0.015"
      :count="5"
      :randomness="0"
      color="#34A853"
      :size="0.02"
    />
    <Precipitation
      :speed="0.015"
      :count="5"
      :randomness="0"
      color="#FBBC05"
      :size="0.02"
    />
    <Precipitation
      :speed="0.015"
      :count="5"
      :randomness="0"
      color="#EA4335"
      :size="0.02"
    />
    <!-- <TresMesh > -->
    <Suspense>
      <Astronaut />
    </Suspense>
    <!-- </TresMesh> -->
  </TresCanvas>
</template>

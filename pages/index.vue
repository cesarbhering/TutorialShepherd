<template>
<div>
  <div id='shepherd-teste'>
    <h1>TESTE TESTE </h1>
  </div>

</div>
</template>
<script>
export default {
  name: 'IndexPage',

  mounted() {
      this.$nextTick(() => {
        const tour = this.$shepherd({
          useModalOverlay: true,
          defaultStepOptions: {
            popperOptions: {
              modifiers: [{ name: 'offset', options: { offset: [0, 50] } }]
            }
          }
        });

        tour.addStep({
          attachTo: { element: '#shepherd-teste', on: 'top' },
          text: 'Test'
        });

        tour.start();
      });
    }
}
</script>
<style scoped>
#shepherd-teste {
  background-color: aqua;
  margin: 25%;
  width: 50%;
  border: 3px solid green;
  text-align: center;
  padding: 10px;
  height: 50%;
  top: 5000px;
  bottom: 123;
}
</style>

<template>
  <div class="card-container">
    <img
      :src="characterList.image"
      alt="avatar-image"
    >
    <p><span>Name:</span> {{ characterList.name }}</p>
    <p class="medium__item">
      <span>Gender:</span> {{ characterList.gender }}
    </p>
    <p class="last__item">
      <span>Species:</span> {{ characterList.species }}
    </p>
  </div>
</template>

<script>

export default {
    name: "Card",
    props: ['characterList']
}
</script>

<style scoped>
.card-container {
  display: flex;
  flex-direction: column;
  background-color: #ffffff;
  border-radius: 20px;
  cursor: pointer;
  -moz-osx-font-smoothing: grayscale;
}

.card-container:hover {
  background: -webkit-linear-gradient(#FFF720, #3CD500);
  box-shadow: 5px 5px 5px 5px #3CD500;
}

img {
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
}

.medium__item{
    margin-top: 5px;
}

.last__item{
  margin-bottom: 20px;
  margin-top: 5px;
}

span {
  font-weight: bold;
  font-size: 14px;  
}

</style>

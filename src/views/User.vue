<template>
  <div class="user">
    <h1>This is User setting page</h1>
    <div class="user-card">
      <div class="contents-wrapper">
        <div class="avator">
          <img
            src="https://avatars.githubusercontent.com/u/4125257?v=4"
            alt="avator image"
          />
        </div>
        <div class="basic-information">
          <div>
            <p class="basic-information__key">Name:</p>
            <span class="basic-information__item">{{ name }}</span>
          </div>
          <p>
            <span class="basic-information__key">Age:</span
            ><span class="basic-information__item">{{ age }}</span>
          </p>
          <p>
            <span class="basic-information__key">Gender:</span
            ><span class="basic-information__item">{{ gender }}</span>
          </p>
          <p>
            <span class="basic-information__key">Company/School:</span>
            <span class="basic-information__item">{{ company_school }}</span>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  setup() {
    return {
      name: "Keeth Kuwahara",
      age: 35,
      gender: "Male",
      company_school: "Yumemi Inc,",
    };
  },
});
</script>

<style scoped lang="scss">
.user {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
  background: #fff;

  &-card {
    padding: 1rem;
    margin-top: 1rem;
    border-radius: 8px;
    box-shadow: 0 0 8px gray;
    border: 1px solid #ddd;

    .contents-wrapper {
      display: flex;
      justify-content: center;
    }

    .avator img {
      border-radius: 50%;
      width: 150px;
    }

    .basic-information {
      display: flex;
      flex-direction: column;
      margin-left: 1rem;
      text-align: left;

      &__key {
        display: inline;
        width: 100px;
      }

      &__item {
        font-weight: bold;
        font-size: 2rem;
        color: #42b983;
      }
    }
  }
}
</style>

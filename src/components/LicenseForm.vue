<template>
  <form class="license--form">
    <div class="license--country">
      <select class="license--country--select">
        <option value="nl">NL</option>
        <option value="de">DE</option>
        <option value="uk">UK</option>
        <option value="usa">USA</option>
      </select>
    </div>
    <div class="license--number">
      <input type="text" class="license--number--input" />
    </div>
    <input
      type="submit"
      name="like-driver"
      value="Like"
      class="license--submit"
    />
    <input
      type="submit"
      name="dislike-driver"
      value="Dislike"
      class="license--submit"
    />
  </form>
</template>

<script>
export default {
  name: "LicenseForm"
};
</script>

<style scoped lang="scss">
.license--form {
  --license-number-width: 70%;
  --license-country-width: calc(100% - var(--license-number-width));
  --license-border-width: 1px;
  --license-border: var(--license-border-width) solid black;
  --license-padding: 5px;
  --license-margin: 5px;
  --license-height: 20vh;
  --license-number-color: yellow;

  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;

  & > * {
    margin-top: var(--license-margin);
    margin-bottom: var(--license-margin);
  }

  & .license--country {
    width: calc(
      var(--license-country-width) - var(--license-border-width) -
        (2 * var(--license-padding))
    );
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: blue;
    border-left: var(--license-border);
    border-top: var(--license-border);
    border-bottom: var(--license-border);
    border-radius: 5px 0 0 5px;
    padding: var(--license-padding);
    height: var(--license-height);
  }

  & .license--country--select,
  & .license--number--input {
    height: var(--license-height);
    font-size: var(--license-height);
    max-width: 80%;
  }

  & .license--number {
    width: calc(
      var(--license-number-width) - var(--license-border-width) -
        (2 * var(--license-padding))
    );
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: var(--license-number-color);
    border-right: var(--license-border);
    border-top: var(--license-border);
    border-bottom: var(--license-border);
    border-radius: 0 5px 5px 0;
    padding: var(--license-padding);
    height: var(--license-height);
  }

  & .license--number--input {
    border: 0;
    background-color: var(--license-number-color);
    text-align: center;
  }

  & .license--submit {
    width: 50%;
  }
}
</style>

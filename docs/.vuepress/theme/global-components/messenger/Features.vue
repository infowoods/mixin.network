<template>
  <div class="text-center py-8">
    <h2 class="text-2xl md:text-3xl font-bold">More Features.</h2>
    <div class="features grid gap-4 grid-cols-1 md:grid-cols-5 text-left mt-10">
      <div class="feature md:col-span-3">
        <h3
          class="feature-title text-lg md:text-2xl font-bold px-8 white--text"
        >
          All messages encrypted
        </h3>
        <div class="feature-image-wrapper">
          <img
            src="/images/messenger/feat-encrypted.svg"
            title="All messages encrypted"
            alt="All messages encrypted"
          />
        </div>
      </div>

      <div class="feature grid place-content-between md:col-span-2">
        <h3
          class="feature-title text-lg md:text-2xl font-bold px-8 white--text"
        >
          Chat backup
        </h3>
        <div class="feature-image-wrapper">
          <img
            src="/images/messenger/feat-backup.svg"
            title="Chat backup"
            alt="Chat backup"
          />
        </div>
      </div>

      <div class="feature grid place-content-between md:col-span-2">
        <h3
          class="feature-title text-lg md:text-2xl font-bold px-8 white--text"
        >
          Enormous dApps
        </h3>
        <div class="feature-image-wrapper">
          <img
            src="/images/messenger/feat-dapps.svg"
            title="Enormous dApps"
            alt="Enormous dApps"
          />
        </div>
      </div>

      <div class="feature grid place-content-between md:col-span-3">
        <h3
          class="feature-title text-lg md:text-2xl font-bold px-8 black--text"
        >
          Support all popular cryptos
        </h3>
        <div class="feature-image-wrapper">
          <img
            src="/images/messenger/feat-cryptos.png"
            title="Support all popular cryptocurrencies"
            alt="Support all popular cryptocurrencies"
          />
        </div>
      </div>

      <div class="feature md:col-span-3">
        <h3
          class="feature-title text-lg md:text-2xl font-bold px-8 black--text"
        >
          Transfer easily
        </h3>
        <div class="feature-image-wrapper">
          <img
            src="/images/messenger/feat-transfer.png"
            title="Transfer easily"
            alt="Transfer easily"
          />
        </div>
      </div>

      <div class="feature grid place-content-between md:col-span-2">
        <h3
          class="feature-title text-lg md:text-2xl font-bold px-8 white--text"
        >
          Secured 6 digit TIP
        </h3>
        <div class="feature-image-wrapper">
          <img
            src="/images/messenger/feat-pin.svg"
            title="Chat backup"
            alt="Chat backup"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Slogan",
};
</script>

<style lang="scss" scoped>
.feature {
  border-radius: 32px;
  background-color: #f6f7fa;
  position: relative;
  .feature-title {
    position: absolute;
    right: 0;
    left: 0;
    padding-top: 0;
    margin: 32px 0 0 0;
    text-align: center;
  }
}

@media (max-width: 768px) {
  .feature {
    .feature-title {
      margin-top: 16px;
    }
  }
}
</style>

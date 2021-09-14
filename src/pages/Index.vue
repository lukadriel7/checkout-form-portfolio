<template>
  <q-page padding class="row items-center justify-center page-background">
    <q-card dark class="col-xs-12 col-md-6 col-xl-4 checkout">
      <q-card-section class="text-center">
        <h2>Checkout</h2>
      </q-card-section>
      <q-card-section :horizontal="$q.screen.gt.sm">
        <q-card-section>
          <h5>Billing Address</h5>
          <div class="column q-gutter-md">
            <q-input
              standout="text-white"
              dark
              outlined
              label="Name"
              placeholder="John Smith"
            />
            <q-input
              standout="text-white"
              dark
              outlined
              label="Email"
              type="email"
              placeholder="example@example.com"
            />
            <q-input
              standout="text-white"
              dark
              outlined
              label="Address"
              type="address"
              placeholder="512 16th Street"
            />
            <q-input
              standout="text-white"
              dark
              outlined
              label="City"
              placeholder="New York"
            />
            <div>
              <div class="row q-col-gutter-md">
                <div class="col-6">
                  <q-input
                    standout="text-white"
                    dark
                    outlined
                    label="State"
                    placeholder="NY"
                  />
                </div>
                <div class="col-6">
                  <q-input
                    standout="text-white"
                    dark
                    outlined
                    label="Zip"
                    placeholder="22015"
                  />
                </div>
              </div>
            </div>
          </div>
        </q-card-section>
        <q-card-section>
          <h5>Payment</h5>

          <div class="column q-gutter-md">
            <div>
              <label for="cc">Accepted cards</label>
              <div id="cc" class="row q-gutter-md">
                <q-icon name="fab fa-cc-visa" color="indigo-10" size="lg" />
                <q-icon name="fab fa-cc-mastercard" color="red-10" size="lg" />
                <q-icon
                  name="fab fa-cc-amex"
                  color="deep-purple-10"
                  size="lg"
                />
                <q-icon name="fab fa-cc-discover" color="orange-10" size="lg" />
              </div>
            </div>
            <q-input
              standout="text-white"
              dark
              outlined
              label="Name on Card"
              placeholder="John Smith"
            />
            <q-input
              standout="text-white"
              dark
              outlined
              label="Credit Card Number"
              mask="#### #### #### ####"
              placeholder="1111 1111 1111 1111"
            />
            <q-input
              standout="text-white"
              dark
              outlined
              label="Expiry Month"
              type="text"
              placeholder="October"
            />
            <div>
              <div class="row q-col-gutter-md">
                <div class="col-6">
                  <q-input
                    standout="text-white"
                    dark
                    outlined
                    label="Expiry Year"
                    type="year"
                    mask="####"
                    placeholder="2026"
                  />
                </div>
                <div class="col-6">
                  <q-input
                    standout="text-white"
                    dark
                    outlined
                    type="number"
                    mask="###"
                    label="CVV"
                    placeholder="013"
                  />
                </div>
              </div>
            </div>
          </div>
        </q-card-section>
      </q-card-section>
      <q-card-actions vertical>
        <q-btn
          unelevated
          rounded
          outline
          size="lg"
          label="checkout"
          class="full-width"
        />
      </q-card-actions>
    </q-card>
  </q-page>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'PageIndex',
  components: {},
  setup() {
    return {};
  },
});
</script>

<style lang="scss" scoped>
.checkout {
  transition: 500ms;
  backdrop-filter: blur(7px);
  background-color: rgba(0, 0, 0, 0.1);
  border-radius: 30px;
  box-shadow: $shadow-12;
  border: 1px solid rgba(255, 255, 255, 0.15);
}
.checkout:hover {
  transition: 500ms;
}

.page-background {
  background-image: linear-gradient(
    to right top,
    #d16ba5,
    #c777b9,
    #ba83ca,
    #aa8fd8,
    #9a9ae1,
    #8aa7ec,
    #79b3f4,
    #69bff8,
    #52cffe,
    #41dfff,
    #46eefa,
    #5ffbf1
  );
}
</style>
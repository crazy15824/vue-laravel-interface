<template>
  <footer class="footer-shadow">
    <Modal v-model="isOpenPrivacy" max-width="800px">
      <div class="modalBox">
         <Privacy />
      </div>
    </Modal>
    <Modal v-model="isOpenTerms" max-width="800px">
      <div class="modalBox">
         <Terms />
      </div>
    </Modal>
    <div class="footer">
      <div class="col-md-12">
          <div >
            <div class="footer border-top-0" style="padding-top: 10px">
              <div class="container">
                  <div class="row  align-items-center flex-row-reverse copyright">
                    <div class="col-lg-12 col-sm-12 mt-3 mr-2 mt-lg-0 text-right">
                      Copyright © 2020 &nbsp; <a class="g-blue" href="https://www.ivse.finance" target="_blank">IvSe Finances</a>
                    </div>
                  </div>
                  <div class="text-right privacy">
                    <span class="price"><a href="#">Privacy&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|</a></span>
                    <span class="price"><a href="#">Terms&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|</a></span>
                    <span class="price"><a href="#">About Us</a></span>
                  </div>
                  <div class="d-none d-md-block ">
                    <div class="social">
                        <a class="social-icon linksfooter" :href="twitter" target=_blank><font-awesome-icon class="g-blue" :icon="['fab', 'twitter']" /></a>
                        <a class="social-icon linksfooter" :href="telegram" target=_blank><font-awesome-icon class="g-blue" :icon="['fab', 'telegram-plane']" /></a>
                        <a class="social-icon linksfooter" :href="github" target=_blank><font-awesome-icon class="g-blue" :icon="['fab', 'github']" /></a>
                    </div>
                  </div>
              </div>
            </div>
          </div>
          <!-- pagination-wrapper -->
        <!-- section-wrapper -->
      </div><!-- COL-END -->
    </div>
  </footer>
</template>

<script lang="ts">
import { Modal } from 'vue-neat-modal'
import Privacy from "@/components/statics/Privacy.vue";
import Terms from "@/components/statics/Terms.vue";

export default {
  name: 'Wallet',
  data() {
    return {
      isOpenPrivacy: false,
      isOpenTerms: false,
      github: "",
      twitter: "",
      telegram: ""
    }
  },
    mounted() {
      this.github   = process.env.VUE_APP_IVSE_GITHUB,
      this.twitter  = process.env.VUE_APP_IVSE_TWITTER,
      this.telegram = process.env.VUE_APP_IVSE_TELEGRAM
  },
  components: {
    Privacy,
    Terms,
    Modal
  },
}
</script>



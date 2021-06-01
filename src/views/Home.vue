<template>
  <Header />
  <div class="container-fluid no-fluid no-padding">
    <div class="row sm-gutters">
      <div class="col-md-3 sidebar ptb15">
          <Pairs />
          <div class="topspace"></div>
          <News />
      </div>
      <div class="col-md-9 content ptb15">
        <div class="content-round">
          <Tokeninfo />
          <tradingview />
          <div class="topspace"></div>
          <div class="topspace"></div>
          <Orders class="history-border"/>
        </div>
      </div>
    </div>
  </div>
  <Footer />

</template>

<script lang="ts">
import Header from "@/components/Header.vue"
import Footer from "@/components/Footer.vue"
import Orders from "@/components/Orders.vue"
import Tokeninfo from "@/components/Tokeninfo.vue"
import Pairs from "@/components/Pairs.vue"
import News from "@/components/News.vue"
import tradingview from '@/tradingview/tradingview.vue';

export default ({
  name: "Home",
  data() {
    return {
    }
  },
  components: {
    tradingview,
    Header,
    Orders,
    Pairs,
    News,
    Tokeninfo,
    Footer,
  }
});
</script>


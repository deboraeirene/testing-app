<template>
<app-root _nghost-exk-c36="" ng-version="10.0.11">
    <div _ngcontent-exk-c36="" class="global-wrapper">
      <app-header _ngcontent-exk-c36="" _nghost-exk-c35="">
        <nav _ngcontent-exk-c35="" class="navbar navbar-expand navbar-light">
          <a _ngcontent-exk-c35="" href="https://hangman.jpcc.my.id/" class="aug"> SKYBRIDGE TEST </a>
          <button _ngcontent-exk-c35="" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation" class="navbar-toggler">
            <span _ngcontent-exk-c35="" class="navbar-toggler-icon"></span>
          </button>
        </nav>
      </app-header>
      <router-outlet _ngcontent-exk-c36=""></router-outlet>
      <app-home _nghost-exk-c31="">
      
        <div _ngcontent-exk-c31="" class="header-wrapper">
          <div _ngcontent-exk-c31="" class="header-big"> Hi, debora eirene </div>
          <div _ngcontent-exk-c31="" class="header-small"> Do you wanna build a snowman? </div>
        </div>
        <div _ngcontent-exk-c31="" class="friends-wrapper">
          <div _ngcontent-exk-c31="" class="friend-card-wrapper">
            <div _ngcontent-exk-c31="" class="friends-title"> Here you can call me FRIENDS </div>
            <div _ngcontent-exk-c31="" class="friend-card vip">
              <div _ngcontent-exk-c31="" class="vip"><span _ngcontent-exk-c31="" class="txt">VIP</span></div>
             
              <div _ngcontent-exk-c31="" class="img-wrapper">
                <div _ngcontent-exk-c31="" class="img"
                  style="background-image: url(&quot;https://api-hangman.jpcc.my.id/image/patrick.png&quot;);"></div>
              </div>
              <div _ngcontent-exk-c31="" class="title-big"> Hi, my name is Patrick </div>
              <div _ngcontent-exk-c31="" class="title-small"> Patrick Star </div>
              <div _ngcontent-exk-c31="" class="content-small"> 26 years old. </div>
            </div>
            <div _ngcontent-exk-c31="" class="friend-card vip">
              <div _ngcontent-exk-c31="" class="vip"><span _ngcontent-exk-c31="" class="txt">VIP</span></div>
             
              <div _ngcontent-exk-c31="" class="img-wrapper">
                <div _ngcontent-exk-c31="" class="img"
                  style="background-image: url(&quot;https://api-hangman.jpcc.my.id/image/squidward.png&quot;);"></div>
              </div>
              <div _ngcontent-exk-c31="" class="title-big"> Hi, my name is Squid </div>
              <div _ngcontent-exk-c31="" class="title-small"> Squidward Tentacles </div>
              <div _ngcontent-exk-c31="" class="content-small"> 27 years old. </div>
            </div>
            <div _ngcontent-exk-c31="" class="friend-card vip">
              <div _ngcontent-exk-c31="" class="vip"><span _ngcontent-exk-c31="" class="txt">VIP</span></div>
              <!---->
              <div _ngcontent-exk-c31="" class="img-wrapper">
                <div _ngcontent-exk-c31="" class="img"
                  style="background-image: url(&quot;https://api-hangman.jpcc.my.id/image/sponge.png&quot;);"></div>
              </div>
              <div _ngcontent-exk-c31="" class="title-big"> Hi, my name is Sponge </div>
              <div _ngcontent-exk-c31="" class="title-small"> Spongebob Squarepant </div>
              <div _ngcontent-exk-c31="" class="content-small"> 22 years old. </div>
            </div>
            <!---->
          </div>
        </div>
        
      </app-home>
      <!---->
    </div>
  </app-root>
</template>

<script>
    import axios from "axios"
    export default {
        name: 'test',
        data() {
            return {
                input: ''
            }
        },
        mounted() {
            console.log("abc")
            axios.get("https://api-hangman.jpcc.my.id/api/wordcheck/test")
                .then((success) => {
                    console.log(this.input);
                    this.input = success.data.data.input;
                }, (error) => {
                    console.log(error);
                    alert(error);
                });
        }
    }
</script>
<style scoped>
    .header-wrapper[_ngcontent-exk-c31] {
      width: 100%;
      background-color: #5c41ad;
      padding: 100px 20px;
      text-align: center
    }

    .header-wrapper[_ngcontent-exk-c31] .header-big[_ngcontent-exk-c31] {
      font-size: 80px;
      color: #fff;
      transition: all .2s
    }

    .header-wrapper[_ngcontent-exk-c31] .header-small[_ngcontent-exk-c31] {
      text-transform: uppercase;
      font-weight: 700;
      color: hsla(0, 0%, 100%, .6)
    }

    .header-wrapper[_ngcontent-exk-c31] .header-input[_ngcontent-exk-c31] input[_ngcontent-exk-c31] {
      transition: all .2s;
      font-size: 20px;
      border: 0;
      border-bottom: 2px solid #fff;
      background-color: transparent;
      color: #fff
    }
        .header-wrapper[_ngcontent-exk-c31] .header-input[_ngcontent-exk-c31] input[_ngcontent-exk-c31]::-moz-placeholder {
      color: hsla(0, 0%, 100%, .3)
    }

    .header-wrapper[_ngcontent-exk-c31] .header-input[_ngcontent-exk-c31] input[_ngcontent-exk-c31]::-ms-input-placeholder {
      color: hsla(0, 0%, 100%, .3)
    }

    .header-wrapper[_ngcontent-exk-c31] .header-input[_ngcontent-exk-c31] input[_ngcontent-exk-c31]::placeholder {
      color: hsla(0, 0%, 100%, .3)
    }

    .header-wrapper.focused[_ngcontent-exk-c31] .header-big[_ngcontent-exk-c31] {
      font-size: 20px
    }

    .header-wrapper.focused[_ngcontent-exk-c31] .header-input[_ngcontent-exk-c31] input[_ngcontent-exk-c31] {
      font-size: 80px
    }

    .header-wrapper[_ngcontent-exk-c31] .header-action[_ngcontent-exk-c31] {
      padding: 20px 0;
      margin-top: 25px
    }

    .header-wrapper[_ngcontent-exk-c31] .header-action[_ngcontent-exk-c31] .btn[_ngcontent-exk-c31] {
      color: hsla(0, 0%, 100%, .8)
    }

    .header-wrapper[_ngcontent-exk-c31] .header-action[_ngcontent-exk-c31] .btn[_ngcontent-exk-c31]:focus,
    .header-wrapper[_ngcontent-exk-c31] .header-action[_ngcontent-exk-c31] .btn[_ngcontent-exk-c31]:hover {
      color: #fff
    }

    .friends-wrapper[_ngcontent-exk-c31] {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column
    }

    .friends-wrapper[_ngcontent-exk-c31] .friend-card-wrapper[_ngcontent-exk-c31] {
      width: 700px;
      text-align: center
    }

    .friends-wrapper[_ngcontent-exk-c31] .friend-card-wrapper[_ngcontent-exk-c31] .friends-title[_ngcontent-exk-c31] {
      font-weight: 700;
      font-size: 150%;
      padding: 40px 20px 0;
      color: #777;
      width: 100%;
      border-bottom: 2px solid #eee;
      text-align: left
    }

    .friends-wrapper[_ngcontent-exk-c31] .friend-card-wrapper[_ngcontent-exk-c31] .friend-card[_ngcontent-exk-c31] {
      display: inline-block;
      border-radius: 5px;
      border: 1px solid #f2f2f2;
      background-color: #fafafa;
      margin: 20px 3px;
      padding: 0;
      text-align: center;
      transition: all .2s
    }

    .friends-wrapper[_ngcontent-exk-c31] .friend-card-wrapper[_ngcontent-exk-c31] .friend-card[_ngcontent-exk-c31]:hover {
      background-color: #f1f1f1;
      border-color: #5c41ad
    }

    .friends-wrapper[_ngcontent-exk-c31] .friend-card-wrapper[_ngcontent-exk-c31] .friend-card.vip[_ngcontent-exk-c31] {
      border-radius: 0 5px 5px 5px
    }

    .friends-wrapper[_ngcontent-exk-c31] .friend-card-wrapper[_ngcontent-exk-c31] .friend-card.vip[_ngcontent-exk-c31] .vip[_ngcontent-exk-c31] {
      width: 0;
      height: 0;
      border-bottom: 0;
      border-right: 40px solid transparent;
      margin-bottom: -40px;
      border-top: 40px solid #5c41ad
    }

    .friends-wrapper[_ngcontent-exk-c31] .friend-card-wrapper[_ngcontent-exk-c31] .friend-card.vip[_ngcontent-exk-c31] .vip[_ngcontent-exk-c31] .txt[_ngcontent-exk-c31] {
      color: #fff;
      position: relative;
      top: -28px;
      width: 0;
      left: 8px;
      text-align: center;
      font-size: 10px;
      font-family: arial;
      display: block;
      transform: rotate(-45deg);
      font-weight: 700
    }

    .friends-wrapper[_ngcontent-exk-c31] .friend-card-wrapper[_ngcontent-exk-c31] .friend-card[_ngcontent-exk-c31] .title-big[_ngcontent-exk-c31] {
      font-size: 120%;
      padding: 10px 0
    }

    .friends-wrapper[_ngcontent-exk-c31] .friend-card-wrapper[_ngcontent-exk-c31] .friend-card[_ngcontent-exk-c31] .title-small[_ngcontent-exk-c31] {
      font-size: 90%;
      font-weight: 700;
      text-transform: uppercase
    }

    .friends-wrapper[_ngcontent-exk-c31] .friend-card-wrapper[_ngcontent-exk-c31] .friend-card[_ngcontent-exk-c31] .img-wrapper[_ngcontent-exk-c31] {
      padding: 20px 10px
    }

    .friends-wrapper[_ngcontent-exk-c31] .friend-card-wrapper[_ngcontent-exk-c31] .friend-card[_ngcontent-exk-c31] .img-wrapper[_ngcontent-exk-c31] .img[_ngcontent-exk-c31] {
      width: 200px;
      border-radius: 10000px;
      border: 2px solid #999;
      height: 200px;
      background-size: contain;
      background-repeat: no-repeat;
      background-position-x: center;
      background-position-y: center;
      background-color: #fff
    }

    .friends-wrapper[_ngcontent-exk-c31] .friend-card-wrapper[_ngcontent-exk-c31] .friend-card[_ngcontent-exk-c31] .content-small[_ngcontent-exk-c31] {
      padding: 10px 0 25px;
      font-weight: 75%;
      color: #5c41ad;
      font-weight: 700
    }

    .user-wrapper[_ngcontent-exk-c31] {
      max-width: 700px;
      margin: 80px auto 0
    }

    .user-wrapper[_ngcontent-exk-c31] .loading[_ngcontent-exk-c31] {
      min-height: 600px;
      display: flex;
      justify-content: center;
      align-items: center
    }

    .user-wrapper[_ngcontent-exk-c31] .loading[_ngcontent-exk-c31] fa-icon[_ngcontent-exk-c31] {
      color: #5c41ad
    }

    .user-wrapper[_ngcontent-exk-c31] .user-title[_ngcontent-exk-c31] {
      font-weight: 700;
      font-size: 150%;
      padding: 40px 20px 0;
      color: #777;
      width: 100%;
      border-bottom: 2px solid #eee;
      text-align: left;
      margin-bottom: 20px
    }

    .user-wrapper[_ngcontent-exk-c31] .table[_ngcontent-exk-c31] tbody[_ngcontent-exk-c31] tr[_ngcontent-exk-c31]:nth-child(odd) td[_ngcontent-exk-c31] {
      background-color: #f8f8f8
    }

    .user-wrapper[_ngcontent-exk-c31] .table[_ngcontent-exk-c31] tbody[_ngcontent-exk-c31] tr[_ngcontent-exk-c31]:hover td[_ngcontent-exk-c31] {
      background-color: #fee
    }

    .user-wrapper[_ngcontent-exk-c31] .pagination[_ngcontent-exk-c31] {
      margin: 10px 0 20px;
      display: flex;
      align-items: center;
      justify-content: center
    }

    .user-wrapper[_ngcontent-exk-c31] .pagination[_ngcontent-exk-c31] .button[_ngcontent-exk-c31] {
      padding: 5px 10px;
      border: 1px solid #ddd;
      min-width: 50px;
      text-align: center;
      cursor: pointer
    }

    .user-wrapper[_ngcontent-exk-c31] .pagination[_ngcontent-exk-c31] .button[_ngcontent-exk-c31] fa-icon[_ngcontent-exk-c31] {
      color: #5c41ad
    }

    .user-wrapper[_ngcontent-exk-c31] .pagination[_ngcontent-exk-c31] .button[_ngcontent-exk-c31]:first-child {
      border-radius: 5px 0 0 5px
    }

    .user-wrapper[_ngcontent-exk-c31] .pagination[_ngcontent-exk-c31] .button[_ngcontent-exk-c31]:last-child {
      border-radius: 0 5px 5px 0
    }

    .user-wrapper[_ngcontent-exk-c31] .pagination[_ngcontent-exk-c31] .button.selected[_ngcontent-exk-c31] {
      background-color: #5c41ad;
      color: #fff
    }
</style>
<template>
  <q-page class="">
    <div class="container">
      <q-drawer
        v-model="menuActive"
        bordered>
        <div class="flex column items-center justify-center q-py-xl">
          <p class="text-practice text-35 text-blue mb-80">cheby</p>
          <p class="text-black text-h6 q-mb-lg" @click="menuActive= false, scrollToElement('collection')">Collection</p>
          <p class="text-black text-h6 q-mb-lg" @click="menuActive= false, scrollToElement('journey')">Journey</p>
          <p class="text-black text-h6 q-mb-lg" @click="menuActive= false, scrollToElement('team')">Team</p>
          <p class="text-black text-h6 q-mb-lg" @click="menuActive= false, scrollToElement('faq')">Faq</p>
          <p class="text-black text-h6 mb-80" @click="menuActive= false, scrollToElement('social')">Social</p>
          <div class="flex items-center justify-center">
            <a href="" class="q-mr-lg">
              <svg width="62" height="62" viewBox="0 0 62 62" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M49.326 13.2862C47.3544 12.3938 41.5631 11.1471 37.04 10.6412C35.4079 10.4587 28.2016 10.2434 28.0656 10.3731C28.031 10.4061 27.407 10.4671 26.6798 10.5088C22.4276 10.7521 14.8955 12.2661 12.733 13.3121C11.8543 13.7368 10.7954 14.7618 10.3671 15.602C9.42875 17.4427 7.63433 23.4482 6.79559 27.5556C5.87571 32.06 5.44619 35.7049 5.19982 41.0995C5.08886 43.5285 5.21533 43.9494 6.43706 45.2293C10.0289 48.9899 15.2141 51.3758 20.3194 51.6157C21.6604 51.6788 21.726 51.6696 22.384 51.3236C23.53 50.7209 23.706 50.4 24.7923 46.9334C25.3268 45.2268 25.7295 43.7936 25.6871 43.7484C25.6442 43.7032 25.3256 43.6294 24.9796 43.5847C23.4596 43.3878 20.7793 42.6848 18.6818 41.933C16.9709 41.3197 16.5766 41.1062 16.0701 40.5182C14.5603 38.7646 15.51 36.0036 17.7983 35.4946C18.5834 35.3201 18.6532 35.335 21.3228 36.2549C23.1166 36.873 24.7923 37.2886 26.7162 37.5931C28.7337 37.9123 33.4995 37.9109 35.4335 37.5905C37.3425 37.2743 39.8367 36.6257 41.4259 36.0322C43.1768 35.3782 43.6277 35.3096 44.5077 35.5639C46.861 36.2439 47.5334 39.1644 45.7109 40.7911C45.2659 41.1881 44.7713 41.4512 43.799 41.8079C41.952 42.4857 39.7663 43.0935 38.0423 43.409C37.2309 43.5575 36.5193 43.7214 36.4602 43.7736C36.3194 43.8983 38.0786 49.5651 38.4658 50.2331C38.8088 50.8252 39.7317 51.4861 40.3855 51.6081C41.6305 51.8402 44.8447 51.3599 47.148 50.5976C48.3793 50.1899 50.7935 49.0528 51.7396 48.4344C53.9009 47.0225 56.1332 45.0223 56.5985 44.0809C56.8204 43.6326 56.8449 43.331 56.8318 41.2015C56.7966 35.4464 55.8588 29.0283 54.1246 22.6731C53.4774 20.3004 52.2121 16.5175 51.7879 15.6853C51.3519 14.8303 50.1504 13.6591 49.326 13.2862ZM20.5562 27.314C19.7341 25.5596 20.7131 23.4473 22.5684 22.9729C23.2132 22.8079 24.435 22.9286 24.9951 23.2124C25.5863 23.5122 26.2568 24.225 26.5068 24.8195C26.6016 25.0461 26.6798 25.5732 26.6798 25.9906C26.6798 26.8813 26.4883 27.3986 25.9204 28.0415C24.4326 29.7255 21.4993 29.3278 20.5562 27.314ZM35.6769 24.683C36.0742 23.8755 36.7179 23.3014 37.5119 23.0456C38.2594 22.8051 39.4573 22.8808 40.098 23.2089C41.192 23.7691 41.8196 24.783 41.8196 25.9906C41.8196 28.0678 39.891 29.5024 37.7762 28.9981C35.8505 28.539 34.8209 26.4222 35.6769 24.683Z" fill="#7063FF"/>
              </svg>
            </a>
            <a href="">
              <svg width="48" height="38" viewBox="0 0 48 38" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M41.9283 8.43395C41.6213 6.2204 40.5032 4.19976 38.7907 2.76392C37.0783 1.32809 34.8936 0.5794 32.6605 0.663064C30.4273 0.746727 28.3048 1.65678 26.7046 3.21672C25.1044 4.77666 24.1405 6.8753 24 9.10562C14.855 12.8773 5.91667 3.49978 5.91667 3.49978C3.33333 18.9998 11.0833 26.104 11.0833 26.104C7.57 29.3331 0.75 29.3331 0.75 29.3331C0.75 29.3331 4.83167 37.0831 22.915 37.0831C40.9983 37.0831 42.0833 16.4164 42.0833 16.4164C43.7868 15.7966 45.2276 14.6136 46.1672 13.0633C47.1067 11.5131 47.4888 9.68843 47.25 7.89145C45.5076 8.30498 43.7183 8.48738 41.9283 8.43395Z" fill="#7063FF"/>
              </svg>
            </a>
          </div>
        </div>
      </q-drawer>
      <header class="header top q-px-md q-px-md-none">
        <q-btn @click="menuActive=!menuActive" round dense class="lt-md" icon="menu"/>
        <p class="text-practice text-35">cheby</p>
        <div class="header-inner gt-sm">
          <nav class="nav">
            <ul>
              <li @click="scrollToElement('collection')">Collection</li>
              <li @click="scrollToElement('journey')">Journey</li>
              <li @click="scrollToElement('team')">Team</li>
              <li @click="scrollToElement('faq')">FAQ</li>
              <li @click="scrollToElement('social')">Social</li>
            </ul>
          </nav>
          <div class="">
            <a href="#">
              <svg class="q-mr-md" width="42" height="42" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M33.4135 9.0002C32.0779 8.3957 28.1548 7.55116 25.0908 7.20847C23.9851 7.08482 19.1034 6.93895 19.0113 7.0268C18.9878 7.04922 18.5651 7.09048 18.0725 7.11877C15.192 7.28359 10.0896 8.3092 8.62473 9.01775C8.02947 9.30548 7.31216 9.99984 7.02201 10.569C6.38634 11.8159 5.17076 15.8842 4.60258 18.6666C3.97944 21.7179 3.68847 24.1871 3.52157 27.8415C3.44641 29.487 3.53208 29.772 4.35971 30.6391C6.79288 33.1866 10.3054 34.8028 13.7638 34.9654C14.6723 35.0081 14.7167 35.0018 15.1625 34.7675C15.9388 34.3592 16.058 34.1418 16.7939 31.7935C17.156 30.6374 17.4288 29.6665 17.4001 29.6359C17.371 29.6053 17.1552 29.5553 16.9208 29.525C15.8911 29.3916 14.0754 28.9154 12.6546 28.4061C11.4956 27.9906 11.2284 27.846 10.8853 27.4477C9.86253 26.2598 10.5059 24.3894 12.0561 24.0447C12.5879 23.9264 12.6352 23.9365 14.4436 24.5597C15.6587 24.9783 16.7939 25.2599 18.0972 25.4662C19.4639 25.6824 22.6923 25.6815 24.0025 25.4645C25.2957 25.2502 26.9853 24.8109 28.0618 24.4088C29.2479 23.9658 29.5534 23.9193 30.1495 24.0916C31.7437 24.5522 32.1991 26.5306 30.9646 27.6326C30.6631 27.9015 30.3281 28.0797 29.6694 28.3214C28.4182 28.7805 26.9376 29.1923 25.7697 29.406C25.2201 29.5066 24.738 29.6176 24.698 29.6529C24.6026 29.7374 25.7943 33.5762 26.0566 34.0288C26.289 34.4299 26.9141 34.8776 27.357 34.9602C28.2004 35.1174 30.3778 34.7921 31.9381 34.2757C32.7722 33.9995 34.4076 33.2292 35.0485 32.8103C36.5126 31.8539 38.0248 30.4988 38.34 29.8612C38.4904 29.5575 38.5069 29.3531 38.4981 27.9106C38.4742 24.012 37.8389 19.6642 36.6642 15.3591C36.2257 13.7518 35.3686 11.1892 35.0813 10.6254C34.7859 10.0462 33.972 9.25283 33.4135 9.0002ZM13.9243 18.5029C13.3674 17.3145 14.0306 15.8835 15.2874 15.5622C15.7242 15.4504 16.5518 15.5322 16.9313 15.7244C17.3318 15.9275 17.786 16.4104 17.9553 16.8131C18.0196 16.9666 18.0725 17.3236 18.0725 17.6065C18.0725 18.2098 17.9428 18.5602 17.5581 18.9958C16.5502 20.1365 14.5632 19.8671 13.9243 18.5029ZM24.1674 16.7206C24.4365 16.1736 24.8725 15.7847 25.4104 15.6114C25.9168 15.4485 26.7282 15.4998 27.1623 15.7221C27.9034 16.1016 28.3285 16.7883 28.3285 17.6065C28.3285 19.0136 27.022 19.9854 25.5894 19.6438C24.285 19.3328 23.5875 17.8988 24.1674 16.7206Z" fill="white"/>
              </svg>

            </a>
            <a href="#">
              <svg width="42" height="42" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M33.145 13.8427C32.937 12.3432 32.1796 10.9743 31.0195 10.0017C29.8595 9.02901 28.3796 8.52183 26.8668 8.5785C25.354 8.63518 23.9161 9.25167 22.8321 10.3084C21.7481 11.3651 21.0952 12.7868 21 14.2977C14.805 16.8527 8.75 10.5002 8.75 10.5002C7 21.0002 12.25 25.8127 12.25 25.8127C9.87 28.0002 5.25 28.0002 5.25 28.0002C5.25 28.0002 8.015 33.2502 20.265 33.2502C32.515 33.2502 33.25 19.2502 33.25 19.2502C34.404 18.8302 35.38 18.0289 36.0165 16.9787C36.6529 15.9285 36.9117 14.6925 36.75 13.4752C35.5697 13.7553 34.3576 13.8788 33.145 13.8427Z" fill="white"/>
              </svg>

            </a>
          </div>

        </div>
        <div style="font-size: 18px; padding: 24px" class="button blue gt-sm">connect a wallet </div>
      </header>
    </div>
    <section class="offer">
      <div class="container">
        <div  class="offer-img">
          <q-img fit="contain" src="~assets/gif.gif" alt=""/>
        </div>

        <p class="text-practice text-72 text-w-shadow-b mb-30">Meet the gorgeous/<br>astonishing ChebuBears!</p>
        <p class="text-24 offer-text">
          ChebuBears are not just a collection of painted bears, they are the reincarnation of the legendary Cheburashka, the Soviet Union’s best-loved cartoon character, who still  winnings hearts after half a century.
        </p>
        <!--        <div class="offer-bottom">-->
        <!--          <p class="text-48 text-practice">Launch date: t b a</p>-->
        <!--          <div class="button green">button</div>-->
        <!--        </div>-->
        <div class="offer-bottom-alt">
          <p class="text-96 text-bold text-w-shadow-b text-w">Launch date: <span class="text-gr">T</span><span class="text-r2">B</span><span class="text-orange-4">A</span></p>

        </div>
      </div>
    </section>
    <img class="section_top" src="~assets/bg2_top.png" alt="">
    <section   class="collection">

      <div ref="collection" class="container">
        <p class="text-72 text-practice text-w-shadow-b text-w text-center mb-45">A huge family with<br class="gt-sm"> its own history…
        </p>
        <p class="text-24  text-center text-black mb-100">
          At the request of Cheburashka, you can find a character remotely resembling a brown bear.
          We took the liberty to dilute this model with new tones corresponding to the current trends in the world of digital art.<br><br>
          You will get acquainted with the hero of the Soviet stage, trying on the images of various heroes and villains, the roles of people, various evil spiritsr and even gods.

        </p>
        <!--        <div  class="collection-wrapper">-->
        <!--          <div class="buttons">-->
        <!--            <div-->
        <!--              @click="$refs.coll.prev()" class="prev-btn"><svg width="64" height="64" viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg">-->
        <!--              <circle cx="32" cy="32" r="32" />-->
        <!--              <path d="M39 32H25"  stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>-->
        <!--              <path d="M32 39L25 32L32 25"  stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>-->
        <!--            </svg>-->
        <!--            </div>-->
        <!--            <div @click="$refs.coll.next()" class="next-btn">-->
        <!--              <svg width="64" height="64" viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg">-->
        <!--                <circle cx="32" cy="32" r="32" />-->
        <!--                <path d="M25 32H39"  stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>-->
        <!--                <path d="M32 39L39 32L32 25"  stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>-->
        <!--              </svg>-->

        <!--            </div>-->
        <!--          </div>-->
        <!--          <Carousel ref="coll" :settings="settings_top" :breakpoints="breakpoints_top">-->
        <!--            <Slide v-for="(item,index) in collection" :key="index">-->
        <!--              <div class="collection-item" >-->
        <!--                <img draggable="false" :src="item.img" alt="">-->
        <!--                <p class="collection-item__title">{{item.title}}</p>-->
        <!--                <p class="collection-item__text">{{item.text}}</p>-->
        <!--              </div>-->
        <!--            </Slide>-->
        <!--          </Carousel>-->

        <!--        </div>-->
        <q-img src="~assets/coll.png"/>

      </div>
    </section>
    <img class="section_top" src="~assets/bg3_top.png" alt="">
    <section class="rarity">
      <div class="container">
        <p class="text-72 text-practice text-w-shadow-b text-w text-center mb-45">rarity</p>
        <p class="text-24 offer-text text-center mb-100">         The ChebuBears  family can really be called huge. And how, in such a variety, can you understand what kind of rarity a character has dropped to you? This table will help you!
        </p>
        <div class="rarity-wrapper mb-45">
          <div class="row q-col-gutter-lg">
            <div class="col-12 col-md-7">
              <div class="text-practice text-black text-h6 q-mb-lg">tiers</div>
              <div class="rarity-grid b-b">
                <p class="text-blue">Tier #1</p>
                <p class="text-grey-9">3500</p>
              </div>
              <div class="rarity-grid ">
                <p class="text-black">Tier #2</p>
                <p class="text-grey-5">2500</p>
              </div>
              <div class="rarity-grid mb-45">
                <p class="text-black">Tier #3</p>
                <p class="text-grey-5">1500</p>
              </div>
              <div class="text-practice text-black text-h6 q-mb-lg">Types</div>
              <div class="rarity-grid ">
                <p class="text-gr">Common</p>
                <p class="text-grey-9">Classic colors and clothes</p>
              </div>
              <div class="rarity-grid ">
                <p class="text-ye">Uncommon</p>
                <p class="text-grey-9">Colored and variegated</p>
              </div>
              <div class="rarity-grid ">
                <p class="text-r1"> Rare</p>
                <p class="text-grey-9">Rare clothing combinations</p>
              </div>
              <div class="rarity-grid ">
                <p class="text-r2">Ultra Rare</p>
                <p class="text-grey-9">Zombies, UFO, Freaks</p>
              </div>
            </div>
            <div class="col-5 gt-sm">
              <q-img src="~assets/chebus.png"/>
            </div>
          </div>
        </div>
        <q-img class="lt-md q-mb-lg" src="~assets/chebus.png"/>
        <div class="rarity-wrapper mb-45">
          <div class="text-practice text-black text-h6 q-mb-lg">Variations</div>
          <div class="row q-col-gutter-lg">
            <div class="col-12 col-md-6">

              <div class="rarity-grid ">
                <p class="text-black">12</p>
                <p class="text-grey-9">Backgrounds</p>
              </div>
              <div class="rarity-grid ">
                <p class="text-black">14</p>
                <p class="text-grey-9">Body color</p>
              </div>
              <div class="rarity-grid ">
                <p class="text-black">16</p>
                <p class="text-grey-9">Clothes</p>
              </div>
              <div class="rarity-grid ">
                <p class="text-black">32</p>
                <p class="text-grey-9">Facial expressions</p>
              </div>

            </div>
            <div class="col-12 col-md-6">
              <div class="rarity-grid ">
                <p class="text-black">14</p>
                <p class="text-grey-9">Headgear</p>
              </div>
              <div class="rarity-grid ">
                <p class="text-black">24</p>
                <p class="text-grey-9">Accessories</p>
              </div>
              <div class="rarity-grid ">
                <p class="text-black">32</p>
                <p class="text-grey-9">Glasses</p>
              </div>
              <div class="rarity-grid ">
                <p class="text-blue">1 821 606 000</p>
                <p class="text-blue">Total variations</p>
              </div>
            </div>
          </div>
        </div>


      </div>
    </section>
    <section class="rare-collection">

      <div class="container">
        <p class="text-72 text-practice text-w-shadow-b text-w text-center mb-30">Alpha-Bears Collection</p>
        <p class="text-24 offer-text text-center mb-30">
          That's why it's really worth hunting.<br>
          Of course, every bear in our collection is equally unique and valuable to us, but there are those that stand out strongly from the general background, such we call Alpha.
        </p>
        <div class="rare-collection-wrapper">
          <div class="buttons">
            <div @click="$refs.rare.prev()" class="prev-btn"><svg width="64" height="64" viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg">
              <circle cx="32" cy="32" r="32" />
              <path d="M39 32H25"  stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
              <path d="M32 39L25 32L32 25"  stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
            </div>
            <div @click="$refs.rare.next()" class="next-btn">
              <svg width="64" height="64" viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg">
                <circle cx="32" cy="32" r="32" />
                <path d="M25 32H39"  stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M32 39L39 32L32 25"  stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>

            </div>
          </div>
          <Carousel ref="rare" >
            <Slide class="q-px-md" v-for="(item,index) in rare_collection" :key="index">
              <div class="rare-collection-item" >
                <div class="rare-collection-item__img-wrapper">
                  <div class="rare-collection-item__img-inner" :style="{'background': `url(${item.bg_img}`}">
                    <q-img fit="contain" :src="item.img" alt=""/>
                  </div>
                </div>
                <div class="rare-collection-item__bottom">
                  <div class="rare-collection-item__title">
                    <p class="text-35 text-b text-practice mr-20">{{item.title1}}</p>
                    <p class="text-35 text-blue text-practice mr-15">{{item.title2}}</p>
                    <img draggable="false" :src="item.icon" alt="">
                  </div>
                  <p class="rare-collection-item__text text-b" v-html="item.text">

                  </p>
                  <div class="rare-collection-item__got">
                    <p class="text-24 text-black text-bold ">{{item.got_text}}</p>

                    <div  class="rare-collection-item__got-item" :class="{'has_link':got_item.is_link}"
                          v-for="(got_item,index1) in item.got_items" :key="index1">
                      <img class="q-mr-sm" :src="got_item.icon" alt="">
                      <p >{{got_item.text}}</p>
                      <div v-if="got_item.img" class="rare-collection-item__got-item-img">
                        <img :src="got_item.img" alt="">
                      </div>

                    </div>


                  </div>
                  <div class="text-left">
                    <div class="button blue bl-sh">Check</div>
                  </div>

                </div>

              </div>
            </Slide>
          </Carousel>

        </div>

      </div>
    </section>
    <img class="section_top" src="~assets/bg4_top.png" alt="">
    <section ref="journey" class="journey">
      <img draggable="false" class="journey-img-l gt-sm" src="~assets/j-l.png" alt="">
      <img draggable="false" class="journey-img-r gt-sm" src="~assets/j-r.png" alt="">
      <div  class="container">
        <p class="text-72 text-practice text-w-shadow-b text-w text-center mb-45">journey</p>
        <p class="text-24 offer-text text-center mb-100">
          Like any other, our journey begins with a clear plan of what and how we need to do.<br>
          The approved ideas have been collected, worked out and polished and now, you can read them below

        </p>
        <div class="journey-wrapper">
          <div class="journey-grid">
            <div class="journey-item" v-for="(item,index) in journey" :key="index">
              <div class="journey-item__img">
                <img v-if="item.img" :src="item.img" alt="">
              </div>
              <div class="journey-item__info " :class="{'w-border':item.need_border}">
                <p class="journey-item__info-date" :class="{done:item.is_done,negative:!item.need_border}">{{item.date}}</p>
                <p class="journey-item__info-title">{{item.title}}</p>
                <p class="journey-item__info-text">{{item.text}}</p>
                <q-img class="lt-md" fit="contain" v-if="item.img" :src="item.img" alt=""/>
              </div>
            </div>

          </div>
        </div>
      </div>
    </section>
    <img class="section_top" src="~assets/bg5_top.png" alt="">
    <section class="team">
      <div ref="team" class="container">
        <p class="text-72 text-practice text-w-shadow-w text-b text-center mb-45">the team</p>
        <p class="text-24 offer-text text-center mb-100">
          This project was accompanied by our entire team from the very beginning of its journey.
          A huge amount of effort was spent to bring a fresh look to the model of Soviet art without losing the brand's harsh style.
          <br><br>
          Each team member is a master of his craft, responsible strictly for his working stage. Thanks to this, we have a wide range of views on the current state of our project, which allows us to solve the tasks set on time, as well as soberly assess the situation in the world of modern digital art

        </p>
        <div class="team-grid">
          <div class="team-item" v-for="(item,index) in team" :key="index">
            <img draggable="false" :src="item.img" alt="">
            <div class="team-item__link"><img src="~assets/dis.svg" alt=""> <a :href="item.url">{{item.link_text}}</a></div>
            <div class="team-item__text">{{item.text}}</div>
          </div>
        </div>
        <div class="text-center">
          <a href="https://quinque.digital/" target="_blank">
            <div class="button blue">more about our team</div>
          </a>

        </div>
      </div>
    </section>
    <img class="section_top" src="~assets/bg6_top.png" alt="">
    <section class="faq">
      <div ref="faq" class="container">
        <p class="text-72 text-practice text-w-shadow-b text-w text-center mb-80">faq</p>

        <div class="faq-wrapper">
          <q-list >
            <div v-for="(item,index) in faqs"
                 :key="index">
              <q-expansion-item
                group="somegroup"
                expand-icon-class="text-green-11"
                :label="item.q"
                :header-class="$q.screen.lt.md ? 'text-dark  text-body1' : 'text-dark  text-h6'"
              >
                <q-card style="background: transparent">
                  <q-card-section class="text-dark">
                    {{item.a}}
                  </q-card-section>
                </q-card>
              </q-expansion-item>
              <hr style="opacity: .5">
            </div>
          </q-list>
        </div>

      </div>
    </section>
    <img class="section_top" src="~assets/bg7_top.png" alt="">
    <section class="social">
      <div ref="social" class="container">
        <p class="text-72 text-practice text-w-shadow-b text-w text-center mb-45">social</p>
        <p class="text-24 offer-text text-center mb-100">
          In order to keep up to date with the latest news and not miss anything important, we advise you to subscribe to our social networks.
          <br>
          There the team will interact with the audience and publish the current stages of our project

        </p>
        <div class="text-center">

          <a href="#">
            <svg class="q-mr-lg" width="42" height="42" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M33.4135 9.0002C32.0779 8.3957 28.1548 7.55116 25.0908 7.20847C23.9851 7.08482 19.1034 6.93895 19.0113 7.0268C18.9878 7.04922 18.5651 7.09048 18.0725 7.11877C15.192 7.28359 10.0896 8.3092 8.62473 9.01775C8.02947 9.30548 7.31216 9.99984 7.02201 10.569C6.38634 11.8159 5.17076 15.8842 4.60258 18.6666C3.97944 21.7179 3.68847 24.1871 3.52157 27.8415C3.44641 29.487 3.53208 29.772 4.35971 30.6391C6.79288 33.1866 10.3054 34.8028 13.7638 34.9654C14.6723 35.0081 14.7167 35.0018 15.1625 34.7675C15.9388 34.3592 16.058 34.1418 16.7939 31.7935C17.156 30.6374 17.4288 29.6665 17.4001 29.6359C17.371 29.6053 17.1552 29.5553 16.9208 29.525C15.8911 29.3916 14.0754 28.9154 12.6546 28.4061C11.4956 27.9906 11.2284 27.846 10.8853 27.4477C9.86253 26.2598 10.5059 24.3894 12.0561 24.0447C12.5879 23.9264 12.6352 23.9365 14.4436 24.5597C15.6587 24.9783 16.7939 25.2599 18.0972 25.4662C19.4639 25.6824 22.6923 25.6815 24.0025 25.4645C25.2957 25.2502 26.9853 24.8109 28.0618 24.4088C29.2479 23.9658 29.5534 23.9193 30.1495 24.0916C31.7437 24.5522 32.1991 26.5306 30.9646 27.6326C30.6631 27.9015 30.3281 28.0797 29.6694 28.3214C28.4182 28.7805 26.9376 29.1923 25.7697 29.406C25.2201 29.5066 24.738 29.6176 24.698 29.6529C24.6026 29.7374 25.7943 33.5762 26.0566 34.0288C26.289 34.4299 26.9141 34.8776 27.357 34.9602C28.2004 35.1174 30.3778 34.7921 31.9381 34.2757C32.7722 33.9995 34.4076 33.2292 35.0485 32.8103C36.5126 31.8539 38.0248 30.4988 38.34 29.8612C38.4904 29.5575 38.5069 29.3531 38.4981 27.9106C38.4742 24.012 37.8389 19.6642 36.6642 15.3591C36.2257 13.7518 35.3686 11.1892 35.0813 10.6254C34.7859 10.0462 33.972 9.25283 33.4135 9.0002ZM13.9243 18.5029C13.3674 17.3145 14.0306 15.8835 15.2874 15.5622C15.7242 15.4504 16.5518 15.5322 16.9313 15.7244C17.3318 15.9275 17.786 16.4104 17.9553 16.8131C18.0196 16.9666 18.0725 17.3236 18.0725 17.6065C18.0725 18.2098 17.9428 18.5602 17.5581 18.9958C16.5502 20.1365 14.5632 19.8671 13.9243 18.5029ZM24.1674 16.7206C24.4365 16.1736 24.8725 15.7847 25.4104 15.6114C25.9168 15.4485 26.7282 15.4998 27.1623 15.7221C27.9034 16.1016 28.3285 16.7883 28.3285 17.6065C28.3285 19.0136 27.022 19.9854 25.5894 19.6438C24.285 19.3328 23.5875 17.8988 24.1674 16.7206Z" fill="white"/>
            </svg>

          </a>
          <a href="#">
            <svg width="42" height="42" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M33.145 13.8427C32.937 12.3432 32.1796 10.9743 31.0195 10.0017C29.8595 9.02901 28.3796 8.52183 26.8668 8.5785C25.354 8.63518 23.9161 9.25167 22.8321 10.3084C21.7481 11.3651 21.0952 12.7868 21 14.2977C14.805 16.8527 8.75 10.5002 8.75 10.5002C7 21.0002 12.25 25.8127 12.25 25.8127C9.87 28.0002 5.25 28.0002 5.25 28.0002C5.25 28.0002 8.015 33.2502 20.265 33.2502C32.515 33.2502 33.25 19.2502 33.25 19.2502C34.404 18.8302 35.38 18.0289 36.0165 16.9787C36.6529 15.9285 36.9117 14.6925 36.75 13.4752C35.5697 13.7553 34.3576 13.8788 33.145 13.8427Z" fill="white"/>
            </svg>

          </a>

        </div>
      </div>
    </section>
    <footer class="footer ">
      <div class="container">
        <div class="header bottom">
          <p class="text-practice text-35">cheby</p>
          <div class="header-inner">
            <nav class="nav">
              <ul>
                <li @click="scrollToElement('collection')">Collection</li>
                <li @click="scrollToElement('journey')">Journey</li>
                <li @click="scrollToElement('team')">Team</li>
                <li @click="scrollToElement('faq')">FAQ</li>
                <li @click="scrollToElement('social')">Social</li>
              </ul>
            </nav>
            <div class="">
              <a href="#">
                <svg class="q-mr-lg" width="42" height="42" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd" clip-rule="evenodd" d="M33.4135 9.0002C32.0779 8.3957 28.1548 7.55116 25.0908 7.20847C23.9851 7.08482 19.1034 6.93895 19.0113 7.0268C18.9878 7.04922 18.5651 7.09048 18.0725 7.11877C15.192 7.28359 10.0896 8.3092 8.62473 9.01775C8.02947 9.30548 7.31216 9.99984 7.02201 10.569C6.38634 11.8159 5.17076 15.8842 4.60258 18.6666C3.97944 21.7179 3.68847 24.1871 3.52157 27.8415C3.44641 29.487 3.53208 29.772 4.35971 30.6391C6.79288 33.1866 10.3054 34.8028 13.7638 34.9654C14.6723 35.0081 14.7167 35.0018 15.1625 34.7675C15.9388 34.3592 16.058 34.1418 16.7939 31.7935C17.156 30.6374 17.4288 29.6665 17.4001 29.6359C17.371 29.6053 17.1552 29.5553 16.9208 29.525C15.8911 29.3916 14.0754 28.9154 12.6546 28.4061C11.4956 27.9906 11.2284 27.846 10.8853 27.4477C9.86253 26.2598 10.5059 24.3894 12.0561 24.0447C12.5879 23.9264 12.6352 23.9365 14.4436 24.5597C15.6587 24.9783 16.7939 25.2599 18.0972 25.4662C19.4639 25.6824 22.6923 25.6815 24.0025 25.4645C25.2957 25.2502 26.9853 24.8109 28.0618 24.4088C29.2479 23.9658 29.5534 23.9193 30.1495 24.0916C31.7437 24.5522 32.1991 26.5306 30.9646 27.6326C30.6631 27.9015 30.3281 28.0797 29.6694 28.3214C28.4182 28.7805 26.9376 29.1923 25.7697 29.406C25.2201 29.5066 24.738 29.6176 24.698 29.6529C24.6026 29.7374 25.7943 33.5762 26.0566 34.0288C26.289 34.4299 26.9141 34.8776 27.357 34.9602C28.2004 35.1174 30.3778 34.7921 31.9381 34.2757C32.7722 33.9995 34.4076 33.2292 35.0485 32.8103C36.5126 31.8539 38.0248 30.4988 38.34 29.8612C38.4904 29.5575 38.5069 29.3531 38.4981 27.9106C38.4742 24.012 37.8389 19.6642 36.6642 15.3591C36.2257 13.7518 35.3686 11.1892 35.0813 10.6254C34.7859 10.0462 33.972 9.25283 33.4135 9.0002ZM13.9243 18.5029C13.3674 17.3145 14.0306 15.8835 15.2874 15.5622C15.7242 15.4504 16.5518 15.5322 16.9313 15.7244C17.3318 15.9275 17.786 16.4104 17.9553 16.8131C18.0196 16.9666 18.0725 17.3236 18.0725 17.6065C18.0725 18.2098 17.9428 18.5602 17.5581 18.9958C16.5502 20.1365 14.5632 19.8671 13.9243 18.5029ZM24.1674 16.7206C24.4365 16.1736 24.8725 15.7847 25.4104 15.6114C25.9168 15.4485 26.7282 15.4998 27.1623 15.7221C27.9034 16.1016 28.3285 16.7883 28.3285 17.6065C28.3285 19.0136 27.022 19.9854 25.5894 19.6438C24.285 19.3328 23.5875 17.8988 24.1674 16.7206Z" fill="white"/>
                </svg>

              </a>
              <a href="#">
                <svg width="42" height="42" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M33.145 13.8427C32.937 12.3432 32.1796 10.9743 31.0195 10.0017C29.8595 9.02901 28.3796 8.52183 26.8668 8.5785C25.354 8.63518 23.9161 9.25167 22.8321 10.3084C21.7481 11.3651 21.0952 12.7868 21 14.2977C14.805 16.8527 8.75 10.5002 8.75 10.5002C7 21.0002 12.25 25.8127 12.25 25.8127C9.87 28.0002 5.25 28.0002 5.25 28.0002C5.25 28.0002 8.015 33.2502 20.265 33.2502C32.515 33.2502 33.25 19.2502 33.25 19.2502C34.404 18.8302 35.38 18.0289 36.0165 16.9787C36.6529 15.9285 36.9117 14.6925 36.75 13.4752C35.5697 13.7553 34.3576 13.8788 33.145 13.8427Z" fill="white"/>
                </svg>

              </a>
            </div>
          </div>
        </div>
      </div>

    </footer>



    <!--<p>is wallet connect : {{is_connect}}</p>-->
    <!--<p>acc ID : {{accId}}</p>-->
    <!--    <q-btn @click="check" label="check"/>-->
    <!--    <q-btn @click="conn" label="connect wallet"/>-->
    <!--    <q-btn @click="connMint({ requestSignIn: true })" label="mint"/>-->
    <!--    <q-input v-model="title" label="title"/>-->
    <!--    <q-input v-model="descr" label="descr"/>-->
    <!--    <q-file v-model="file" label="file"/>-->




  </q-page>
</template>

<script>



import { scroll } from 'quasar'
const { getScrollTarget, setVerticalScrollPosition } = scroll

import { connect, keyStores, WalletConnection }  from  "near-api-js";
// const { connect, keyStores, WalletConnection } = nearAPI;
if (!process.env.SERVER) {
  const keyStore = new keyStores.BrowserLocalStorageKeyStore();
}
import { Wallet, Chain, Network ,MetadataField, } from 'mintbase'
const KEY = '1ba96e51-61f7-4a09-b462-e02f676b6417'
export default {
  data(){
    return {
      wallet: null,
      is_connect: false,
      menuActive: false,
      accId: null,
      title: 'title',
      descr: 'descr',
      file: '',
      faqs:[
        {q:'In which network will the sale take place?',a:'We chose NEAR Protocol as a network in which we could see the development of our project at all its stages.\n'},
        {q:'Which wallet should I use?',a:'To work on the NEAR blockchain, you need to use the official NEAR wallet.'},
        {q:'How much bears can I buy?',a:'Each user has 3 bears available for purchase.\n' +
            'This restriction is made so that each user gets his bear.'},
        {q:'Where can I sell nft?',a:'You can sell your bear on the PARAS marketplace. To do this, it is enough to connect your wallet and register an account.'},
        {q:'How do I access your game?',a:'Unfortunately, the game is currently under development. Now active work is underway, so soon we will be able to present you the first shots.\n' +
            '\n' +
            'In the future, after the release of the game, you will need bears from Tier 2 to access.'},
      ],
      team: [
        {img: 't1.png', link_text: 'Yoon Jang', url: '#', text: 'Art-director'},
        {img: 't2.png', link_text: 'Hong Wooram', url: '#', text: 'Illustrator'},
        {img: 't3.png', link_text: 'Koun Han', url: '#', text: 'Illustrator'},
        {img: 't4.png', link_text: 'Brice Kiyoung Lee', url: '#', text: 'Developer'},


      ],
      collection: [
        {
          img: 'coll/test.png',
          title: 'Lorem ipsum dolor',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Eget sed risus accumsan, magna molestie urna.'
        },
        {
          img: 'coll/test.png',
          title: 'Lorem ipsum dolor',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Eget sed risus accumsan, magna molestie urna.'
        },
        {
          img: 'coll/test.png',
          title: 'Lorem ipsum dolor',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Eget sed risus accumsan, magna molestie urna.'
        },
        {
          img: 'coll/test.png',
          title: 'Lorem ipsum dolor',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Eget sed risus accumsan, magna molestie urna.'
        },
        {
          img: 'coll/test.png',
          title: 'Lorem ipsum dolor',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Eget sed risus accumsan, magna molestie urna.'
        },
        {
          img: 'coll/test.png',
          title: 'Lorem ipsum dolor',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Eget sed risus accumsan, magna molestie urna.'
        },
      ],
      rare_collection: [
        {
          bg_img: 'rare/cartoon_bg.jpg',
          img: 'rare/cartoon_collection.png',
          title1: 'Cartoons heroes',
          title2: '10 NFTs',
          icon: 'icon.png',
          text: 'Extremely rare specimens. This set is a well-known cartoon characters who have nurtured hundreds of thousands of young minds located in the most distant parts of the world.',
          got_text: 'Collect all 3 of 10 -> got',
          got_items: [
            {text: '500 NIER', is_link: false,icon:'near.svg'},
            {text: 'Artwork', is_link: false,icon:'artwork.svg'},
            {text: 'Collection merch', is_link: false,icon:'collection.svg'},
            {text: 'Alpha NFT', is_link: true,icon:'alpha.svg', img: 'rare/Cartoon_Alpha.png'},
          ]
        },//item
        {
          bg_img: 'rare/dc_bg.jpg',
          img: 'rare/dc_collection.png',
          title1: 'DC Champions',
          title2: '10 NFTs',
          icon: 'icon.png',
          text: 'The real justice league!\n' +
            'Here are the champions of the DC universe, valiantly defending our planet from various extraterrestrial invasions and attacks for more than ten years!',
          got_text: 'Collect all 3 of 10 -> got',
          got_items: [
            {text: '500 NIER', is_link: false,icon:'near.svg'},
            {text: 'Artwork', is_link: false,icon:'artwork.svg'},
            {text: 'Collection merch', is_link: false,icon:'collection.svg'},
            {text: 'Alpha NFT', is_link: true,icon:'alpha.svg', img: 'rare/DC_Alpha.png'},
          ]
        },//item
        {
          bg_img: 'rare/genesis_bg.jpg',
          img: 'rare/genesis_collection.png',
          title1: 'Area 51',
          title2: '10 NFTs',
          icon: 'icon.png',
          text: 'In fact, it is not known whether these bears actually exist. Although various photos and videos with their participation are distributed on the network, and the number of witnesses is growing every day, there is no reliable fact of their existence yet.',
          got_text: 'Collect all 3 of 10 -> got',
          got_items: [
            {text: '500 NIER', is_link: false,icon:'near.svg'},
            {text: 'Artwork', is_link: false,icon:'artwork.svg'},
            {text: 'Collection merch', is_link: false,icon:'collection.svg'},
            {text: 'Alpha NFT', is_link: true,icon:'alpha.svg', img: 'rare/Random_Alpha.png'},
          ]
        },//item
        {
          bg_img: 'rare/starwars_bg.jpg',
          img: 'rare/starwars_collection.png',
          title1: 'StarWars',
          title2: '10 NFTs',
          icon: 'icon.png',
          text: 'Luke, I\'m your token…',
          got_text: 'Collect all 3 of 10 -> got',
          got_items: [
            {text: '500 NIER', is_link: false,icon:'near.svg'},
            {text: 'Artwork', is_link: false,icon:'artwork.svg'},
            {text: 'Collection merch', is_link: false,icon:'collection.svg'},
            {text: 'Alpha NFT', is_link: true,icon:'alpha.svg', img: 'rare/Starwars_Alpha.png'},
          ]
        },//item
        {
          bg_img: 'rare/marvel_bg.jpg',
          img: 'rare/marvel_collection.png',
          title1: 'MARVEL Champions',
          title2: '10 NFTs',
          icon: 'icon.png',
          text: 'Knights of the Marvel universe. Representatives of various factions united by one common feature - incredible strength. It\'s worth thinking twice before contacting these guys',
          got_text: 'Collect all 3 of 10 -> got',
          got_items: [
            {text: '500 NIER', is_link: false,icon:'near.svg'},
            {text: 'Artwork', is_link: false,icon:'artwork.svg'},
            {text: 'Collection merch', is_link: false,icon:'collection.svg'},
            {text: 'Alpha NFT', is_link: true,icon:'alpha.svg', img: 'rare/Marvel_Alpha.png'},
          ]
        },//item
        {
          bg_img: 'rare/ufo_bg.jpg',
          img: 'rare/ufo_collection.png',
          title1: 'ChebuAliens',
          title2: '10 NFTs',
          icon: 'icon.png',
          text: 'A race of extraterrestrial ChebuBears living on the planet QuinQue World. It is not completely clear whether they are hostile or not. All the ships sent for research disappeared without a trace in the cosmic ocean, leaving behind only mysterious photos',
          got_text: 'Collect all 3 of 10 -> got',
          got_items: [
            {text: '500 NIER', is_link: false,icon:'near.svg'},
            {text: 'Artwork', is_link: false,icon:'artwork.svg'},
            {text: 'Collection merch', is_link: false,icon:'collection.svg'},
            {text: 'Alpha NFT', is_link: true,icon:'alpha.svg', img: 'rare/ufo_Alpha.png'},
          ]
        },//item
        {
          bg_img: 'rare/misfits_bg.jpg',
          img: 'rare/misfits_collection.png',
          title1: 'Reverse Side',
          title2: '10 NFTs',
          icon: 'icon.png',
          text: 'The reverse side of the ChebuVerse. Those who were not accepted by the usual society of bears gathered here. They were forced to get together in a group in order to somehow survive, and all the poisoning interests in common served as an excellent basis for their union.',
          got_text: 'Collect all 3 of 10 -> got',
          got_items: [
            {text: '500 NIER', is_link: false,icon:'near.svg'},
            {text: 'Artwork', is_link: false,icon:'artwork.svg'},
            {text: 'Collection merch', is_link: false,icon:'collection.svg'},
            {text: 'Alpha NFT', is_link: true,icon:'alpha.svg', img: 'rare/badguys_Alpha.png'},
          ]
        },//item
        {
          bg_img: 'rare/zombie_bg.jpg',
          img: 'rare/zombie_collection.png',
          title1: 'Nightmares',
          title2: '10 NFTs',
          icon: 'icon.png',
          text: 'The scariest representatives of ChebuBears. Living in utter darkness and feeding on other people\'s fears, they terrify all living beings from the moment of their birth.',
          got_text: 'Collect all 3 of 10 -> got',
          got_items: [
            {text: '500 NIER', is_link: false,icon:'near.svg'},
            {text: 'Artwork', is_link: false,icon:'artwork.svg'},
            {text: 'Collection merch', is_link: false,icon:'collection.svg'},
            {text: 'Alpha NFT', is_link: true,icon:'alpha.svg', img: 'rare/Zombie_Alpha.png'},
          ]
        },//item

      ],
      journey: [
        {
          img: 'j-1.png',
          is_done: true,
          need_border: true,
          date: 'Q4 2021',
          title: 'concept and design',
          text: 'The design idea of our model was borrowed directly from its Soviet original. \n' +
            'Here we have interwoven modern artistic canons in order to satisfy the visual needs of the present time\n'
        },//item
        {
          img: false,
          is_done: true,
          need_border: true,
          date: 'JANUARY–FEBRUARY 2022',
          title: 'website development',
          text: 'An important part of any modern history is the website.\n' +
            '\n' +
            'In fact, the website is a passport of the project, with which the user can get acquainted with all the information he is interested in. \n' +
            'The fruits of our labors will be demonstrated here to the whole world\n'
        },//item
        {
          img: 'j-2.png',
          is_done: true,
          need_border: true,
          date: 'FEBRUARY 2022',
          title: 'candy machine and creation of NFT under NeaR',
          text: 'Our NFTs are randomly generated using a candy machine, the exceptions to the rules are genesis and alpha collections. \n' +
            'Our cubs will be located in the NEAR Protocol\n'
        },//item
        {
          img: 'j-3.png',
          is_done: true,
          need_border: true,
          date: 'MARCH 2022',
          title: 'community',
          text: 'The community is something we have made a special emphasis on. Art is certainly the main business of our life, but without you, modern connoisseurs, this art would simply have no one to exist for. Realizing this, we try to build friendly relations both with the participants of our project and with the crypto community\n'
        },//item
        {
          img: 'j-4.png',
          is_done: false,
          need_border: true,
          date: 'MARCH 11 2022',
          title: 'Opening of sales: Tier 1',
          text: 'The actual day on which the start of sales of our collection is scheduled.\n' +
            'There will be 3333 bears in total, located in the NEAR blockchain\n' +
            'To access the purchase, you will be asked to go through a simple Google form\n'
        },//item
        {
          img: false,
          is_done: false,
          need_border: true,
          date: 'MARCH 2022',
          title: 'Giveaways',
          text: 'For you, dear participants of our project, we have planned constant giveaways. Gifts can be very different, ranging from roles in the discord and ending with gifts in the form of our own sword, which we will kindly deliver to your door'
        },//item
        {
          img: false,
          is_done: false,
          need_border: true,
          date: 'MARCH 2022',
          title: 'Start of Soft Toys Production',
          text: 'Each ChebuBear holder can order a physical adaptation of their model.\n' +
            'That is, your ChebuBear is actually a document, using which you can request a soft toy directly\n' +
            'from our workshop.\n' +
            '\n' +
            'Each toy will be made in its own individual style, so you can rightfully be called a real collector - only you have such a thing'
        },//item
        {
          img: false,
          is_done: false,
          need_border: true,
          date: 'MARCH 2022',
          title: 'Stacking technology',
          text: 'Subsequently, after the first village, we will introduce the technology of stacking your bears, with the help of which each of the holders will\n' +
            'have the opportunity to put their ChebuBears into operation in order to receive rewards'
        },//item
        {
          img: 'j-5.png',
          is_done: false,
          need_border: false,
          date: 'APRIL 2022',
          title: 'Opening of sales: Tier 2',
          text: 'A unique collection of bears, consisting of 2222 bears. This collection comes out together with an RPG-style game-a walker, access to which will be possible only when you connect a wallet containing bears from Tier 1.\n'
        },//item

      ],
      settings_top: {
        itemsToShow: 1,
        loop:true,

        snapAlign: 'center',
      },
      // breakpoints are mobile first
      // any settings not specified will fallback to the carousel settings
      breakpoints_top: {
        // 700px and up
        200: {
          itemsToShow: 2,
          snapAlign: 'center',
        },
        600: {
          itemsToShow: 3,
          snapAlign: 'center',
        },
        // 1024 and up
        1024: {
          itemsToShow: 4,
          snapAlign: 'start',
        },
      },
      settings_bottom: {
        itemsToShow: 1,
        snapAlign: 'center',
      },
      // breakpoints are mobile first
      // any settings not specified will fallback to the carousel settings

    }
  },

  async mounted() {
    console.log('mount')
    // const near = await connect(
    //   {
    //     networkId: "testnet",
    //     keyStore, // optional if not signing transactions
    //     nodeUrl: "https://rpc.testnet.near.org",
    //     walletUrl: "https://wallet.testnet.near.org",
    //     helperUrl: "https://helper.testnet.near.org",
    //     explorerUrl: "https://explorer.testnet.near.org",
    //   }
    // )
    // this.wallet = new WalletConnection(near,'Mintbase.js');
  },

  methods:{
    scrollToElement (el) {
      const ref = this.$refs[el]
      const target = getScrollTarget(ref)

      const offset = ref.offsetTop
      console.log(offset)
      const duration = 500
      setVerticalScrollPosition(target, offset, duration)
    },
    async conn(){
      console.log('dd')

      await this.wallet.requestSignIn(
        "ddnnsstest.mintspace2.testnet", // contract requesting access
        "Example App", // optional
        "http://localhost:8081", // optional
        "http://localhost:8081" +
        "" // optional
      );
    },
    async check(){
      console.log('w',this.wallet)
      console.log('w',this.wallet.getAccountId())
      console.log('wallet.isSignedIn()',this.wallet.isSignedIn())
      console.log('wallet.account',this.wallet.account())
      if(this.wallet.isSignedIn()){
        this.is_connect = true

      }

    },
    async connMint() {

      const { data: walletData, error } = await new Wallet().init({
        networkName: Network.testnet,
        chain: Chain.near,
        apiKey: KEY,
      })

      const { wallet, isConnected } = walletData
      console.log('walletData',walletData)


      if (isConnected) {
        const {data: details} = await wallet.details()
        console.log(details)
      }
      const {data: uploadResponse,error1:uploadError} = await wallet?.minter?.uploadField(MetadataField.Media,this.file)
      console.log('data',uploadResponse)
      console.log('error1',uploadError)
      wallet?.minter?.setMetadata({
        title:this.title,
        description:this.descr
      })

      console.log(wallet.minter.currentMint)
      wallet.mint(1,'ddnnsstest.mintspace2.testnet',undefined,undefined,'test')

    },



  }
}
</script>
<style lang="sass">
.text-practice
  font-family: 'Practice', sans-serif
.text-upper
  text-transform: uppercase
.text-35
  font-size: 35px
.text-48
  font-size: 48px
  line-height: 54px
.text-72
  font-size: 72px
  line-height: 81px
.text-96
  font-size: 72px
  line-height: 126px
.text-18
  font-size: 18px
.text-24
  font-size: 23px
  line-height: 43px
  font-weight: 500
.text-w
  color: white
.text-b
  color: black
.text-blue
  color: #4546EA !important
.text-gr
  color: #00AD80
.text-ye
  color: #D6C000
.text-r1
  color: #FF7F5C
.text-r2
  color: #FF3789


.text-w-shadow-b
  text-shadow: 5px 6px black

.text-w-shadow-w
  text-shadow: 5px 6px white
.text-center
  text-align: center
.mr-20
  margin-right: 20px
.mr-15
  margin-right: 15px
.mb-30
  margin-bottom: 30px

.mb-45
  margin-bottom: 45px
.mb-80
  margin-bottom: 80px
.mb-100
  margin-bottom: 100px !important

.button
  border-radius: 36px
  font-family: 'Practice', sans-serif
  font-size: 24px
  line-height: 100%
  display: inline-block
  padding: 24px 78px
  text-align: center
  cursor: pointer
  user-select: none
  box-shadow: 5px 5px 0 0 #ffffff
  &.green
    background: #8FFF91
    color: black
  &.blue
    background: #4546EA
    color: white
  &.bl-sh
    box-shadow: 5px 5px 0 0 #000

.container
  max-width: 1200px
  padding: 0 10px
  margin: 0 auto
  position: relative
@media (max-width: 900px)
  .text-96
    font-size: 48px
    line-height: 62px
  .text-72
    font-size: 48px
    line-height: 62px
  .text-48
    font-size: 24px
    line-height: 27px
  .text-24
    font-size: 17px
    line-height: 27px
  .button
    font-size: 18px
    padding: 15px 50px
.header
  display: flex
  align-items: center
  justify-content: space-between

  &.top
    position: absolute
    width: 100%
    padding-top: 40px
  &.bottom
    padding: 100px 0
  &-inner
    display: flex
    align-items: center
    justify-content: space-between
    flex-basis: 670px
  & .nav
    flex-basis: 470px
    ul
      flex-basis: 470px
      display: flex
      align-items: center
      justify-content: space-between
      li
        cursor: pointer

@media (max-width: 900px)
  .header
    &.bottom
      flex-wrap: wrap
      flex-direction: column
      & .text-practice
        margin-bottom: 80px
      & .header-inner
        flex-basis: unset
        flex-direction: column
        align-items: center
        justify-content: center
      & .nav
        flex-basis: unset
        ul
          flex-direction: column
          flex-basis: unset
          padding: 0
          li
            margin-bottom: 20px

.section_top
  display: block
  width: 100%
  height: auto
.offer
  background: url(~assets/offer-bg.png) no-repeat center
  background-size: cover
  padding-top: 170px
  text-align: center
  padding-bottom: 200px
  &-img
    background: url(~assets/offer-img.png) no-repeat center
    height: 408px
    width: 408px
    margin: 0 auto 80px
    display: flex
    padding: 40px
    align-items: center
    justify-content: center

  &-text
    max-width: 812px
    margin: 0 auto 60px
  &-bottom
    display: flex
    align-items: center
    justify-content: space-between
    max-width: 965px
    margin: 0 auto
    border: 2px solid #FFFFFF
    box-sizing: border-box
    border-radius: 42px
    padding: 15px 60px
@media (max-width: 900px)
  .offer
    &-img
      width: 200px
      height: 200px
      background-size: contain
      padding: 20px
      margin-bottom: 60px
    &-text
      font-size: 18px
      line-height: 32px
    &-bottom
      flex-wrap: wrap
      padding: 15px 30px
      align-items: center
      justify-content: center
      flex-direction: column
      p
        margin-bottom: 40px !important
.collection
  padding: 100px 0 100px 0
  background: url(~assets/bg_2.png) repeat-y center
  background-size: cover
  margin-top: -1px

  &-wrapper
    position: relative
    & .prev-btn
      position: absolute
      left: -120px
      top: 100px
      cursor: pointer
      svg
        circle
          fill: #FFFFFF
          transition: all .2s linear
        path
          stroke: #4546EA
          transition: all .2s linear
      &:hover
        svg
          circle
            fill: #4546EA
          path
            stroke: #FFFFFF
    & .next-btn
      position: absolute
      right: -120px
      top: 100px
      cursor: pointer
      svg
        circle
          transition: all .2s linear
          fill: #FFFFFF
        path
          transition: all .2s linear
          stroke: #4546EA
      &:hover
        svg
          circle
            fill: #4546EA
          path
            stroke: #FFFFFF

  &-item
    img
      border-radius: 24px
      margin-bottom: 15px
      width: 276px
      height: 276px
      object-fit: contain

    &__title
      text-align: center
      font-family: 'Practice', sans-serif
      color: black
      margin-bottom: 15px
    &__text
      text-align: center
      font-weight: 400
      line-height: 25px
@media (max-width: 900px)
  .collection
    &-wrapper
      margin: 0 -10px
    &-item
      img
        width: 160px
        height: 160px

.rare-collection
  padding: 120px 0 200px 0
  background: url(~assets/bg_3.png) no-repeat center
  background-size: cover
  margin-top: -1px

  &-wrapper
    position: relative
    max-width: 1140px
    margin: 0 auto
    & .prev-btn
      position: absolute
      left: -120px
      top: 280px
      cursor: pointer
      svg
        circle
          fill: #FFFFFF
          transition: all .2s linear
        path
          stroke: #4546EA
          transition: all .2s linear
      &:hover
        svg
          circle
            fill: #4546EA
          path
            stroke: #FFFFFF
    & .next-btn
      position: absolute
      right: -120px
      top: 280px
      cursor: pointer
      svg
        circle
          transition: all .2s linear
          fill: #FFFFFF
        path
          transition: all .2s linear
          stroke: #4546EA
      &:hover
        svg
          circle
            fill: #4546EA
          path
            stroke: #FFFFFF
  &-item
    width: 100%
    & .button
      position: relative
      top: -5px
    &__bottom
      background: #FFFFFF
      border-radius: 24px
      padding: 40px
      overflow: hidden
    &__img-wrapper
      margin-bottom: 30px
    &__img-inner
      width: 100%
      height: 600px
      background-size: cover !important
      border-radius: 36px
      display: flex
      flex-direction: column
      align-items: center
      justify-content: center
      padding-top: 50px
      img
        display: inline-block !important
        width: unset !important
        max-width: unset !important
        height: unset

    &__title
      display: flex
      align-items: center
      margin-bottom: 20px
      img
        display: inline-block !important
        width: 32px !important
        max-width: unset !important
        height: 32px
        object-fit: contain
    &__text
      position: relative
      max-width: 625px
      line-height: 25px
      margin-bottom: 50px
      text-align: left
      &::after
        position: absolute
        content: ''
        width: 500%
        height: 2px
        background: #68EDCB
        left: -40px
        bottom: -25px
    &__got
      margin-bottom: 30px
      display: flex
      align-items: center
      & .text-black
        margin-right: 40px
      &-item
        position: relative
        display: flex
        background: #FFFFFF
        border: 2px solid #4546EA
        color: #4546EA
        box-sizing: border-box
        border-radius: 8px
        padding: 8px 12px
        font-size: 14px
        margin-right: 15px
        font-weight: 500
        &.has_link
          position: relative
          background: #4546EA
          p
            color: #fff
            cursor: pointer
          &:hover > div
            opacity: 1
            transition: opacity .2s linear

        &-img
          position: absolute
          opacity: 0
          width: 200px
          height: 200px
          object-fit: contain
          left: 50%
          bottom: 143%
          transform: translatex(-50%)
          img
            width: 200px
            height: 200px
            object-fit: contain

@media (max-width: 900px)
  .rare-collection
    &-item__img-inner
      height: 350px
      padding: 30px
      img
        width: 100%
        height: 100%
    &-item
      &__bottom
        padding: 20px
        & .text-left
          text-align: center !important
      &__title
        flex-wrap: wrap
        font-size: 24px
        line-height: 38px
        p:first-child
          flex-basis: 100%
          text-align: left
      &__text
        font-size: 14px
        line-height: 22px
      &__got
        flex-wrap: wrap
        p:first-child
          flex-basis: 100%
          text-align: left
          margin-bottom: 10px
        &-item
          margin-bottom: 10px
          &-img
            width: 300px
            height: 300px
            left: 0
            transform: unset
            img
              width: 300px
              height: 300px


.journey
  padding: 100px 0
  background: url(~assets/bg_4.png) repeat-y center

  margin-top: -1px
  position: relative
  &-img-l
    position: absolute
    left: 40px
    top: 50px
  &-img-r
    position: absolute
    right: 40px
    bottom: 50px
  &-wrapper
    max-width: 812px
    margin: 0 auto
  &-grid
    display: grid
    grid-template-columns: 1fr
    grid-gap: 40px
  &-item
    display: grid
    grid-template-columns: 1fr 2fr
    grid-gap: 30px
    &__img
      img
        border-radius: 24px
    &__info
      position: relative
      //height: fit-content
      min-height: 224px
      &.w-border
        &::before
          position: absolute
          content: ''
          width: 2px
          height: 95%
          left: -27px
          top: 35px
          background: white
      &-date
        position: relative
        color: #8FFF91
        margin-bottom: 40px
        &::before
          position: absolute
          content: url(~assets/dot.svg)
          left: -30px
        &.negative
          color: #EF5D5D
        &.done
          padding-left: 40px
          &::after
            position: absolute
            left: 0px
            content: url(~assets/done.svg)
      &-title
        margin-bottom: 24px
        font-family: "Practice",sans-serif
        font-size: 24px
      &-text
        line-height: 25px

@media (max-width: 900px)
  .journey

    &-item
      grid-template-columns: 1fr
      padding-left: 45px
      &__img
        display: none
      &__info
        &-text
          font-size: 14px
          line-height: 22px
          margin-bottom: 20px




.team
  padding: 100px 0
  background: url(~assets/bg_5.png) repeat-y center
  &-grid
    //max-width: 870px
    //margin: 0 auto 80px
    display: grid
    grid-template-columns: 1fr 1fr 1fr 1fr
    margin-bottom: 80px
    grid-gap: 100px
  &-item
    text-align: center
    img
      border-radius: 100%
      width: 220px
      height: 220px
      object-fit: contain
      margin-bottom: 30px
    &__link
      display: flex
      align-items: center
      justify-content: center
      font-weight: 700
      color: black
      margin-bottom: 10px
      img
        width: 24px
        height: 24px
        margin-bottom: 0 !important
        margin-right: 10px


//&::before
//  position: absolute
//  content: url(~assets/dis.svg)
//  left: -30px
//&:hover
//  color: #4546EA
//  &:before
//    content: url(~assets/dis1.svg)

@media (max-width: 900px)
  .team-grid
    grid-template-columns: 1fr
    grid-gap: 60px

.faq
  padding: 100px 0
  background: url(~assets/bg_6.png) no-repeat center
  &-wrapper
    position: relative
    max-width: 870px
    margin: 0 auto
    &::before
      position: absolute
      content: url(~assets/faq-img.png)
      left: -20%
      top: -160px
@media (max-width: 900px)
  .faq
    &-wrapper
      &::before
        content: none
.social
  padding: 100px 0 400px 0
  background: url(~assets/bg_7.png) no-repeat center
  & .mb-45
    position: relative
    z-index: 0
    &::after
      position: absolute
      content: url(~assets/star1.svg)
      bottom: -100%
      left: 50%
      transform: translateX(-50%)
      z-index: -1
  & .mb-100
    position: relative
    z-index: 0
    &::after
      position: absolute
      content: url(~assets/star2.svg)
      bottom: -60%
      left: 50%
      transform: translateX(-50%)
      z-index: -1
@media (max-width: 900px)
  .social
    & .mb-100
      &::after
        left: unset
        right: -40px
        bottom: -30%
.footer
  position: relative
  background: url(~assets/footer_bg.png) repeat-y center
  &::before
    position: absolute
    content: url(~assets/footer.png)
    top: -312px
    left: 50%
    transform: translateX(-50%)
@media (max-width: 900px)
  .footer
    &::before
      content: url(~assets/footer-sm.png)
      top: -130px

.rarity
  background: url(~assets/bg_3.png) repeat-y center
  padding: 100px 0

  &-wrapper
    background: #FFFFFF
    border-radius: 24px
    padding: 60px
  &-grid
    padding: 20px 0
    display: grid
    grid-template-columns: 1fr 1fr
    border-bottom: 2px solid
    border-color: #B8B8BB
    &.b-b
      border-color: #7063FF
@media (max-width: 900px)
  .rarity
    &-wrapper
      padding: 20px
</style>

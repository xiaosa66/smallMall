<template>
  <div class="app-init home-index">
    <header class="public-header">
      <form class="search-box clear">
        <div class="fl logo">
          <!--          <span class="iconfont icon-xiaomi"></span>-->
          <img style="border-radius: 50%;margin-top: 0.1rem; "
               src="https://zuifeiyi-1258006205.cos.ap-beijing.myqcloud.com/article/zuifeiyiLogo.jpeg" alt="">
        </div>
        <div class="input-box" @click="$router.openPage('/search')">
          <span class="iconfont icon-sousuo-copy absolute"></span>
          <input type="text" class="input-controller" placeholder="搜索商品名称" readonly>
        </div>
        <div class="myself-center fr" @click="$router.openPage('/mine')">
          <span class="iconfont icon-smile"></span>
        </div>
      </form>
      
      <nav class="menu-box scroll-box-x noscroll">
        <ul class="wrap-box clear">
          <li class="item" :class="{ 'active' : index == navListActiveIndex }" v-for="(value, index) in navList"
              @click="navChange(index)" :key="index">
            <span>{{value.name}}</span>
          </li>
        </ul>
      </nav>
    </header>
    <div ref="view01" class="app-init scroll-box tab-box mi-tj footer-hack" v-show="navListActiveIndex == 0">
      <!--      <swiper :list="bannerList"></swiper>-->
      <div class="shop-item">
        <img src="http://qiniu.verydog.cn//show.liluo.cc/2018011316464243450.png" alt="">
        
        <div class="shop-box clear">
          <div class="shop-box-item" v-for="(target, index) in shoplist" :key="index"
               @click="$router.openPage(target.href)">
            <img v-lazy="target.src" alt="">
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        
        </div>
      </div>
    </div>
    
    <div ref="view02" class="app-init scroll-box tab-box footer-hack" v-show="navListActiveIndex == 1">
      <!--      <swiper :list="bannerList01"></swiper>-->
      
      <div class="shop-item">
        <div class="shop-box clear">
          <div class="shop-box-item" v-for="(target, index) in shoplist01" :key="index"
               @click="$router.openPage(target.href)">
            <img v-lazy="target.src" alt="">
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        </div>
      </div>
    </div>
    
    <div ref="view03" class="app-init scroll-box tab-box footer-hack" v-show="navListActiveIndex == 2">
      <!--      <swiper :list="bannerList02"></swiper>-->
      <div class="shop-item">
        <div class="shop-box clear">
          <div class="shop-box-item" v-for="(target, index)  in shoplist02" :key="index"
               @click="$router.openPage(target.href)">
            <img v-lazy="target.src" alt="">
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        </div>
      </div>
    </div>
    
    <div ref="view04" class="app-init scroll-box tab-box footer-hack" v-show="navListActiveIndex == 3">
      <!--      <swiper :list="bannerList03"></swiper>-->
      <div class="shop-item">
        <div class="shop-box clear">
          <div class="shop-box-item" v-for="(target, index)  in shoplist03" :key="index"
               @click="$router.openPage(target.href)">
            <img v-lazy="target.src" alt="">
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        </div>
      </div>
    </div>
    
    <div ref="view05" class="app-init scroll-box tab-box footer-hack" v-show="navListActiveIndex == 4">
      <!--      <swiper :list="bannerList04"></swiper>-->
      <div class="shop-item">
        <img src="http://qiniu.verydog.cn//show.liluo.cc/2018011316464243450.png" alt="">
        <div class="shop-box clear">
          <div class="shop-box-item" v-for="(target, index) in shoplist04" :key="index"
               @click="$router.openPage(target.href)">
            <img v-lazy="target.src" alt="">
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        </div>
      </div>
    </div>
    
    <div ref="view06" class="app-init scroll-box tab-box footer-hack" v-show="navListActiveIndex == 5">
      <img v-lazy="'http://qiniu.verydog.cn//show.liluo.cc/2018011317010732422.png'"
           @click="$router.openPage('/detail/1003')" alt="">
      <img v-lazy="'http://qiniu.verydog.cn//show.liluo.cc/48ca6cfb19c45e7cbecbd8c34c757445.jpg'" alt="">
      <img v-lazy="'http://qiniu.verydog.cn//show.liluo.cc/2018011317012799998.png'" alt="">
      <img v-lazy="'http://qiniu.verydog.cn//show.liluo.cc/2018011317013522274.png'" alt="">
      <img v-lazy="'http://qiniu.verydog.cn//show.liluo.cc/2018011317005752430.png'" alt="">
      <img v-lazy="'http://qiniu.verydog.cn//show.liluo.cc/2018011317011947232.png'" alt="">
      <img v-lazy="'http://qiniu.verydog.cn//show.liluo.cc/2018011317014434073.png'" alt="">
    </div>
    
    <div ref="view07" class="app-init scroll-box tab-box footer-hack" v-show="navListActiveIndex == 6">
      <swiper :list="bannerList06"></swiper>
      <div class="shop-item">
        <img src="http://qiniu.verydog.cn//show.liluo.cc/2018011316464243450.png" alt="">
        <div class="shop-box clear">
          <div class="shop-box-item" v-for="(target, index) in shoplist06" :key="index"
               @click="$router.openPage(target.href)">
            <img v-lazy="target.src" alt="">
            <p class="title">{{ target.title }}</p>
            <p class="con">{{ target.con }}</p>
            <p class="money">
              <span class="small">￥</span> {{ target.money }}
            </p>
          </div>
        </div>
      </div>
    </div>
  
  
  </div>
</template>

<script type="text/ecmascript-6">
    import swiper from '../../components/swiper'
    import VueDB from '../../util/vue-db/vue-db'

    let DB = new VueDB()

    export default {
        data() {
            return {
                bannerList: [
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/01.png',
                        href: '/detail/1001'
                    },
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/02.jpg',
                        href: '/detail/1002'
                    },
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/03.jpg',
                        href: '/detail/1003'
                    },
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/04.jpg',
                        href: '/detail/1004'
                    }
                ],
                shoplist: [
                    {
                        src: 'https://si.geilicdn.com/wdseller502441367-76e700000168055f4f1b0a216239_1242_1656.jpg.webp?w=750&h=750&cp=1',
                        title: '四季剪纸小夜灯DIY材料包',
                        con: '举步之明，光明立现',
                        money: 120,
                        href: '/detail/1008'
                    },
                    {
                        src: 'https://si.geilicdn.com/vshop502441367-1459596511577-99b5c-s1.jpg.webp?w=750&h=750&cp=1',
                        title: '原创螺旋发插「一枝梅」',
                        con: '材料：铜、合金、料器',
                        money: 118,
                        href: '/detail/1017'
                    },
                    {
                        src: 'https://si.geilicdn.com/wdseller502441367-2b0d0000016c369abe430a20b7b9_1242_1656.jpg.webp?w=640&h=400',
                        title: '【天然蓝染◆丝毛围巾】',
                        con: '幽远深邃，亦带明媚清浅',
                        money: 448,
                        href: '/detail/1009'
                    },
                    {
                        src: 'https://si.geilicdn.com/vshop502441367-1492431421288-DA992-s1.jpg.webp?w=750&h=750&cp=1',
                        title: '昆曲工尺谱文身贴纸2.0',
                        con: '原创设计 |《牡丹亭》',
                        money: 20,
                        href: '/detail/1019'
                    },
                    {
                        src: 'https://si.geilicdn.com/bj-wd-502441367-1516804927220-1554607960_1080_1440.jpg.webp?w=750&h=750&cp=1',
                        title: '原创耳坠「红泪」一对',
                        con: '材料：黄铜、玛瑙珠',
                        money: 89,
                        href: '/detail/1012'
                    },
                    {
                        src: 'https://si.geilicdn.com/forward502441367-5c82000001674ec8a1ec0a028841_1656_1242.jpg.webp?w=750&h=750&cp=1',
                        title: '2019剪纸创意年历',
                        con: '原创设计｜（礼盒装）',
                        money: 119,
                        href: '/detail/1010'
                    },
                    {
                        src: 'https://si.geilicdn.com/bj-wd-502441367-1535043967603-635916044_1686_1264.jpg.webp?w=750&h=750&cp=1',
                        title: '原创发夹/胸针「蓝莲花」',
                        con: '手工布艺作品',
                        money: 49,
                        href: '/detail/1011'
                    }
                ],
                navList: [
                    {
                        name: '店长推荐'
                    },
                    {
                        name: '耳上明月铛'
                    },
                    {
                        name: '发间多宝簪'
                    },
                    {
                        name: '手工材料包'
                    },
                    {
                        name: '其他'
                    }
                ],
                navListActiveIndex: 0,

                bannerList01: [
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/1888a9f0a6ae807113cb428b9e01f5fe.jpg',
                        href: '/detail/1007'
                    },
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011213275295675.png',
                        href: '/detail/1009'
                    }
                ],
                shoplist01: [
                    {
                        src: 'https://si.geilicdn.com/bj-wd-502441367-1516804927220-1554607960_1080_1440.jpg.webp?w=750&h=750&cp=1',
                        title: '原创耳坠「红泪」一对',
                        con: '材料：黄铜、玛瑙珠',
                        money: 89,
                        href: '/detail/1012'
                    },
                    {
                        src: 'https://si.geilicdn.com/vshop502441367-1455549882483-47999-s18.jpg.webp?w=750&h=750&cp=1',
                        title: '原创耳坠「莲华胜」一对',
                        con: '材料：黄铜、玉珠',
                        money: 89,
                        href: '/detail/1013'
                    }, {
                        src: 'https://si.geilicdn.com/bj-wd-502441367-1516775441109-1717797430_1080_739.jpg.webp?w=750&h=750&cp=1',
                        title: '原创耳坠「翠铃铎」一对',
                        con: '材料：黄铜、玉珠',
                        money: 89,
                        href: '/detail/1014'
                    }
                ],

                bannerList02: [
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011213533255816.png',
                        href: '/detail/1011'
                    }
                ],
                shoplist02: [
                    {
                        src: 'https://si.geilicdn.com/vshop502441367-1459687041476-86bed-s1.jpg.webp?w=750&h=750&cp=1',
                        title: '原创发簪「金萼」',
                        con: ' 材料：黄铜',
                        money: 289,
                        href: '/detail/1015'
                    },
                    {
                        src: 'https://si.geilicdn.com/vshop502441367-1459597245772-fe567-s1.jpg.webp?w=750&h=750&cp=1',
                        title: '原创发钗「白梅香」银色款',
                        con: '材料：天然淡水珍珠、黄铜',
                        money: 249,
                        href: '/detail/1016'
                    },
                    {
                        src: 'https://si.geilicdn.com/vshop502441367-1459596511577-99b5c-s1.jpg.webp?w=750&h=750&cp=1',
                        title: '原创螺旋发插「一枝梅」',
                        con: '材料：铜、合金、料器',
                        money: 118,
                        href: '/detail/1017'
                    },
                    {
                        src: 'https://si.geilicdn.com/vshop502441367-1459436965337-43774-s1.jpg.webp?w=750&h=750&cp=1',
                        title: '原创发簪「小荷」',
                        con: '小荷才露尖尖角',
                        money: 138,
                        href: '/detail/1018'
                    }
                ],

                bannerList03: [
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2bf70582edb45d83d7120a22c87200c9.jpg',
                        href: '/detail/1013'
                    }
                ],
                shoplist03: [
                    {
                        src: 'https://si.geilicdn.com/wdseller502441367-76e700000168055f4f1b0a216239_1242_1656.jpg.webp?w=750&h=750&cp=1',
                        title: '四季剪纸小夜灯DIY材料包',
                        con: '举步之明，光明立现',
                        money: 120,
                        href: '/detail/1008'
                    }
                ],

                bannerList04: [
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011316542272196.png',
                        href: '/detail/1014'
                    }
                ],
                shoplist04: [
                    {
                        src: 'https://si.geilicdn.com/vshop502441367-1492431421288-DA992-s1.jpg.webp?w=750&h=750&cp=1',
                        title: '昆曲工尺谱文身贴纸',
                        con: '原创设计 |《牡丹亭》',
                        money: 20,
                        href: '/detail/1019'
                    },
                    {
                        src: 'https://si.geilicdn.com/vshop502441367-1465742778315-EC5E0-s1.jpg.webp?w=750&h=750&cp=1',
                        title: '《诗经》明刻本·文身贴纸',
                        con: '原创设计 |《诗经》',
                        money: 20,
                        href: '/detail/1020'
                    }
                ],

                bannerList06: [
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011317083831934.png',
                        href: '/detail/1015'
                    }
                ],
                shoplist06: [
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011317083193859.png',
                        title: '8H护颈乳胶枕 Z2',
                        con: '多重新科技  升级好睡眠',
                        money: 239,
                        href: '/detail/1016'
                    },
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011317083193859.png',
                        title: '8H护颈乳胶枕 Z2',
                        con: '多重新科技  升级好睡眠',
                        money: 239,
                        href: '/detail/1016'
                    },
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011317083193859.png',
                        title: '8H护颈乳胶枕 Z2',
                        con: '多重新科技  升级好睡眠',
                        money: 239,
                        href: '/detail/1016'
                    },
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011317083193859.png',
                        title: '8H护颈乳胶枕 Z2',
                        con: '多重新科技  升级好睡眠',
                        money: 239,
                        href: '/detail/1016'
                    },
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011317083193859.png',
                        title: '8H护颈乳胶枕 Z2',
                        con: '多重新科技  升级好睡眠',
                        money: 239,
                        href: '/detail/1016'
                    },
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011317083193859.png',
                        title: '8H护颈乳胶枕 Z2',
                        con: '多重新科技  升级好睡眠',
                        money: 239,
                        href: '/detail/1015'
                    }
                ],

                bannerList07: [
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011317121511939.png',
                        href: '/detail/1017'
                    }
                ],
                shoplist07: [
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011317120865819.png',
                        title: '小米影视会员卡',
                        con: '畅享海量片库',
                        money: 498,
                        href: '/detail/1018'
                    },
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011317120865819.png',
                        title: '小米影视会员卡',
                        con: '畅享海量片库',
                        money: 498,
                        href: '/detail/1018'
                    },
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011317120865819.png',
                        title: '小米影视会员卡',
                        con: '畅享海量片库',
                        money: 498,
                        href: '/detail/1018'
                    },
                    {
                        src: 'http://qiniu.verydog.cn//show.liluo.cc/2018011317120865819.png',
                        title: '小米影视会员卡',
                        con: '畅享海量片库',
                        money: 498,
                        href: '/detail/1018'
                    }
                ]
            }
        },
        components: {
            swiper
        },
        mounted() {
            // 笨方法，设置N个盒子的scroll top

            this.navListActiveIndex = DB.getItemOnce('home-index-nowIndex').toNumber() || 0

            setTimeout(() => {
                this.$refs.view01.scrollTop = DB.getItemOnce('home-index-view01').toNumber() || 0
                this.$refs.view02.scrollTop = DB.getItemOnce('home-index-view02').toNumber() || 0
                this.$refs.view03.scrollTop = DB.getItemOnce('home-index-view03').toNumber() || 0
                this.$refs.view04.scrollTop = DB.getItemOnce('home-index-view04').toNumber() || 0
                this.$refs.view05.scrollTop = DB.getItemOnce('home-index-view05').toNumber() || 0
                this.$refs.view06.scrollTop = DB.getItemOnce('home-index-view06').toNumber() || 0
                this.$refs.view07.scrollTop = DB.getItemOnce('home-index-view07').toNumber() || 0
            }, 10)


        },
        methods: {
            navChange(index) { // 导航栏切换
                this.navListActiveIndex = index;
            }
        },
        beforeRouteLeave(to, from, next) {
            DB.setItem('home-index-view01', this.$refs.view01.scrollTop)
            DB.setItem('home-index-view02', this.$refs.view02.scrollTop)
            DB.setItem('home-index-view03', this.$refs.view03.scrollTop)
            DB.setItem('home-index-view04', this.$refs.view04.scrollTop)
            DB.setItem('home-index-view05', this.$refs.view05.scrollTop)
            DB.setItem('home-index-view06', this.$refs.view06.scrollTop)
            DB.setItem('home-index-view07', this.$refs.view07.scrollTop)

            DB.setItem('home-index-nowIndex', this.navListActiveIndex)
            next();
        }
    }
</script>

<style type="text/sass" lang="sass">
  
  .home-index .tab-box
    top: 2.5rem
    
    .home-index .tab-box.mi-tj .nav-mi-tj a
      display: block
      width: 25%
    
    .home-index .shop-box
      background-color: #fff

</style>

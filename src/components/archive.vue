<template>
    <div class="animated fadeIn">
        <ty-title
            :title="title"
        />
        <ul class="items archives">
            <li v-for="item in list" :key="item.index">
                <a :href="item.link">
                    <span class="text">{{ item.value }}</span>
                    <span class="date">{{ item.date }}</span>
                </a>
            </li>
        </ul>
    </div>
</template>

<script>
import tyTitle from './ty-title'
export default {
  components: {
      'ty-title': tyTitle
  },
  props: {},
  data () {
    return {
        title: 'Archives',
        list: [
                {
                    link: 'https://blog.yukarin.me/archives/16.html',
                    value: '[萌化项目] 扁平ACG风落地页',
                    date: '8102/9/10'
                },{
                    link: 'https://blog.yukarin.me/archives/19.html',
                    value: 'TY-LandingPage:一个简单的落地导航页',
                    date: '8102/9/9'
                },{
                    link: 'https://blog.yukarin.me/archives/17.html',
                    value: '[魔改项目] 知乎PC网页版夜间模式',
                    date: '8102/8/23'
                },{
                    link: 'https://blog.yukarin.me/archives/4.html',
                    value: '幻想领域1.4.3修复版',
                    date: '8102/8/7'
                },{
                    link: 'https://github.com/Miya-Yukarin/Ling-lib/tree/master/LandingPage%20v2.0',
                    value: '(已停止维护)LandingPage:一个简单的落地导航页项目',
                    date: '8102/8/6'
                }
        ]
    }
  },
  watch: {},
  computed: {},
  methods: {},
  created () {},
  mounted () {}
}
</script>
<style lang="less" scoped>
div{
    display: flex;
    flex-direction: column;
    padding: 0;
    header{
        margin-top: 2.4rem;
    }
    ul{
        padding: 0 .6rem;
    }
    li{
        padding: .6rem 0;
        .text{
            color: rgba(0,0,0,.87);
            font-size: 1.2rem;
        }
        .date{
            font-size: .8rem;
        }
    }
}
</style>

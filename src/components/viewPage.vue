<template>
  <div id="app">
    <header>
      Comicomic
    </header>
    <main>
      <div class="select"></div>
      <div class="content">
        <div class="one"></div>
        <div class="two">
          <div class="cover"></div>
          <div class="introduction">
            <div class="title">MY HEXSCHOOL</div>
            <div class="intro-content">
              <div class="sub-intro"> 
                <div class="column1">Genres</div>
                <div class="column2">Fusce/vehicula/dolor</div>
              </div>
              <div class="sub-intro">
                <div class="column1">Author</div>
                <div class="column2">Namae Shiranai</div>
              </div>
              <div class="sub-intro">
                <div class="column1">Status</div>
                <div class="column2">Ongoing</div>
              </div>
              <div class="sub-intro">
                <div class="column1">Rate</div>
                <div class="column2"><Rate></Rate></div>
              </div>
              <div class="summary">
                <div class="column1">summary</div>
                <div class="column2">
                  If your banker breaks, you snap; if your apothecary by mistake sends you poison in your pills, you die. 
                  <br><br>
                  Therefore, I say, I saw that this situation of mine was the precise situation of every mortal that has this Siamese connexion with a plurality of other mortals. 
              </div>
            </div>
            
            </div>
          </div>
        </div>
        <div class="two-select">
          <div class="title">My Hexschool</div>
          <select>
            <option value="0">Chapter 1</option>
            <option value="1">Audi</option>
          </select>
          <select>
            <option value="0">Chapter 1</option>
            <option value="1">Audi</option>
          </select>
          <div class="theme">
            <div><i class="fas fa-sun"></i></div>
            <div class="select">
              <div class="dark"></div>
              <div class="white"></div>
            </div>
            <div><i class="fas fa-moon"></i></div>
          </div>
        </div>
        <div class="three"></div>
        <div class="four">
          <div class="all-chapters">
            <div>All Chapters</div>
          </div>
          <div class="chapter">
            <div @click="showComic">Chapter 1: The F2E Challenge Start!</div>
            <div @click="showComic">Chapter 2: Todo List is Going Crazy!</div>
          </div>
        </div>
        <div class="four-comic">

        </div>
        <div class="five"></div>
      </div>  
    </main>
  </div>
</template>

<script>

export default {
  name: 'App',
  data: function(){
    return {}
  },
  mounted() {
  },
  methods: {
    showComic() {

    }
  }
}
</script>

<style lang="sass">
$imgpath: './assets/'
$img1: $imgpath + 'ad-1.png'
$img2: $imgpath + 'comiccover.png'
$img3: $imgpath + 'ad-2.png'
$img5: $imgpath + 'ad-3.png'

$headerH: 70px;
$green: #7ED321;
$red: #D0021B;
$blue: #4A90E2;
@mixin page-padding 
	padding: 0px 30px;
@mixin title
  font-weight: bold
  color: #000000; 
  font-size: 24px;
@mixin total-area($color, $area)
  font-weight: bold
  font-size: 16px;
  color: #000000; 
  padding: 26px 70px
  height: 138px
  grid-area: $area
  background-color: #fff
  div
    &:before
      font-family: FontAwesome
      content: "\f155"
      margin-right: 10px
  .count
    font-size: 36px;
    color: $color


html 
  height: 100%;
  body 
    margin: 0px 0px;
    height: 100%;
    background: #F2F2F2 ;

#app 
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;

  header
    height: 74px
    line-height: 74px
    background-color: #000
    font-family: Roboto;
    font-size: 36px;
    color: #50FF44;
    font-weight: bold
    font-style: italic
  main
    width: 100%
    position: relative
    .content
      width: 620px
      position: absolute
      left: 0
      right: 0
      margin: 10px auto
      > div
        margin: 20px auto
      .one
        height: 120px
        background-image: url($img1)
        background-size: contain
        
      .two
        &::after
          content: ''
          display: block
          clear: both
        .cover
          width: 300px
          height: 450px
          background-image: url($img2)
          background-size: cover
          background-repeat: no-repeat;
          border: 4px solid #000000
          float: left
        .introduction
          float: left
          width: calc(100% - 300px)
          .title
            height: 52px
            background-color: #000
            font-weight: bold
            font-family: Roboto;
            font-size: 36px;
            color: #FFFFFF;
            line-height: 52px;
            margin-bottom: 10px
          .intro-content
            padding: 0px 20px
            text-align: left
            .sub-intro
              &::after
                content: ''
                display: block
                clear: both
              padding: 5px 0px
              .column1
                font-weight: bold
                font-family: Roboto;
                font-size: 16px;
                color: #000000;
                line-height: 24px;
                float: left
                width: 80px
              .column2
                font-family: Roboto;
                font-size: 16px;
                color: #000000;
                line-height: 24px;
                float: left
            .summary
              .column1
                font-weight: bold
                font-family: Roboto;
                font-size: 16px;
                color: #000000;
                line-height: 24px;
                width: 80px
              .column2
                padding: 5px 0px
                font-family: Roboto;
                font-size: 16px;
                color: #000000;
                line-height: 24px;
      .two-select
        &::after
          content: ''
          display: block
          clear: both
        .title
          text-align: left
          width: 145px
          display: inline-block
          font-weight: bold
          font-family: Roboto;
          font-size: 20px;
          color: #000000;
          position: relative
          float: left
          &::after
            position: absolute;
            content: "";
            top: 8px;
            right: 0px;
            width: 0;
            height: 0;
            border: 6px solid transparent;
            border-color: transparent transparent transparent #000 
        select
          float: left
          border: 2px solid #000000
          background-color: #fff
          color: #000
          width: 127px
          height: 35px
          font-weight: bold
          font-family: Roboto;
          font-size: 16px;
          color: #000000;
          display: inline-block
          outline: none
          &:nth-child(3)
            border-left: 0px
        .theme
          float: right
          > div
            float: left
            color: #000
          .select
            margin: 0px 10px
            border: 2px solid #000
            box-sizing: border-box;
            width: 48px
            height: 24px
            padding: -10px
            > div
              width: 50%
              height: 100%
              float: left
              margin: 0
            .dark
              background-color: #000
            .white
              background-color: #fff
          .fa-sun,.fa-moon
            font-size: 24px
      .three
        height: 120px
        background-image: url($img3)
        background-size: contain
 
      .four
        height: 120px
 
        .all-chapters
          &::after
            content: ''
            display: block
            clear: both
          > div
            font-weight: bold
            font-family: Roboto;
            font-size: 24px;
            color: #FFFFFF;
            background-color: #000
            width: 181px
            float: left
          
        .chapter
          background: #FFFFFF
          border: 4px solid #000000
          text-align: left
          font-weight: bold
          font-family: Roboto;
          font-size: 16px;
          > div
            margin: 10px
            position: relative
            &:last-child:after
              content: 'NEW'
              position: absolute
              text-align: center
              width: 55px
              background: #50FF44;
              font-weight: bold
              font-family: Roboto;
              font-size: 14px
              color: #000000
              line-height: 20px
              height: 18px
              top: 0
              bottom: 0
              margin: auto 10px   
      .five
        height: 120px
        background-image: url($img5)
        background-size: contain
@media screen and (max-height: 800px) 
  #app
    main
      .content
        .one,.three,.five
          height: 0px

  
</style>

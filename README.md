# 包含内容

html、css、js、vue、react 常用命令
element PLUS 常用组件

# 代码片段对应

## html

```html
<!-- form ：form表单基本结构-->
<form action="" method="">
  <input type="" name="" value="" />
</form>

<!--table：table表格基本结构-->
<table>
  <tr>
    <td></td>
  </tr>
</table>
```

## css

```css
/* dis-flex：flex基本结构 */
display: flex;
justify-content: center;
align-items: center;

/* dis-grid：grid基本结构 */
display: grid;
grid-template-columns: 1fr;
grid-template-rows: 1fr;
justify-items: center;
align-items: center;

/* wh100：测试用小方块 */
width: 100px;
height: 100px;
backcground-color: red;

/* *：清除内外边距 */
* {
  margin: 0;
  padding: 0;
}

/* ellipsis-one：将文本设置为一行，超出部分变省略号*/
white-space: nowrap;
text-overflow: ellipsis;
overflow: hidden;

/* ellipsis-two：将文本设置为多行，超出部分变省略号，本片段指的是两行 */
display: -webkit-box;
-webkit-line-clamp: 2;
-webkit-box-orient: vertical;
overflow: hidden;
text-overflow: ellipsis;

/* @key：设置动画基本模板 */
@keyframes animationName {
  0% {
    /* 初始状态 */
  }
  100% {
    /* 最终状态 */
  }
}

/* @med：媒体查询基本模板 */
      /*
       max-width:600px:表示屏幕宽度小于600px的样式，括号中使用该样式
       min-width:600px:表示屏幕宽度大于600px的样式，括号中使用该样式
      */
      @media screen and (xxx) {
       $1
      }
```

## react

## javascript

```javascript
// fun：普通方法模板
function fun() {

}

// =>：箭头函数模板
fun()=>{

}

// l：空打印模板
console.log()

//l#：打印一行“#”分隔符
console.log('#############################################################)

//l*：打印一行“*”分隔符
console.log('********************************************)

//l-：打印一行“-”分隔符
console.log('--------------------------------------------)

//l=：打印一行“=”分隔符
console.log('============================================)

//l+：打印一行“+”分隔符
console.log('++++++++++++++++++++++++++++++++++++++++++++)

//l?：打印一行“？”分隔符
console.log('????????????????????????????????????????????)

//l!：打印一行“！”分隔符
console.log('!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!)

//l@：打印一行“@”分隔符
console.log('@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@)

// docu：获取单个元素节点
const xxx=document.querySelector()

// coduall：获取某一类型所有元素节点
const xxx=document.querySelectorAll()

//deepCopy：通过json的序列化和反序列化进行深拷贝
const ans = JOSN.parse(JSON.stringify(xxx))

//ymd：将当前日期转换为“年-月-日”格式的方法
function dateToFormat(param){
  const date = new Date(param);
  let year = date.getFullYear();
  let month = date.getMonth() + 1;
  let day = date.getDate();
  return `${year}年${month}月${day}日`;
}

//ymdhms：将当前日期转换为“年-月-日 时:分:秒”格式的方法
function dateToFormat2(param){
  const date = new Date(param);
  let year = date.getFullYear();
  let month = date.getMonth() + 1;
  let day = date.getDate();
  let hour = date.getHours();
  let minute = date.getMinutes();
  let second = date.getSeconds();
  return `${year}年${month}月${day}日 ${hour}时${minute}分${second}秒`;
}

// /phone/：判断一个字符串是否为手机号的方法，内涵手机号的正则表达式
function isPhone(param){
  const reg = /^1[3-9]\\d{9}$/;
  return reg.test(param);
}

// /email/：判断一个字符串是否为邮箱的方法，内涵邮箱的正则表达式
function isEmail(param){
  const reg = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\\.[a-zA-Z]{2,}$/;
  return reg.test(param);
}

```

## vue

```vue
// tss：vue基本框架，不使用set语法糖
<template>
  <div></div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: '$2'
  setup() {
      return {

      };
  }
});
</script>

<style scoped></style>

// tss-setup：vue基本框架，使用set语法糖
<template></template>

<script setup lang="ts"></script>

<style scoped></style>

//debounce：vue中防抖函数组件，可直接引入使用
type CallbackFunc<T extends unknown[]> = (...args: T) => void

export function debounce<T extends unknown[]>(
  func: CallbackFunc<T>,
  wait: number,
): (...args: T) => void {
  let timeoutId: ReturnType<typeof setTimeout> | undefined
  return (...args: T) => {
    const later = () => {
      clearTimeout(timeoutId)
      func(...args)
    }
    clearTimeout(timeoutId)
    timeoutId = setTimeout(later, wait)
  }
}

// throttle：vue中节流函数组件，可直接引入使用
type CallbackFunc<T extends unknown[]> = (...args: T) => void;
      
export function throttle<T extends unknown[]>(
  func: CallbackFunc<T>,
  limit: number,
): (...args: T) => void {
  let inThrottle: boolean;
  let lastTime: number;
  return (...args: T) => {
    const now = Date.now();
    if (!lastTime) {
      lastTime = now;
    }
    if (!inThrottle && now - lastTime >= limit) {
      func(...args);
      lastTime = now;
      inThrottle = true;
      setTimeout(() => {
        inThrottle = false;
      }, limit);
    }
  };
}
```

## react

## react

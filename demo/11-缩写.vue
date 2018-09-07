// 缩写

// v-bind缩写 :
// 完整语法
<a v-bind:href="url"></a>

// 缩写
<a :href="url"></a>

// v-on缩写 @

// 完整语法
<a v-on:click="doSomething"></a>  //有个疑问到底值v-on是用onclick的方法绑定的还是监听

// 缩写
<a @click="doSomething"></a>
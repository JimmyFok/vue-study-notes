        // vue.js的模板，也可以直接写JSX语法
        // 模板语法
        
        // 1、文本
        <span>Message: {{ msg }}</span>
        
        // v-once指令，执行一次性插值
        <span v-once>这个将不会改变: {{ msg }}</span>

        // 2、原始HTML
        // {{}}会将数据解释为普通文本，而非HTML代码。
        <p>Ussing mustaches: {{rawHtml}}</p>
        <p>Using v-html directive:  <span v-html="rawHtml"></span></p>

        // 站点上动态渲染的任意HTML可能会非常好危险，容易导致XSS工具，所以只有对可信内容，例如自己开发的部分才可以插。
        // 3、特性（可以理解为标签上的Attribute）
        <div v-bind:id="dynameicId"></div>

        <button v-bind:disabled="isButtonDisabled">Button</button>
        // 注意：这里是不会渲染出来的。isButtonDisabled是null、undefined或false，渲染的时候不会出现在对应的元素上

        // 4、JS表达式。{{}}支持js表达式，但是限制的是单个表达式，不然就不会生效。
        {{number+1}}

        // 模板表达式放在沙盒中？！只能访问全局变量的一个白名单，如Math和Date

        
```js
// 格式化数字
const number = 1234567.89;
const formattedNumber = number.toLocaleString('zh-CN'); // 格式化为中国的数字格式
console.log(formattedNumber); // 输出 "1,234,567.89"

// 格式化日期
const date = new Date();
const formattedDate = date.toLocaleDateString('zh-CN', { year: 'numeric', month: 'long', day: 'numeric' });
console.log(formattedDate); // 输出 "2022年九月28日"

// 格式化时间
const time = new Date();
const formattedTime = time.toLocaleTimeString('zh-CN');
console.log(formattedTime); // 输出 "下午3:45:12"

// 自定义格式
const customNumber = 12345.67;
const customFormattedNumber = customNumber.toLocaleString('zh-CN', { style: 'currency', currency: 'CNY' });
console.log(customFormattedNumber); // 输出 "¥12,345.67"

```

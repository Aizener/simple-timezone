### 一个超级简单的各地时区时间选择库
[一看就明白的超简单示例](https://aizener.github.io/simple-timezone/)

### 安装&使用
```shell
npm install --save simple-timezone
```
```js
import Timezone from 'simple-timezone'

const tz = new Timezone()
console.log(tz.getDate('HongKong', 'yyyy年mm月dd日 hh时MM分ss秒'))  // getDate第二个参数可不传，默认yyyy-mm-dd hh-MM-ss
```

### API
- getListGroupByArea 获取不同洲的时区信息；
- getTime：name  根据name（时区英文名字）获取当地时间戳；
- getDate: name | format = 'yyyy-mm-dd hh:MM:ss' 根据name（时区英文名字）获取当地时间，时间是format格式化的时间；
- add：obj 因为获取的时区都是事先写好的一个json对象，并不会涵盖所有，所以提供这个方法用来自定义
```js
tz.add({ 'demo': { cn: '测试地区', offset: 2, area: 'ASIA', country: '中国' } })
```

> 因为业务或许需要，先封装一哈，暂时就这，后续有时间补充...

# Vue
## 一、vue中select的使用以及select设置默认选中

**解决过程**  
html代码如下，通过v-model可以获取到选中的值，如果option中存在value属性，优先获取value值即coupon.id，如果不存在，则获取option的文本内容，也就是下面代码中coupon.name.  

**html:**
```java
<select name="public-choice" v-model="couponSelected" @change="getCouponSelected">                                        
    <option :value="coupon.id" v-for="coupon in couponList" >{{coupon.name}}</option>                                    
</select>
```

**js:**  
```js
var vm = new Vue({
                el: '#app',
                data:{
                    couponList:[
                        {
                            id: 'A',
                            name: '优惠券1'
                        },
                        {
                            id: '1',
                            name: '优惠券2'
                        },
                        {
                            id: '2',
                            name: '优惠券3'
                        }
                    ],
                    couponSelected: '',
                },
                created(){
　　　　　　　　　　　　//如果没有这句代码，select中初始化会是空白的，默认选中就无法实现
                    this.couponSelected = this.couponList[0].id;
                },
                methods:{

　　　　　　　　　　　　getCouponSelected(){
                        //获取选中的优惠券
                        console.log(this.couponSelected)
                    }


                }
            })
```
            
**隐藏属性就是**  
当我们把v-model中的couponSelected,也就是data里的couponSelected的值赋值为循环的option中的value后，那这个option就会被默认选中。  
**[转载自] https://www.cnblogs.com/till-the-end/p/8473738.html**


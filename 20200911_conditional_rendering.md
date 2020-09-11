## --------- Conditional rendering ------------
#### 1) Sự khá nhau giữa v-if và v-show
- v-if: 

Ví dụ
```php
<template>
    <div class="conditional-rendering">
        <div class="block-1" v-if="isActive == false">
            This is block 1
        </div>
        <div class="block-2" v-if="isActive == true">
            This is block 2
        </div>
        <div>
            <button @click="isActive = !isActive">Button</button>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                isActive: true
            }
        }
    }
</script>

<style lang="scss" scoped>
</style>
```
-> Khi dùng v-if, chỉ khi điều kiện đúng thì element đó mới được render ra ngoài
- v-show:
```php
<template>
    <div class="conditional-rendering">
        <div class="block-1" v-show="isActive == false">
            This is block 1
        </div>
        <div class="block-2" v-show="isActive == true">
            This is block 2
        </div>
        <div>
            <button @click="isActive = !isActive">Button</button>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                isActive: true
            }
        }
    }
</script>

<style lang="scss" scoped>
</style>
```
-> Khi dùng v-show, tất cả element đều được render ra từ đầu nhưng khác nhau về thuộc tính (css, display)
- Nếu nộ dung trong block ít và user tác động đến block nhiều thì nên dùng v-show để tăng tốc độ xử lí
- Nếu nội dung của block nhiều cùng nhiều xử lí hoặc block ít thay đổi thì ko nên dùng v-show vì sẽ nặng làm giảm hiệu năng

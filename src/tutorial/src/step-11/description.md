# Компоненти {#components}

Досі ми працювали лише з одним компонентом. Справжні додатки Vue зазвичай створюються за допомогою вкладених компонентів.

Батьківський компонент може рендерити інший компонент у своєму шаблоні як дочірній. Щоб використовувати дочірній компонент, нам потрібно спочатку його імпортувати:

<div class="composition-api">
<div class="sfc">

```js
import ChildComp from './ChildComp.vue'
```

</div>
</div>

<div class="options-api">
<div class="sfc">

```js
import ChildComp from './ChildComp.vue'

export default {
  components: {
    ChildComp
  }
}
```

Нам також потрібно зареєструвати компонент за допомогою опції `components`. Тут ми використовуємо скорочення властивостей об'єкта, щоб зареєструвати компонент `ChildComp` під ключем `ChildComp`.

</div>
</div>

<div class="sfc">

Потім ми можемо використовувати компонент у шаблоні як:

```vue-html
<ChildComp />
```

</div>

<div class="html">

```js
import ChildComp from './ChildComp.js'

createApp({
  components: {
    ChildComp
  }
})
```

Нам також потрібно зареєструвати компонент за допомогою опції `components`. Тут ми використовуємо скорочення властивостей об'єкта, щоб зареєструвати компонент `ChildComp` під ключем `ChildComp`.

Оскільки ми пишемо шаблон в DOM, він буде підпорядкований правилам парсингу браузера, які не враховують регістр для імен тегів. Тому для посилання на дочірній компонент нам потрібно використовувати ім'я в стилі `kebab-cased`:

```vue-html
<child-comp></child-comp>
```

</div>


Тепер спробуйте самі - імпортуйте дочірній компонент і виведіть його в шаблоні.

# Frontend
Тестовое задание для Frontend-разработчиков

## Описание
Представьте, что вам необходимо реализовать каталог товаров для крупного 
интернет магазина. На данной странице выводится название категории,
блоки с фильтрацией, сортировкой, баннеры, описание, но основным блоком на 
данной странице является список товаров.

## Задача
Ваша задача заключается в том, что бы отображать список товаров на этой странице.
Нет необходимости что-либо подгружать с серверов, эти данные можно просто 
замокать и имитировать подгрузку данных отображением лоадера.

Cписок товаров необходимо сгенерировать самостоятельно.
Тип данных товара можно взять [отсюда](#типы-данных). Менять эти типы
данных **запрещено**.

В качестве выполненной работы необходимо предоставить ссылку на репозиторий с исходниками.
Проект должен запускаться локально. 

## Требования к технологиям
- React **без классовых компонентов**
- React Hooks
- Минимальная ширина экрана - 320px. Максимальная 1280px
- *Желательно использовать CSS Modules, SASS.
- *Желательно использовать TypeScript.

## Требования к визуалу
- При первичной загрузке необходимо отображать 20 первых товаров
- Приложение не должно тормозить даже когда на экране более 1000 товаров
- Осуществлять lazy load подгрузку когда скролл приближается к нижней границе
экрана. Подгрузка осуществляется по 20 товаров
- Все кнопки, названия товаров должны быть на одном горизонтальном уровне.
- Кликом на изображение, название и кнопку 'Подробнее' в карточке товара, необходимо 
выполнять переход по ссылке указанной в поле link
- Название товара должно обрезаться в случае если будет занимать больше двух строк, 
но при наведение на название плавно увеличиваться вверх для показа полного текста названия,
уменьшая  при этом изображение, карточка при  наведении на название показана на макете,
компонент - Product hover
- Значок со скидкой и цена со скидкой показываются только при условии что она ниже обычной цены, 
процент скидки высчитывается при выводе.
- Выполненная работа должна соответствовать [макету](#макет) указанному 
ниже. 


## Типы данных
```typescript
// Список вариаций 
enum ActionsType {
  HIT, 
  NEW
}

// Товар
interface Product {
  // Изображение
  image: string,
  // Название
  name: string;
  // Ссылка для перхода
  link: string;
  // Актуальная цена 
  price: number; 
  // Цена со скидкой
  priceDiskount: number;
  // Акции
  action?: ActionsType[]
}
```

## Макет
https://www.figma.com/file/llBdQ9L8oIn1oZh2qVmU0F/Catalog

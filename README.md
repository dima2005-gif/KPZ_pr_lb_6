# Величко Дмитро ІПЗ 3.02
# Практично-лабораторне заняття №6
## Розробка UI для реалізації CRUD-операцій

Склонував проект
![Image](https://github.com/user-attachments/assets/2a71f750-7d6e-4bd9-9a79-76b9bc9b23f4)


Так встановимо деякі залежності у наш проект. 

По-перше напишемо команду ```npm install``` для встановлення деяких залежностей

![Image](https://github.com/user-attachments/assets/79bc5f82-1c31-4fdd-9c7e-33a1e6fe7f50)


як бачимо тут помилки, вони полягають у тому, що проблема з версіями залежностей.

Підемо жорстким шляхом проігноруючи версії акетів. Виконаємо команду: ```npm install --legacy-peer-deps```

![Image](https://github.com/user-attachments/assets/58aecfa0-1ef9-4f7d-8c8a-5428ae390c3d)


Тепер запустимо наш проект виконавши команду ```npm run dev```

![npm_run_dev](https://github.com/user-attachments/assets/0b16a1b9-e8ad-47de-88c0-e3a7e74d0ca9)


Тепер ми можеио перейти за адресою ```http://localhost:5173/```

![hello_world](https://github.com/user-attachments/assets/bf5c2f34-acdd-47b0-8685-ebcb1ed17620)


## 1. Сторінка колекції екземплярів сутності (/posts). 2. Сторінка окремого екземпляра сутності (/posts/:id або /posts/new)

Так спочатку створемо наші сторінки. Перед цим зайдемо у каталог /components/ui створемо
2 файла EntityCard і Modal і створемо у цих каталогах 2 файла у форматі .tsx і.ts

![component_ui](https://github.com/user-attachments/assets/f42db2a7-5d54-48e6-9443-ff1f46dcec39)

Тепер зміст файлів

# ```EntityCard.tsx```
![entitycard_1](https://github.com/user-attachments/assets/a7ef67cc-062c-43c2-a93a-c77b77f950fb)
![entitycard_2](https://github.com/user-attachments/assets/3c7ec552-3fe2-4375-a34d-2125e9e66ccc)

# ```index.ts```
![entitycard_index](https://github.com/user-attachments/assets/f0abbd70-0409-42a5-9377-9f9e7531f696)

# ```Modal.tsx```
![modal](https://github.com/user-attachments/assets/c42f408a-e543-4f1d-ae9d-141097a692aa)

# ```index.ts```
![modal_index](https://github.com/user-attachments/assets/f64d10a2-e1f3-4807-936a-8683beee75a9)


Так тепер перейдемо у каталог pages створимо три файла: ```Entities.tsx```, ```EntityCreate.tsx```, ```EntityDetails.tsx```

![pages](https://github.com/user-attachments/assets/214d9eb9-f032-4840-b7b9-7d21e6830475)


# ```Entities.tsx```
![entities_1](https://github.com/user-attachments/assets/b3f7ae16-3f82-4394-b176-8987f5258658)

![entities_2](https://github.com/user-attachments/assets/efc7a287-2d00-456f-a0c5-0f656e1d5b61)

![entities_3](https://github.com/user-attachments/assets/a36c2da7-6d94-4e16-b933-1ff360e74869)


# ```EntityCreate.tsx```
![entities_create_1](https://github.com/user-attachments/assets/b8f002f3-5e37-41ca-9224-892db8f76ce8)
![entities_create_2](https://github.com/user-attachments/assets/c8f9537b-671b-4a2e-8891-f26268eddc2a)
![entities_create_3](https://github.com/user-attachments/assets/94182f25-492c-49e3-8af0-e04003afa428)


# ```EntityDetails.tsx```
![entity_details](https://github.com/user-attachments/assets/d09a8aca-68d0-4529-ad01-ad09d47f82f7)


Тепер пейдемо у папку routes створимо файл entities з 3 файлами: ```$id.ts```, ```index.ts```, ```new.ts```
![routes](https://github.com/user-attachments/assets/17e0c2e5-7070-4e1f-9de3-8c1eb68debf8)

# ```$id.ts```
![id](https://github.com/user-attachments/assets/045715b8-8b47-4f87-b60f-03a3e8603283)


# ```index.ts```
![index](https://github.com/user-attachments/assets/50f6585f-ff82-48cc-92f7-9a0f350ae5f9)

# ```new.ts```
![new](https://github.com/user-attachments/assets/c022fc1d-8e4c-4182-89fe-3b4b1c9f3ea9)


У файл ```routeTree.gen.ts``` додамо шляхи до роутера:
![routeTree_1](https://github.com/user-attachments/assets/998a62d5-29d9-4315-9751-9dc4e9835c43)
![routeTree_2](https://github.com/user-attachments/assets/e0757b76-5857-4111-855f-b6bb6fa09938)
![routeTree_3](https://github.com/user-attachments/assets/6821f810-09a8-47a8-bd02-eb787f061d0b)
![routeTree_4](https://github.com/user-attachments/assets/23517949-7dec-48f5-a16d-ddccc34ed84a)
![routeTree_5](https://github.com/user-attachments/assets/2c121873-e98a-43c9-a65b-9103dd416e31)


У  каталозі ```src``` створемо каталог ```entities``` файл ```index.ts``` де ми напишемо мок-функції

![mock_function_1](https://github.com/user-attachments/assets/dacc95c7-7546-4f10-aa99-f48d85cb8d1f)
![mock_function_2](https://github.com/user-attachments/assets/cdc76978-376e-407a-8723-c8e47980c667)
![mock_function_3](https://github.com/user-attachments/assets/3b1b12b4-95fc-4004-98b2-44b2211dadf6)

У каталозі ```src``` створемо каталог ```types``` і створемо файл ```Entity.ts```

![types](https://github.com/user-attachments/assets/da9bbb98-4d7c-4e36-b119-58d33ff0e2d7)

Тепер запустимо наш проект, для цього в терміналі напишемо команду: ```pnpm run dev```

![result](https://github.com/user-attachments/assets/eb77b2b2-4b51-4174-9096-2b88b70b8580)

## Створення нової сутності

![create](https://github.com/user-attachments/assets/8eee2376-6a9a-4302-9621-d09020f51e7a)

## Поява нової сутності 
![new_attribute](https://github.com/user-attachments/assets/e4539046-eec3-4386-b345-629c2d63e1f5)


## Зміна сутності

![update_attribute](https://github.com/user-attachments/assets/9771be57-abf8-405a-8271-483e266018ff)

## Видалення сутності

![delete](https://github.com/user-attachments/assets/b09a5214-410e-4610-9b06-b0a788840037)

## Оновлений список після видалення
![update_list](https://github.com/user-attachments/assets/b3c00a48-70e9-491b-bcb5-c07ff5241896)


## Загальний висновок

У ході практично-лабораторного заняття №6 було повністю реалізовано UI для виконання CRUD-операцій (створення, читання, оновлення та видалення) над сутностями. Було пройдено повний цикл розробки:
- Склоновано та налаштовано проект із відповідними залежностями;
- Успішно вирішено проблеми сумісності за допомогою ```--legacy-peer-deps```;
- Реалізовано компонентну структуру інтерфейсу (компоненти ```EntityCard```, ```Modal```);
- Створено сторінки для перегляду списку сутностей, створення нових, перегляду деталей та редагування;
- Налаштовано маршрутизацію для навігації між сторінками;
- Створено типи та мок-дані для роботи з даними;
- Перевірено функціональність додавання, редагування та видалення сутностей з оновленням списку у режимі реального часу.

Проєкт працює стабільно, відповідає принципам SPA (Single Page Application), а інтерфейс дозволяє зручно керувати сутностями. Ця робота є хорошою практикою у створенні сучасних UI-додатків з React та TypeScript.

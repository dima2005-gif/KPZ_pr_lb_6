Практично-лабораторне заняття №6
Розробка UI для реалізації CRUD-операцій
Склонував проект
git_clone.png
Так встановимо деякі залежності у наш проект. 
По-перше напишемо команду npm install для встановлення деяких залежностей
npm_install.png
як бачимо тут помилки, вони полягають у тому, що проблема з версіями залежностей.
Підемо жорстким шляхом проігноруючи версії акетів. Виконаємо команду: npm install --legacy-peer-deps
npm_install_--legacy-peer-deps.png
Тепер запустимо наш проект виконавши команду npm run dev
npm_run_dev
Тепер ми можеио перейти за адресою http://localhost:5173/
hello_world.png
1. Сторінка колекції екземплярів сутності (/posts)
Реалізувати рендеринг списку всіх доступних екземплярів сутності.
Для кожного елемента відображати основну інформацію (ключові поля).
Передбачити можливість переходу на сторінку конкретного екземпляра (/posts/:id).
Додати кнопку "Створити новий екземпляр", яка веде на маршрут /posts/new.
Реалізувати можливість видалення елемента з колекції (з підтвердженням дії).

Так спочатку створемо наші сторінки. Перед цим зайдемо у каталог /components/ui створемо
2 файла EntityCard і Modal і створемо у цих каталогах 2 файла у форматі .tsx і.ts
components_ui.png
Так тепер перейдемо у каталог pages створимо три файла: Entities.tsx, EntityCreate.tsx, EntityDetails.tsx
pages.jpg
Entities.tsx
entities_1.png
entities_2.png
entities_3.png

EntityCreate.tsx
entities_create_1.png
entities_create_2.png
entities_create_3.png

EntityDetails.tsx
entity_details.png

Тепер пейдемо у папку routes створимо файл entities з 3 файлами: $id.ts, index.ts, new.ts
routes.png

$id.ts
id.png

index.ts
index.png

new.ts
new.png

фото з routes/entities
У файл routeTree.gen.ts додамо шляхи до роутера:
routeTree_1.png
routeTree_2.png
routeTree_3.png
routeTree_4.png
routeTree_5.png

фото з змістом цього файлу
У  каталозі src створемо каталог entities файл index.ts де ми напишемо мок-функції
mock_function_1.png
mock_function_2.png
mock_function_3.png

фото с файлом entities 
У каталозі src створемо каталог types і створемо файл Entity.ts
types.png
фото цього файлу.
Тепер запустимо наш проект, для цього в терміналі напишемо команду: pnpm run dev
result.png
Створення нової сутності
create.png
поява нової сутності 
new_attribute.png
Зміна сутності
update_attribute.png
Видалення сутності
delete.png
Оновлений список після видалення
update_list.png


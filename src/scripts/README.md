# 📁 Папка `scripts`

В данной папке размещаются скриптовые файлы проекта (`*.js`), отвечающие за динамическое поведение интерфейса и взаимодействие с пользователем.

## 💡 Динамическая составляющая макета:

---

### 1. Фиксация и прозрачность хедера при прокрутке страницы

**Описание:**  
При прокрутке страницы у навигационного блока появляется подложка (фон), чтобы избежать наложения контента на хедер и улучшить читаемость.

**Элементы:**  
- Родительский контейнер хедера (`.header`)
- Прокрутка окна

**Файл:** scroll/navbarFixed.js

---

### 2. Автоматический вывод карточек (тегов, отзывов, тарифов и т.д.)

**Описание:**  
Некоторые карточки (например, тарифные планы, отзывы, теги) могут загружаться динамически при старте страницы (в будущем — с сервера).

**Элементы:**  
- Контейнер карточек
- Каждая карточка — ссылка с иконкой, заголовком и описанием

**Файл:** slider/tariffsSlider.js`, `reviews/autoScroll.js

---

### 3. Добавление в избранное (лайк, сердечко)

**Описание:**  
При клике на иконку сердечка — иконка подсвечивается (например, красным), а счётчик лайков увеличивается. Повторный клик снимает отметку.

**Элементы:**  
- Иконка (сердце)
- Счётчик пользователей

**Файл:** components/favoriteToggle.js *(если будет)*

---

### 4. Фильтрация тегов при вводе в поисковую строку

**Описание:**  
При вводе в строку поиска — показываются только совпадающие теги, остальные скрываются.

**Элементы:**  
- Поле ввода (поиск)
- Список тегов под ним

**Файл:** components/tagFilter.js *(если будет)*

---

### 5. Отображение форм авторизации / регистрации

**Описание:**  
При клике на кнопку "Войти" открывается модальное окно с формами, между которыми можно переключаться (вход / регистрация).

**Элементы:**  
- Кнопка "Войти"
- Формы внутри модального окна

**Файл:** forms/modalToggle.js`, `forms/formSwitch.js`, `forms/tabSwitch.js

---

### 6. Валидация форм и отправка

**Описание:**  
Поля формы валидируются на клиенте. При успешной отправке — данные очищаются, отображается сообщение об успехе.

**Элементы:**  
- Поля форм
- Кнопка отправки
- Модальное окно подтверждения

**Файл:** forms/validationRegister.js`, `forms/enrollModal.js

---

> 💡 Каждая функциональность вынесена в отдельный модуль внутри папки `scripts` или подкаталогов (`forms/`, `scroll/`, `slider/`, и т.д.) для удобства разработки и поддержки.
# EndeavourOS + Cinnamon
> Есть возможность выбрать zen или lts ядра.
## Pamac (Установка и удаление программ)
```
yay -S pamac-aur
```
*`yay` уже включен в EndeavourOS*

После установки в настройках необходимо включить поддержку Aur.
____
## Программы и утилиты
> Не забудьте обновить систему!
- ### Нижний док
    - plank
    - plank-theme-nordic-night-git (тема для дока)
- ### Тема
    - nordic-theme
    - nordic-wallpapers (обои)
    - tela-icon-theme (иконки)
- ### Консольные утилиты
    - kitty (терминал)
    - neovim
    - tmux
    - starship
- ### Софт
    - firefox-developer-edition
    - discord
    - steam
    - flameshot
## Параметры системы
Ниже показаны минимальные настройки, которые следует сделать в параметрах системы.

- ### Темы
    - Значки - `Tela-nord-dark`
    - Приложения - `Nordic`
    - Указатель мыши - `Qogir-dark`
    - Рабочий стол - `Nordic`

- ### Фоновые рисунки
    Добавить папку `/usr/share/backgrounds/nordic-wallpapers` и выбрать подходящие обои.

- ### Автозагрузка
    Добавить команду приложения:

    - Имя - `Plank`
    - Команда - `plank`
    - Описание - необязательно заполнять
    - Задержка автозапуска - `0`

- ### Апплеты
    Загрузить апплеты `Cinnamenu` и `Color Picker`.

    *Для работы `Color Picker` необходимо установить `python-xlib`.*

- ### Окна (прикрепление)
    Включить пункт **`Увеличить на весь экран, вместо прикрепления, в момент перемещения окна к верхней границе`**.

- ### Клавиатура
    Во вкладке **`Комбинации клавиш`** нажать на **`Добавить пользовательскую комбинацю`**:
    - Название - `Flameshot`
    - Команда - `flameshot gui`
    - Клавиша - *`По желанию`*

- ### Предпочтительные приложения
    - Файловый менеджер - `Nemo`
    - Интернет - `Firefox developer edition` *(Или любой другой браузер)*
    - Терминал - `Kitty`
    - Текст - `Текстовый редактор`

## Последующая настройка системы
После перезагрузки появится док. Для его настройки нужно зажать `Ctrl` и кликнуть правой кнопкой мыши по доку и в выпадающем меню нажать `Параметры`.
В открывшемся окне нужно выбрать тему `nordic-night`, включить увеличение иконок и установить ползунок на значении `115` и во вкладке **`Поведение`** скрытие панели переключить на `Автоматическое скрытие`.

Остаётся закрепить необходимы программы в доке.

### Панель
Настойте панель как вам удобно и расположите все необходимые апплеты. Апплет меню стоит заменить на `Cinnamenu`.

### Терминал
Откройте терминал `kitty` и напишите команду для выбора тем
```
kitty +kitten themes
```
В открывшемся меню выберите тему `Nord`.

Откройте в любом редакторе кода конфик kitty и впишите необходимые параметры
```
~/.config/kitty/kitty.conf
--------------------------
# Прозрачность
background_opacity 0.85
dynamic_background_opacity yes

# Размер шрифта
font_size 13.0
```

Отредактируйте файл `~/.bashrc` и добавьте в него команду для активации starship
```
eval "$(starship init bash)"
```

## NVM (Управление версиями nodejs)
[Github NVM](https://github.com/nvm-sh/nvm#installing-and-updating)
### Установка
```
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
```

### Установка и выбор версии nodejs

Для установки используйте команду
```
nvm install <версия>
```

Для выбора другой установленной версии используйте команду
```
nvm use <версия>
```"# Linux-fast-setup" 
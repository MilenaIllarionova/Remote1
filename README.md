# **Работа с удаленными репозиториями**
1. Создать аккаунт на GitHub.

   Если у вас еще нет аккаунта на GitHub, то нужно его создать. Для этого нужно:
 * перейти на сайт [GitHub](https://github.com) и нажать кнопку "Зарегистрироваться",
   ![image](https://github.com/MilenaIllarionova/Remote1/assets/145788111/8e962514-3572-45d5-a685-eba2df08d4b9)

 * ввести адрес электронной почты,
   ![image](https://github.com/MilenaIllarionova/Remote1/assets/145788111/bd35705a-d07b-4f88-8db9-d699d5276cfc)

 * придумать пароль и ввести имя пользователя.
![image](https://github.com/MilenaIllarionova/Remote1/assets/145788111/fa439ef2-6ca5-4960-ba3b-a853dc06af62)

 * проверить свою учетную запись решив головоломку,
 * после проверки учетной записи нажмите кнопку "Создать учетную запись ",
 * затем GitHub отправляет код запуска по адресу электронной почты. Введите код запуска в диалоговом окне "Ввод кода ", а затем нажмите клавишу ВВОД.
![image](https://github.com/MilenaIllarionova/Remote1/assets/145788111/d66777ba-d804-49de-a51d-a7497c52aef8)

Ура! Вы создали учетную запись.

2. Создать локальный репозиторий.

Для создания локального репозитория необходимо создать и открыть пустую папку. При открытии терминала мы увидим, что это еще не локальный репозитоий. Это мы можем проверить командой `git status`. 

В нашей папке нужно создать еще папку и назвать его. Затем нужно снова открыть терминал. Это можно сделать следующим образом:`навести курсор на папку > нажать правой кнопкой мыши > нажать "Открыть во встроенном терминале"`. 

Затем в этой папке нужно создать файл и можно начать работать с ним.

3. Создать удаленный репозитоий.

Вы создали локальный репозиторий, теперь, вам нужно добавить его на Github, тем самым вы фактически создадите удаленный репозиторий.

Перейдите на [GitHub](https://github.com) и войдите в свой аккаунт. Нажмите кнопку "New repository". На открывшейся странице введите имя репозитория и нажмите кнопку "Create repository".

GitHub нам предложит ввести 3 команды в локальном репозитории:
```Bash
git remote add origin https://github.com/username/myproject.git
```
Данная команда добавит удаленный репозиторий с именем origin, который указывает на ваш Github-репозиторий. Пока мы только добавили запись об удаленном репозитории.

```Bash
git branch -M main
```
Данная команда переименовывает вашу текущую ветку master в main.

Теперь можно выполнить команду git push, чтобы отправить все ваши изменения на удаленный репозиторий:
```Bash
git push -u origin master
```

4. Связать удаленный репозиторий с локальным.

Удалённые репозитории представляют собой версии вашего проекта, сохранённые в интернете или ещё где-то в сети. У вас может быть несколько удалённых репозиториев, каждый из которых может быть доступен для чтения или для чтения-записи.

Для того, чтобы просмотреть список настроенных удалённых репозиториев, вы можете запустить команду `git remote`. Она выведет названия доступных удалённых репозиториев.

Чтобы просмотреть адреса для чтения и записи, привязанные к репозиторию, нужно добавить -v
```Bash
git remote -v
```
Добавить удаленный репозиторий к проекту можно с помощью:
```Bash
git remote add <имя репозитория> <url-адрес репозитория в сети>
```
Для получения и слияния изменений из удаленного репозитория используется команда `git pull`.

Отправить изменения локального репозитория в удаленный `git push`.

```C#
while(count < 0)
{
count++;
}
```
Для работы с чужими удаленными репозиториями для начала нужно их добавить к себе с помощью кнопки `Fork`. 

Затем, клонируем репозиторий к себе на компьютер из своего профиля:
```Bash
git clone https://github.com/name/repository_name.git
```
Только что склонированный репозиторий имеет только одну привязку к удалённому репозиторию. Чтобы иметь привязку и к оригинальному репозитоирию, нужно добавить ещё одну привязку:
```Bash
git push --set-upstream origin branch_name
git push --set-upstream origin branch_name
```

Заходим на github на страницу оригинального репозитория. Создам Pull Request на основе созданной нами ветви. Обычно github уже видит созданную ветвь и сам предлагает создать PR к ней.

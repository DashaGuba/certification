# certification
1. Создание issue с названием "Issue 1", описанием "Something went wrong", label "bug" и assignee текущий логин на GitHub:
   - В Postman откройте новый запрос и выберете метод "POST".
   - Введите URL: http://api.github.com/repos/{owner}/{repo}/issues, где {owner}-владелец репозитория, {repo}- название репозитория.
   - В разделе "Headers" добавьте заголовок "Autorization" с значением "Bearer {token}.
   - В разделе body выберите формат RAW и тип JSON.
   - В поле для ввода введите следующий JSON-код:
   - {
   - "title":"Issue 1",
   - "body":"Something went wrong",
   - "labels":["bug"],
   - "assignees":["{логин на GitHub"}]
   - }
   - нажмите кнопку "Send" для отправки запроса. В ответ вы получите информацию о созданной issue, включая ее number и Id, со статусом 201.
2. Получение списка issues:
   - В Postman откройте новый запрос и выберете метод "GET".
   - Введите URL:  http://api.github.com/repos/{owner}/{repo}/issues, где {owner}-владелец репозитория, {repo}- название репозитория.
   - В разделе "Headers" добавьте заголовок "Autorization" с значением "Bearer {token}.
   - Нажмите кнопку "Send" для отправки запроса. В ответ вы получите список issues в указанном репозитории? со статусом 200
3. Изменение названия задачи на "Issue 2":
   - В Postman откройте новый запрос и выберете метод "PATCH".
   - Введите URL:  http://api.github.com/repos/{owner}/{repo}/issues/{issue_number}, где {owner}-владелец репозитория, {repo}- название репозитория, {issue_number}- номер нужной issue, полученный в запросе POST.
   - В разделе "Headers" добавьте заголовок "Autorization" с значением "Bearer {token}.
   - В разделе "body" выберете формат RAW и тип "JSON".
   - В поле ввода введите следующий JSON-код:
     {
     "title":"Issue 2"
     }
   - Нажмите кнопку "Send" для отправки запроса. В ответ вы получите информацию о обновленной Issue, со статусом 200.
4. Удаление "Issue 2":
   - В Postman откройте новый запрос и выберете метод "DELETE".
   - Введите URL: http://api.github.com/repos/{owner}/{repo}/issues/{issue_number2}/lock, где {owner}-владелец репозитория, {repo}- название репозитория, {issue_number2}- номер нужной issue, полученный в запросе PATCH.
   - В разделе "Headers" добавьте заголовок "Autorization" с значением "Bearer {token}.
   - Нажмите кнопку "Send" для отправки запроса. В ответ вы получите информацию об удаленной issue со статусом 204.  
P.S.: Для использования API GitHub issues необходимо создать аккаунт на GitHub, создать репозиторий и получить API-ключ для соответствующего приложения.      

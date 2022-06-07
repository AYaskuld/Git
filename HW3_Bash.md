## Задание ##  
**1. На локальном репозитории сделать ветки для:**  
- Postman
- Jmeter
- CheckLists
- Bag Reports (баг в названии принимаю Bug_report)
- SQL
- Charles
- Mobile testing

**2. Запушить все ветки на внешний репозиторий**  
**3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта**  
**4. Запушить структуру багрепорта на внешний репозиторий**  
**5. Вмержить ветку Bag Reports в Main**  
**6. Запушить main на внешний репозиторий.**  
**7. В ветке CheckLists набросать структуру чек листа.**  
**8. Запушить структуру на внешний репозиторий**  
**9. На внешнем репозитории сделать Pull Request ветки CheckLists в main**  
**10. Синхронизировать Внешнюю и Локальную ветки Main**  
## Решение ##
  
**1. На локальном репозитории сделать ветки для:**  
- Postman
- Jmeter
- CheckLists
- Bag Reports (баг в названии принимаю Bug_report)
- SQL
- Charles
- Mobile testing

```bash
Git branch Postman
Git branch Jmeter
Git branch CheckLists
Git branch Bug_report
Git branch SQL
Git branch Charles
Git branch Mobile_testing
```
**2. Запушить все ветки на внешний репозиторий**  
```bash
git push --all
```
**3. В ветке Bug_Reports сделать текстовый документ со структурой баг репорта**  
Для удобства, я дополнительно создал папку Bug_reports и создал файл в этой папке  
```bash
git chechout Bug_Reports
mkdir Bug_reports
nano Bug_reports/bug_reports.txt
```
```Добавляю структуру баг репорта и сохраняю```  
  
**4. Запушить структуру багрепорта на внешний репозиторий**  
```bash
git push --force -u origin Bug_reports
```
**5.Вмержить ветку Bag Reports в Main**  
```bash
git checkout main
git merge Bug_Reports (чувствительно к регистру)
```
**6.Запушить main на внешний репозиторий**  
```bash
Git push
```
**7. В ветке CheckLists набросать структуру чек листа**  
Для удобства, я дополнительно создал папку CheckLists и создал файл в этой папке  
```bash
git checkout Checklists
mkdir CheckLists
nano CheckLists/checklists.txt
```
```Добавляю структуру чек листа и сохраняю```  
  
**8. Запушить структуру на внешний репозиторий**  
```bash
git add --a
git commit -m creating_chechlists.txt
git push --force -u origin Checklists
```
**9. На внешнем репозитории сделать Pull Request ветки CheckLists в main** 
В задании не сказано, но для того что бы выполнить задание 10. также необходимо выполнить merge  
```//Жму на кнопку pull request```  
```//добавляю коментарий, соглашаюсь и жму merge```  

**10. Синхронизировать Внешнюю и Локальную ветки Main**  
```bash
git pull
```

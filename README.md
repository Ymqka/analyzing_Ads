# analyzing_Ads
предсказать является ли статья рекламой
буду писать процесс и идеи сюда

процесс:
1) найти данные
2) обучить модель
3) изучить ошибки
4) повторить п.1 и п.2, затем 3
_________________________________________________
пример парсера взят отсюда https://habr.com/post/346198/, так же был использован код из статьи.
Нашел на медузе спонсорские статьи попытавшись спарсить страницу у меня парсило новости годовой 
давности. Попытавшись погуглить проблему, наткнулся на библиотеку silenium, очень удобная вещь,
получилось спарсить все нужные мне ссылки в лист. C silenium мне помогли статья
https://python-scripts.com/web-automation-with-python-and-selenium и документация самого silenium'a.
Теорию процесса очистки данных взял отсюда https://www.kdnuggets.com/2017/12/general-approach-preprocessing-text-data.html
реализацию частично гуглил. Визуализация очень была полезной эта статья:https://www.kaggle.com/jagangupta/stop-the-s-toxic-comments-eda. на train-test-split наивный Байесовский классификатор показывает около 0.95, это неплохой классификатор, хоть и не лучший, в тесте буду пытаться найти лучше, так же спарсю статьи не из медузы и провверю классификатор на них.




__________________________________________________
cleaning_ads_data.ipynb - очистка собранных данных из рекламных статей
cleaning_nonads_data.ipynb - очистка собранных данных из обычных статей
parsing_ads.ipynb - парсинг рекламных статей
parsing_nonads.ipynb - парсинг обычных статей
vizualizing and training.ipynb - визуализация, тренировка и тест классификатора
testeing.ipynb - проверка классификатора на статьях не из медузы
data -| папка с данными 
      | 
      - cleaned_ads_data.csv - очищенные данные из рекламных статей
      - cleaned_nonads_data.csv - очищенные данные из обычных статей
      - parsed_ad_data.csv - спарсенные неочищенные данные из рекламных статей
      - parsed_nonad_data.csv - спарсенные неочищенные данные из обычных статей
      - tested_data.csv - соединеные очищенные данные из рекламных и обычных статей

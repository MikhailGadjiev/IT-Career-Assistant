Отчет представляет собой:
1.	Модуль предсказания позиций
Источник данных: Датасет IT-Salary-Europe-2020 с Kaggle, содержащий результаты опроса зарплат IT-специалистов в Европе за 2020 год.
Ключевые характеристики:
o	1,253 записи
o	9 параметров на запись
o	Включает данные о зарплатах, уровне специалистов, технологиях и условиях работы

Модель машинного обучения:
o	Алгоритм: CatBoostClassifier
o	Выбор обоснован более высокой точностью (60.2%) по сравнению с Decision Tree (58.5%)
o	Используемые признаки:
-	Демографические (возраст, пол)
-	Профессиональные (уровень, технологический стек)
-	Организационные (тип контракта, размер компании)
-	Финансовые (зарплата в рублях)
Функционал: Предсказывает топ-5 наиболее вероятных позиций с указанием вероятности для каждого варианта.

3.	Модуль анализа вакансий
Источники данных:
o	Парсинг актуальных IT-вакансий с hh.ru (последние 3 дня)
o	Парсинг технических статей с Habr.com (за последний год)

Структура данных:
o	Вакансии (df_jobs):
	5 полей включая ключевые навыки, описание и зарплатные вилки
	500+ записей (больше нельзя – мне дают предупреждения)
o	Статьи (df_articles):
	Рейтинги, хештеги, полные тексты
	2000+ статей
Технологическая реализация:
o	NLP-обработка навыков (TF-IDF + косинусная близость)
o	Рекомендательная система:
1.	Сравнение навыков пользователя с требованиями вакансий
2.	Выявление недостающих компетенций
3.	Подбор релевантных обучающих материалов
2.	Интеграция компонентов
Единый интерфейс предоставляет:
o	Персональные карьерные рекомендации
o	Анализ рыночного спроса на навыки
o	Образовательные траектории для профессионального роста
Уникальные особенности:
o	Комбинация методов ML и NLP
o	Практико-ориентированные рекомендации



Литература

[1] LinkedIn. (2025). [Online]. Available: http://linkedin.com 
[2] Coursera. (2025). [Online]. Available: https://www.coursera.org 
[3] Changellenge. (2025). [Online]. Available: https://changellenge.com/ 
[4] A. Géron, Hands-on Machine Learning with Scikit-Learn, Keras, and TensorFlow: Concepts, Tools, and Techniques to Build Intelligent Systems, 3rd ed. O’Reilly Media, Inc., 2022.
[5] J. Gehrke and N. Ye, “Decision tree,” in The Handbook of Data Mining, Lawrence Erlbaum Associates, 2003, pp. 3–23.
[6] A. Cutler, D. R. Cutler, and J. R. Stevens, “Random forests,” in Ensemble Machine Learning: Methods and Applications, Springer, 2012, pp. 157–175.
[7] O. Kramer, “K-nearest neighbors,” in Dimensionality Reduction with Unsupervised Nearest Neighbors, Springer, 2013, pp. 13–23.
[8] C. Bentéjac, A. Csörgő, and G. Martínez-Muñoz, “A comparative analysis of gradient boosting algorithms,” Artificial Intelligence Review, vol. 54, pp. 1937–1967, 2021.
[9] D. Jurafsky and J. H. Martin, Speech and Language Processing: An Introduction to Natural Language Processing, Computational Linguistics, and Speech Cognition, draft (2023), 2024.
[10] G. Jawahar, B. Sagot, and D. Seddah, “What does BERT learn about the structure of language?,” in Proc. 57th Annu. Meet. Assoc. Comput. Linguist. (ACL), 2019, pp. 1–12.
[11] C. Zhou et al., “A comprehensive survey on pretrained foundation models: A history from BERT to ChatGPT,” Int. J. Mach. Learn. Cybern., pp. 1–65, 2024.
[12] hh.ru. (2025). [Online]. Available: https://hh.ru/ 
[13] Habr. (2025). [Online]. Available: https://habr.com/ru/ 
[14] IT Salary Europe 2020. (2020). [Online]. Available: https://github.com/leahsaurus/IT-Salary-Europe-2020 
[15] https://www.hse.ru/edu/vkr/835939310 

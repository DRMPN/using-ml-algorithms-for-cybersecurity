# using-ml-algorithms-for-cybersecurity

[![OSA-improved](https://img.shields.io/badge/improved%20by-OSA-yellow)](https://github.com/aimclub/OSA)

Разработано с использованием:

![numpy](https://img.shields.io/badge/NumPy-013243?logo=NumPy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![scipy](https://img.shields.io/badge/SciPy-8CAAE6?logo=SciPy&logoColor=white)
![tqdm](https://img.shields.io/badge/tqdm-FFC107?logo=tqdm&logoColor=black)

---

## Обзор

Проект предлагает унифицированный ресурс, который превращает необработанные сетевые данные и связанные артефакты в практические сведения об угрозах, обеспечивая точную идентификацию вредоносного трафика, доменов и команд. Он упрощает настройку моделей и предоставляет практические учебные материалы, давая командам безопасности и обучающимся преимущество в современной киберзащите.

---

## Содержание

- [Обзор](#overview)
- [Ключевые возможности](#core-features)
- [Установка](#installation)
- [Вклад](#contributing)
- [Цитирование](#citation)

---

## Ключевые возможности

1. **Всеобъемлющая инженерия признаков потоков пакетов**: Генерирует сырые, статистические и объединённые признаки пакетов (например, `tcp_len_*`, энтропия, отношения клиент/сервер) с помощью специализированных вспомогательных функций, таких как `process_flow` и `extract_statistical_features`, чтобы описать каждый сетевой поток в окнах по 30 пакетов.  
2. **Автоматизированная оптимизация гиперпараметров с LightGBM**: Использует `RandomizedSearchCV` для настройки многоклассового классификатора LightGBM по десяткам параметров (число деревьев, листья, глубина, bagging и др.) для точной идентификации приложений-сервисов.  
3. **Конвейер обнаружения вредоносных HTTP**: Извлекает TF-IDF символьные n-граммы из полей HTTP-запросов/ответов плюс разработанные вручную признаки URL (длина, энтропия, флаги шестнадцатеричных строк) и подаёт их в классификатор XGBoost с агрегацией признаков на уровне файлов.  

---

## Установка

Сборка из исходников:

```sh
git clone https://github.com/DRMPN/using-ml-algorithms-for-cybersecurity
cd using-ml-algorithms-for-cybersecurity
pip install -r requirements.txt
```

---

## Вклад

- **[Сообщить об ошибке](https://github.com/DRMPN/using-ml-algorithms-for-cybersecurity/issues)** — отправьте сообщения об ошибках или запросы новых функций.  
- **[Отправить Pull Request](https://github.com/DRMPN/using-ml-algorithms-for-cybersecurity/tree/main/.github/CONTRIBUTING.md)** — ознакомьтесь с руководством по внесению вкладов.  

---

## Цитирование

Если вы используете это программное обеспечение, пожалуйста, цитируйте его следующим образом.

### APA

DRMPN (2025). using-ml-algorithms-for-cybersecurity repository [Computer software]. https://github.com/DRMPN/using-ml-algorithms-for-cybersecurity

### BibTeX

```bibtex
@misc{using-ml-algorithms-for-cybersecurity,
  author       = {DRMPN},
  title        = {using-ml-algorithms-for-cybersecurity repository},
  year         = {2025},
  publisher    = {GitHub},
  howpublished = {\url{https://github.com/DRMPN/using-ml-algorithms-for-cybersecurity}},
  url          = {https://github.com/DRMPN/using-ml-algorithms-for-cybersecurity}
}
```

---

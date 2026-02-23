# Тесты из DOCX/TXT (Streamlit)

Это веб‑приложение на **Streamlit**, которое загружает тесты из **.docx** или **.txt**, показывает вопросы/варианты, поддерживает картинки/формулы и разметку правильных ответов.

## Структура репозитория

```
.
├─ app_fixed9.py
├─ requirements.txt
├─ packages.txt
├─ runtime.txt
└─ .streamlit/
   └─ config.toml
```

## Локальный запуск (на ПК)

1) Установите зависимости:
```bash
pip install -r requirements.txt
```

2) Запуск:
```bash
streamlit run app_fixed9.py
```

Откроется в браузере по адресу, который покажет Streamlit (обычно http://localhost:8501).

## Деплой в Streamlit Community Cloud

1) Загрузите этот репозиторий в GitHub (обычно public для бесплатного тарифa).
2) В Streamlit Community Cloud нажмите **Create app** → выберите репозиторий/ветку.
3) Укажите main file path: `app_fixed9.py` → **Deploy**.

После деплоя получите ссылку `https://<name>.streamlit.app` — её можно открыть на Android в браузере.

## ImageMagick и формулы/картинки (WMF/EMF)

`packages.txt` включает `imagemagick`. Он нужен, чтобы конвертировать WMF/EMF → PNG.
Без него приложение всё равно работает, но некоторые формулы‑картинки могут не отображаться.

---
Если хотите, можно убрать ImageMagick: просто удалите `packages.txt`.

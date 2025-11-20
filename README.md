# Python CI GitHub Actions Project

Бұл репозиторий Python үшін толық жұмыс істейтін минималды жобаны көрсетеді, оның GitHub Actions CI workflow арқылы автоматты тестілеу жасалады.


## Қалай жұмыс істейді

1. `app.py` ішіндегі функцияны тестілейтін `tests/test_app.py` файлы бар.
2. `requirements.txt` ішінде тестілеуге қажет тәуелділік: `pytest`.
3. `.github/workflows/python-ci.yml` файлы workflow-ды анықтайды:
   - Кодты `push` немесе `pull_request` кезінде тексереді
   - Python 3.11 орнатады
   - Тәуелділіктерді орнатады
   - Тестілерді іске қосып нәтижесін сақтайды

## Орнату және пайдалану

```bash
# Репозиторийді клондау
git clone https://github.com/<пайдаланушы>/<репозиторий>.git
cd red

# Виртуалды орта жасау (қалауыңыз бойынша)
python -m venv venv
source venv/bin/activate   # Linux / Mac
venv\Scripts\activate      # Windows

# Тәуелділіктерді орнату
pip install -r requirements.txt

# Тестілерді іске қосу
pytest



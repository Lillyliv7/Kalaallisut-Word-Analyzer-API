# Greenlandic Word Analyzer API

## Installing & Running

Requirements: Python 3.11 (Currently HFST does NOT work with the latest Python version), fastapi, uvicorn, hfst

```
git clone https://github.com/Lillyliv7/Kalaallisut-Word-Analyzer-API
cd Kalaallisut-Word-Analyzer-API
python3 -m venv venv
source venv/bin/activate
pip3 install fastapi uvicorn hfst
python3 api.py
```

## Usage

Example Analysis: http://localhost:8000/analyze?word=oqaluffik

You can change the port by changing the port argument on the last line of code in api.py

Output:
```
{
   "word":"oqaluffik",
   "analyses":[
      {
         "raw":"@P.LEXNAME.Root@oqalup@P.LEXNAME.IV_k_UTE_gennemgang@+Gram/IV@P.LEXNAME.IV_k2@+Gram/IV@P.LEXNAME.flex-iv2@@C.nar@@P.LEXNAME.flex_iv2_nominalizers@@_EPSILON_SYMBOL_@@_EPSILON_SYMBOL_@@_EPSILON_SYMBOL_@+VIK+Der/vn@P.LEXNAME.vik_vn@@C.Num@@U.gunnaarfik.ON@@U.kkut.OFF@@U.kuq.OFF@@U.vvik.ON@@P.LEXNAME.Z2-Zmorf@@U.Num.Sg@@P.LEXNAME.tup_singular@+N+Abs+Sg@P.LEXNAME.Krestr@",
         "cleaned":"oqalup+Gram/IV+Gram/IV+VIK+Der/vn+N+Abs+Sg",
         "weight":0.0
      }
   ]
}
```

## Credits
https://github.com/giellalt/lang-kal/ , for the analyser file.

# 가상환경 세팅 및 패키지 설치
>|date|name|
>| -----|----|
>|`2021.12.29` |`연세대학교 디지털애널리티스 석사 3학기 용지호` |

----
## 사전 세팅
- **MAC 터미널**
### 1. 파이썬 버전 확인
```angular2html
python3 --version && which python3
python --version && which python
```
![python version](img/python_version.png)

-----
 ### 2. 가상 환경 확인

- ### **conda**
```angular2html
conda info
```
![python version](img/conda_info.png)

- conda 인식 못할 때 bash profile 에 conda path 입력 필요
```angular2html
cd ~/opt/anaconda3/bin
pwd
## export PATH="path:$PATH"
source ~/.bash_profile
```

- ### **venv**

```angular2html
cd /usr/local/opt && ls | grep python*
```

![venv_python](img/venvpython.png)

----

### 3. 가상환경 생성
>- conda 의 경우 python 버전 3.6.8
>- venv 의 경우 크게 상관 없음

- ### **conda**
- 가상환경 생성 
```angular2html
conda create --name tf_nlp python=3.6.8 
conda env list
```


- 가상환경 실행
```angular2html
conda activate tf_nlp
pip freeze
```
- 주피터 노트북에 가상환경 등록
```angular2html
pip install ipykernel
python -m ipykernel install --user --name tf_nlp --display-name "tf_nlp"
```


- 만든 가상환경 삭제하고 싶을 때
```angular2html
conda remove --name tf_nlp --all
```

### 4. JAVA 버전 확인 및 설치

### 5. 패키지 설치
> **본인이 사용하는 가상환경 실행한 뒤 해당 pip install 하기**

```angular2html
pip install tensorflow && pip install konlpy && pip install tweepy==3.10

```
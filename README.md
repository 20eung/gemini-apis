# Gemini API 키를 교체하며 gemini-cli를 사용하는 방법

## 1. Google Cloud API KEY를 발급받는다.

### 1.1 Google Cloud 접속
* https://console.cloud.google.com 접속
* Gmail 계정으로 로그인
* 신규 프로젝트 생성 및 선택
* 아래 내용은 수행하지 않아도 될것 같음
  - 햄버거버튼 클릭 >> API 및 서비스 >> 사용자 인증 정보
  - 상단에서 + 사용자 인증 정보 만들기 >> API 키
  - 생성된 API 키 복사, 보관

### 1.2 모든 Google 계정으로 동일하게 수행하여 프로젝트를 생성한다.

## 2. Google AI Studio 접속

### 2.1 Google AI Studio 접속
* https://aistudio.google.com 접속
* Gmail 계정으로 로그인
* 좌측상단 햄버거버튼 클릭 >> API kyes 클릭
* 우측상단 **+ API 키 만들기** 클릭
* 기존 Google Cloud 프로젝트에서 프로젝트 선택 >> 검색 창 클릭하여 프로젝트 선택
* **기존 프로젝트에 API 키 만들기** 클릭
* API키 생성됨 >> 키 복사

### 2.2 모든 Google 계정으로 동일하게 수행하여 API 키를 발급받는다.
* 좌측상단 햄버거버튼 클릭 >> 좌측하단 gmail 계정 클릭하여 계정 전환

## 3. Alias 설정

### 3.1 ~/.bash_aliases 파일에 아래 내용을 적는다

```bash
# Gemini-CLI API Keys
# 
export GEMINI_API_KEY1="AIzaSy~~~"
alias g1='export GEMINI_API_KEY= GEMINI_API_KEY1; gemini -c'
# 
export GEMINI_API_KEY2="AIza~~~"
alias g2='export GEMINI_API_KEY= GEMINI_API_KEY2; gemini -c'
# 
export GEMINI_API_KEY3="AIzaSy~~~"
alias g3='export GEMINI_API_KEY= GEMINI_API_KEY3; gemini -c'
# 
export GEMINI_API_KEY4="AIzaSy~~~"
alias g4='export GEMINI_API_KEY= GEMINI_API_KEY4; gemini -c'
# 
export GEMINI_API_KEY5="AIzaSy"
alias g5='export GEMINI_API_KEY= GEMINI_API_KEY5; gemini -c'
# 
export GEMINI_API_KEY6="AIzaSy~~~"
alias g6='export GEMINI_API_KEY= GEMINI_API_KEY6; gemini -c'
# 
export GEMINI_API_KEY7="AIzaSy~~~"
alias g7='export GEMINI_API_KEY= GEMINI_API_KEY7; gemini -c'
# 
export GEMINI_API_KEY8="AIzaSy"
alias g8='export GEMINI_API_KEY= GEMINI_API_KEY8; gemini -c'
```

### 3.2 ~/.bashrc 파일에 아래 내용을 적는다.
```bash
if [ -f ~/.zsh_aliases ]; then
  source ~/.zsh_aliases
fi
```

## 4. gemini-cli 사용 중

### 4.1 토큰을 모두 소진하면 /quit 또는 Ctrl-D 로 종료

### 4.2 g1 사용중이었다면 g2, 이어서 g3, g4 ... 사용
```bash
g2
```


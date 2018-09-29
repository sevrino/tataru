# 타타루(Tataru)
[![Build Status](https://travis-ci.org/WoodNeck/tataru.svg?branch=staging)](https://travis-ci.org/WoodNeck/tataru)

한국어 명령어를 받는 디스코드용의 다목적 봇입니다.

접두사는 "타타루"로 고정되어있지만, main.py 파일에서 수정 가능합니다.

# Prerequisites
- Python version 3.5 or higher
- Discord Bot User Token
    - (https://discordapp.com/developers/applications/me)
- Naver Client ID & Secret to use "Naver" cog
    - (https://developers.naver.com/apps/#/register)

# Installing
## Linux
1. Clone this repository

```
git clone https://github.com/WoodNeck/tataru.git
```

2. Install dependencies

```
sudo apt-get install python3-pip
sudo pip3 install discord
sudo pip3 install requests
sudo pip3 install Pillow
sudo pip3 install python-dateutil
sudo apt-get install libopus-dev
sudo pip3 install pynacl
sudo pip3 install youtube_dl
sudo add-apt-repository ppa:mc3man/trusty-media
sudo apt-get update
sudo apt-get dist-upgrade
sudo pip3 install lxml
sudo pip3 install wordcloud
```

3. Execute main.py
```
cd tataru
sudo python3 main.py
```

# 명령어
## General
#### 골라줘
`타타루` `골라줘` `고를` `대상` `들`
```
타타루 골라줘 하나 둘 셋
>>하나
```
여러 가지 인자들 중 하나를 골라줍니다.

*****

#### 따귀
`타타루` `따귀` `대상`
```
타타루 따귀 @찬피
>>@찬피의 뺨을 후려갈겼어용
```
주어진 대상의 따귀를 후려갈깁니다.

*****

#### 주사위
`타타루` `주사위` `최대숫자`
```
타타루 주사위
>>@WoodNeck이(가) 주사위를 굴려 🎲30이(가) 나왔어용
타타루 주사위 1000
>>@WoodNeck이(가) 주사위를 굴려 🎲174이(가) 나왔어용
```
1~100 사이의 주사위를 굴립니다. 1보다 큰 인자가 주어질 경우 1과 해당 인자 사이의 주사위를 굴립니다.

*****

#### 핑
`타타루` `핑`
```
타타루 핑
>>퐁이에용
```
테스트용, 퐁을 표시합니다.

*****

#### 초대
`타타루` `초대`
```
타타루 초대
>>https://discordapp.com/oauth2/authorize?client_id=357073005819723777&scope=bot&permissions=-1
```
타타루 봇 초대용 링크를 표시합니다.

*****

#### 전역일
추가 : `타타루` `전역일` `추가해줘`
```
타타루 전역일 추가해줘
>>등록할 이름을 말해주세용
WN
>>입대일자를 YYYY/MM/DD 양식으로 말해주세용
2013/01/02
>>육군, 공군, 공익중에 어디에 입대했나용?
공군
>>:airplane:️WN을(를) 추가했어용!
```
새로운 전역일을 추가합니다. 

확인 : `타타루` `전역일` `이름`
```
:airplane:️WN의 복무정보에용
입대일: 2013-01-02
전역일: 2015-01-01
복무한 날: 1896일
남은 날: -1167일
오늘까지 복무율: 260.08%
```
해당 이름의 전역일 정보를 표시합니다.

*****

#### 수능
`타타루` `수능`

2018년 수능일까지 남은 시간을 표시합니다.

*****

#### 투표
`타타루` `투표` `질문` `(옵션1)` `(옵션2)` `...`

채팅 내에서 1분간 투표를 받고, 1분 후에 그 결과를 표시합니다.

투표는 Emoji reaction을 통해 가능합니다.

옵션은 최대 10개까지 가능합니다.

*****

#### 나무위키
`타타루` `나무위키` `검색어`

나무위키의 문서를 가져와서 Discord Embed형식으로 표시합니다.

*****

#### 파일관리
`타타루` `파일관리`

타타루의 파일관리용 url을 표시합니다.

## Naver
#### 지식인
`타타루` `지식인` `물어볼 내용`
물어볼 내용에 해당하는 지식인 검색 결과를 표시합니다.

*****

#### 번역
`타타루` `번역할 언어`로 `번역해줘/기계번역해줘` `번역할 내용`
```
타타루 영어로 번역해줘 안녕하세요
>>Hello.
타타루 영어로 기계번역해줘 안녕하세요
>>你好。
```

네이버의 Papago SMT와 NMT API를 사용한 한국어->외국어 번역 기능입니다.

`번역해줘` 사용시 Papago SMT API를, `기계번역해줘` 사용시 Papago NMT API를 사용합니다.

`번역해줘` 사용시 `영어`, `중국어`, `일본어`로 번역 가능합니다.

`기계번역해줘` 사용시 `영어`, `중국어`로 번역 가능합니다.

*****

#### 로마자변환
`타타루` `로마자변환` `변환할 인명`
```
타타루 로마자변환 홍길동
>> Hong Gildong
```
네이버 API를 이용, 인명을 로마자변환한 결과를 받아옵니다.

*****

#### 얼굴인식
`타타루` `얼굴인식` `인식할 이미지 URL`

네이버 API를 이용, 이미지에서 얼굴인식된 결과를 받아옵니다. 얼굴인식 결과에는 감정, 성별, 나이, 닮은 연예인과 같은 정보가 포함되어 있습니다.

*****

#### 네이버이미지
`타타루` `네이버이미지` `검색할 내용`

네이버의 이미지 검색 결과를 받아옵니다.

*****

#### TTS
`타타루` `tts` `말할 내용`

`말할 내용`에 해당하는 텍스트를 디스코드의 음성 채팅에서 재생합니다.

## Google
#### 이미지
`타타루` `이미지` `검색할 내용`

구글의 이미지 검색 결과를 받아옵니다.

*****

#### 유튜브
`타타루` `유튜브` `검색어`

유튜브 영상 검색 결과를 하나씩 표시합니다.

표시되는 이모지 메뉴를 통해 이전/재생/다음/취소를 시행 가능합니다.

`타타루` `유튜브` `재생해줘` `유튜브 url`

유튜브 영상을 현재 타타루의 플레이리스트에 추가하여 재생합니다.

```
https://www.youtube.com/watch?v=0wVlsPVrbkk&list=UUtSeJlS4Z9UCqdQzOQGF8sg
```

유튜브 url은 위와 같이 도중에 list를 포함시 리스트의 상단부터 최대 50개까지 타타루의 플레이리스트에 추가합니다.

## Jjal
#### 단어 - 이미지 변환
`폴더명` `이미지명`

`파일관리` 명령어를 통해 업로드한 이미지에 대해, 위와 같은 형식으로 메시지 입력시 해당 이미지를 디스코드 채팅창에 업로드합니다.

`짤` 폴더는 디폴트 폴더로, 해당 폴더 내부의 이미지는 폴더명 없이도 트리거됩니다.

## Sound
#### 재생해줘
`타타루` `재생해줘` `mp3명`

`파일관리` 명령어를 통해 sound폴더 내에 업로드한 mp3 파일을 재생합니다.

*****

#### 정지
`타타루` `정지`

현재 재생하던 노래를 정지하고, 재생목록을 파기합니다.

*****

#### 스킵
`타타루` `스킵`

현재 재생하는 노래를 스킵합니다.

*****

#### 취소
`타타루` `취소` `번호`

현재 재생목록의 `번호`에 해당하는 항목을 취소합니다.

*****

#### 재생목록
`타타루` `재생목록`

현재 재생목록을 표시합니다.

*****

#### 현재곡
`타타루` `현재곡`

현재 재생하는 노래에 대한 정보를 표시합니다.

*****

#### 루프
`타타루` `루프`

재생목록 반복을 설정/해제합니다.

## Dangerous Invite
#### 위험한초대
`타타루` `위험한초대`

위험한초대 게임을 만듭니다.

Creates a new game of "Dangerous Invite"

명령어 (`타타루 위험한초대`) 입력시 DM을 받고, DM을 통해 3글자의 단어 입력시 위험한초대 게임이 시작됩니다.

게임 시작시 24시간의 시간이 주어지며, 시간 내에 시작한 봇을 제외한 어떤 유저든 해당 단어가 포함된 단어를 말할 시 서버에서 추방되고 게임이 종료됩니다. 혹은 24시간의 시간이 지날시 게임을 시작한 사람이 서버에서 추방됩니다.

## GG2
#### GG2 Bubble 변환
채팅 메시지가 GG2 bubble에 해당하는 메시지일시 해당 버블 이미지를 전송.

- 사용가능한 GG2 Bubbles (Available GG2 Bubbles)
    - `z1` ~ `z9`
    - `x1` ~ `x29`
    - `c1` ~ `c9`
    - `e`
    - `센트리`
    - `우버`

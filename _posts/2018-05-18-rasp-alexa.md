---
title: Using Alexa in Raspberry Pi3 <br> 라즈베리파이3로 알렉사 사용하기
categories: project
tags: 
---

## 라즈베리파이3 환경 구축하기
* 라즈베리파이3 환경 구축하기z
 1. [https://www.raspberrypi.org/](https://www.raspberrypi.org/)에서 최신버전의 Raspbian(OS)를 다운 받습니다. <br/> (RASPBIAN STRETCH WITH DESKTOP ver4.14를 사용했습니다.)
 2. Win32 Disk Imager를 이용해서 SDCard에 이미지를 구워줍니다.
 3. SDCard를 꽂고 전원을 켜줍니다.
 4. Raspberry Pi Configuration에서 필요한 설정을 마칩니다.

* Amazon 개발자 계정 만들기
 1. ID가 없을 경우 회원가입을 누르고 회원가입을 진행합니다.
 2. 아마존 개발자 홈페이지에서 Alexa를 선택해 줍니다.
 3. Alexa Voice Service 탭을 선택해줍니다.
 4. AVSConsole 탭에 들어가서 새로운 Product를 만들어줍니다.
 5. Security Profiles에서 새로운 Security Profile을 만들어 줍니다.

* Alexa 설치하기
 1. Alexa 설정과 관련된 내용을 적어 둘 파일하나를 만듭니다. <br/> 파일에 아래의 내용들을 적어 둡니다. <br/>채울 내용들은 Alexa 생성할 때와 Security profile을 만들던 곳에서 확인할 수 있습니다. <br/>Product name: Alexa <br/>Amazon ID:  <br/>Product ID: Alexa Example <br/>Security Profile ID: <br/> Client ID:  <br/> Client Secret: <br/>
 2. 터미널창을 열어서 Raspbian을 업데이트 합니다. <br/> sudo apt-get update <br/> sudo apt-get upgrade -y <br/> shutdown -r now
 3. git을 이용하여 AlexaPi를 받아와 설치합니다. <br/> `cd /opt` <br/>`sudo apt-get install git`<br/>`sudo git clone https://github.com/alexa-pi/AlexaPi.git`<br/>`sudo ./AlexaPi/src/scripts/setup.sh`<br/>설치시 질문은 몇개만 대답하면 됩니다.<br/>`Which operating system are you using? debian [enter]`<br/>`Which device are you using? raspberrypi [enter]`<br/>`Do you want AlexaPi to run on boot? 1 - yes, use systemd (default, RECOMMENDED and awesome)`<br/>`Would you like to install Airplay support? n (unless you want it, then enter Y)`<br/>`Enter your Device Type ID: Alexa_Example`    <br/>`(Device Type ID는 product ID와 같습니다)`<br/>`Enter your Security Profile Description: `<br/>`AlexaPi Security Profile`<br/>`Enter your Security Profile ID: amzn1.application.xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`<br/>`Enter your Client ID: amzn1.application-oa2-client.xxxxxxxxxxxxxxxxxxx`<br/>`Enter your Client secret: a8dd0a1e3d7exxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`<br/>이 때 질문을 다하고 마지막에 Ctrl-C 와 같이 설치가 완료되었다면 종료를 하라는 문구가 나올텐데 이 때 잘보면 <br/> Ready goto http://192.168.xxx.xx:5050 or http://localhost:5050 이런 문구를 찾을 수 있는데 터미널창을 끄지말고 인터넷을 열어 위 주소로 접속하여 인증을 받습니다. <br/> 인증 받았다면 재부팅을 합니다. (sudo shutdown -r now)
 4. 재부팅 할 때 알렉사가 Hello 라고 말을 해야 합니다. 또는 “알렉사”라고 말하면 “yes”라고 답할 것입니다.<br/>"What does Gordon Ramsay think of my dish?"  라고 묻는다면 평가를 해줄지도 모릅니다.
```
아래의 사이트를 참고하여 만들었습니다.
https://pchelp.ricmedia.com/build-alexapi-with-amazon-alexa-raspberry-pi/
```
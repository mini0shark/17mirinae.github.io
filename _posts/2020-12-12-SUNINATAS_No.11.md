---
layout: post
title: "SUNINATAS No.11"
date: 2020-12-12 01:29:00
categories: SUNINATAS
tags: SUNINATAS
---

써니나타스의 11번 문제는 리버싱 문제다.

<img src="/assets/image/2020-12-12-SUNINATAS_No.11/1.png" width="100%" height="100%" />

Download 를 클릭하면 Unregister.zip 파일을 다운로드 할 수 있다.

압축을 풀면 Register.exe 파일을 얻을 수 있다.

<img src="/assets/image/2020-12-12-SUNINATAS_No.11/2.png" width="100%" height="100%" />

일단 이 프로그램을 실행시켜 보았다.

<img src="/assets/image/2020-12-12-SUNINATAS_No.11/3.png" width="100%" height="100%" />

AAAAAAA 를 넣어서 Register 버튼을 눌렀는데 아무런 메시지가 안 떠서 살짝 당황했지만 침착하게 해당 파일을 올리디버거로 열어보았다.

<img src="/assets/image/2020-12-12-SUNINATAS_No.11/4.png" width="100%" height="100%" />

마우스 오른쪽 버튼을 눌러 Search for - All referenced text strings 를 클릭한다.

<img src="/assets/image/2020-12-12-SUNINATAS_No.11/5.png" width="100%" height="100%" />

창을 크게 띄우고 살펴보면 마지막에 Congratulation 문구와 AuthKey 를 출력해주는 듯한 문구를 확인할 수 있다.

<img src="/assets/image/2020-12-12-SUNINATAS_No.11/6.png" width="100%" height="100%" />

바로 돌아와서 해당 명령어의 위치를 확인한다.

<img src="/assets/image/2020-12-12-SUNINATAS_No.11/7.png" width="100%" height="100%" />

<img src="/assets/image/2020-12-12-SUNINATAS_No.11/8.png" width="100%" height="100%" />

위에 저 다섯 개의 문자들을 EDX 로 넣어주는 것을 보고 이걸 조합하여 입력하면 AuthKey 를 얻을 수 있을 것 같아서 PUSH 되는 순서대로 문자를 조합해보았다.

​
EBX + 310 = 2V  
EBX + 318 = B6  
EBX + 31C = H1  
EBX + 314 = XS  
EBX + 320 = 0F  
==> 2VB6H1XS0F


조합을 완료했으면 Project1.exe 를 실행시켜 입력해준다.

<img src="/assets/image/2020-12-12-SUNINATAS_No.11/9.png" width="100%" height="100%" />

해결이다.
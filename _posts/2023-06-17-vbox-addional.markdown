---
layout: post
title: "VirtualBox Guest Additions 설치 에러"
date: 2023-06-17 12:16:00 +0900
categories: hack
---

최근 [핸즈온 해킹](https://play.google.com/store/books/details?id=r7ZIEAAAQBAJ) 책을 보고 있다. 해킹을 위한 실습 환경 구성을 위해 버추얼 박스에서 칼리 리눅스 환경을 구성해서 사용하고 있는데, 버추얼 박스의 기본 해상도는 640 x 480 이기 때문에 글씨가 작아보이는 것을 피할 수 없다.

때문에 사용하고 있는 컴퓨터의 해상도를 지원하기 위해서 버추얼 박스 게스트 에디션을 설치해주면 되는데 역시 리눅스 환경이라 쉽지 않더랬다.

![vbox-guest](/assets/hack/vbox-guest.jpg)

때문에 해당 버튼을 누르게 되면 게스트 에디션의 iso 파일은 자동으로 다운로드 되어 CD와 같이 불러와 진다. 그리고 시디의 위치로 이동한 뒤 `autorun.sh` 를 실행시켜 주면 설치가 되어야 하는데... 뭔가 설치가 되는 듯 싶은 스크립트가 나오더니 중간에 경고 같은 오류가 생기는 것이었다. linux-headers를 찾지 못했다라는 메시지.

인터넷을 검색해보니 간단하게 해결되는 문제였다.

`apt-cache search linux-headers`

`apt-get install linux-headers-[필요한 리눅스 버전]-amd64`

끝!

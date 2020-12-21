---
layout: post
title:  "1.CALDERA 설치 하기"
date:   2020-12-22 01:12:07 +0900
categories: jekyll update
---

CALDEAR 란 MITRE ATT&CK® 에서 제작한 보안 프레임 워크이다.  
[https://github.com/mitre/caldera](https://github.com/mitre/caldera/)  
해당 링크를 통해 소스코드를 확인 할 수 있다.  
기본적으로 **리눅스**에서만 동작하는 프레임 워크이다.  
본격적으로 설치해 보도록 하자.  


## Requirements

These requirements are for the computer running the core framework:

* Any Linux or MacOS
* Python 3.6.1+ (with Pip3)
* Google Chrome is our only supported browser
* Recommended hardware to run on is 8GB+ RAM and 2+ CPUs

이런 말이 있는데 솔직히 큰 상관은 없다.  
나는 윈도우를 사용하고 있기 때문에 vmware에서 CentOS를 설치 해 주었다.
그리고 이어서 파이썬도 설치해 주었다.


```Bash
git clone https://github.com/mitre/caldera.git --recursive --branch v2.9.0
```

원하는 디렉토리에서 해당 코드를 실행하면 자동으로 설치가 진행된다.
그리고 Caldera에서 필요한 모듈들을 다운받아 주기 위해 다음 코드를 실행하면 된다.

```Bash
pip3 install -r requirements.txt
```

굳이 꼭 pip3일 필요까지는 없지만 파이썬 요구 버전이 3.6.1 이상 인 것을 고려해 적당히 설치해 주면 된다.

오류 없이 설치를 마치면 이제 Caldera를 킬 수 있다.

```Bash
python server.py --insecure
```

해당 코드를 실행하면
![서버 실행](/img/1.PNG)
이런 로그 메세지와 함께 Caldera가 켜지게 된다.
그럼 이제 localhost:8888을 통해 접속을 하면 된다고 적혀 있다.
그런데 내가 여기서 깜박한 것은 여기서 말하는 **localhost**란, 해당 CentOS의 ip 주소를 말한다.   

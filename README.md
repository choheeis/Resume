# Resume

안녕하세요 🙇🏻‍♀️ 

안드로이드 개발자로 취업 준비를 하고 있는 __김초희__ 입니다.

현재는 __Kotlin__ 과 __Jetpack__, __Android Clean Architecture__ 에 관심을 가지고 공부하고 있습니다.

* Email : chchgml10@gmail.com
* [Github](https://github.com/choheeis)
* [Blog](https://choheeis.github.io/newblog/)

## Education

* 서울과학기술대학교 컴퓨터공학과 4학년 재학 예정(현재 휴학 중)
  * 2017.03 ~ ing

* 전주기전여자고등학교 졸업
  * 2014.03 ~ 2017.02
  
## Skills

* Programming Language
  * Kotlin
  * C++
  
* Framework/Library
  * Android Platform
  * Firebase Cloud Messaging(FCM)
  * Retrofit2
  
* Architecture/Design Pattern  
  * Android Clean Architecture

## Projects

### [습관빵](https://github.com/choheeis/6th-habitbread-android)

* __꾸준한 습관 관리 및 동기 부여 제공을 위해 '습관빵을 굽는 제빵사'를 모토로 브랜딩화 한 어플리케이션__

* IT 동아리 Prography 6기 활동 중 진행한 프로젝트

* 기간

    * 2020.04 ~ ing (리팩토링하며 계속 서비스 중)
    
* 역할

    * __Android Clean Architecture 적용__
        
        예전의 프로젝트는 기능 구현 코드를 onCreate() 메소드에 모두 넣어서 개발했었습니다.

        프로그라피 안드로이드 파트 세션 중 [Android Clean Architecture](https://choheeis.github.io/newblog//articles/2020-05/android-clean-architecture) 에 대해 알게 되었고, UI 기반 클래스와 기능 로직 분리의 필요성에 대해 깨닫게 되어 프로젝트에 적용하였습니다.

    * __FCM 알림 구현__

        습관을 달성을 체크해야 하는 요일 및 시간에 알림을 보내는 기능을 구현하기 위해 사용하였습니다.

        평소 Firebase를 사용해보고 싶었고, 습관빵 어플을 iOS 버전으로도 준비하고 있었기 때문에 서버에서 iOS와 Android의 알림을 통합적으로 관리하기 위해 FCM을 사용했습니다.

        [앱이 background 상태일 때와 foreground 상태일 때 FCM 구현 방법](https://choheeis.github.io/newblog//articles/2020-11/firebase-cloud-messaging)이 달랐는데 이를 간과하여 버그가 발생했었지만 후에 정상적으로 리팩토링 하였습니다.

    * __Coroutine을 이용해 비동기 통신 구현__

        Android Clean Architecture를 따르면서 비동기 통신을 구현하려다 보니 Repository 클래스에서 ViewModel 클래스로 데이터를 넘겨주는 부분에서 어려움을 겪었습니다.

        Retrofit2의 enqueue() 콜백 메소드를 사용해서 비동기적 통신을 구현하면 콜백 메소드 내에서 데이터 리턴을 할 수 없었습니다.

        구글링을 통해 Android Clean Architecture + 비동기 통신을 위해 Coroutine 라이브러리를 사용하는 방법을 알게되어 적용하였습니다.

        __리팩토링 필요한 부분__ : Coroutine에 대해 얕게 공부 후 적용했어서 runBlocking 함수를 사용했습니다. Main Thread에서 사용한 것은 아니라 [ANR](https://developer.android.com/topic/performance/vitals/anr?hl=ko#diagnosing_anrs)이 발생하지는 않았지만 Coroutine에 대해 더 공부하고 싶고, runBlocking 함수를 사용하지 않고 구현할 수 있는 방법을 고민하고 싶습니다.


    * __[달력 관련 외부 라이브러리](https://github.com/prolificinteractive/material-calendarview) 를 사용해 습관 달성 표시 구현__ 

        달력의 각 일자에 이미지를 표시하여 습관 달성 표시 기능을 구현했습니다.

        달력은 외부 라이브러리를 사용했는데 github 리드미에 각 일자에 이미지 표시하기에 관한 내용이 없었습니다. 라이브러리 모든 파일을 확인하여 결국 관련 함수를 찾아내 구현하였습니다.

* [Google Play Store 다운로드](https://play.google.com/store/apps/details?id=com.habitbread.main)

<br></br>

### [음성인식 키오스크](https://github.com/Naver-AI-Burning-Day/andriod_kiosk)

* __음성을 통해 주문할 수 있는 키오스크 어플리케이션__

* 2020 NAVER AI Burning Day 본선(해커톤)에 출전하여 진행한 프로젝트

* 기간

  * 2020.02 (2박 3일, 해커톤)
    
* 역할

    * __Android 앱 개발 90%를 맡아서 구현__

        3명의 팀원(Android 1명, 서버 1명, 서버 및 디자인 1명)으로 구성된 팀이였기 때문에 Android 앱 개발의 대부분을 혼자 개발했습니다.

    * __Naver Cloud Platform에서 제공하는 Clova API를 사용해 음성 인식 주문 기능 구현__
  
        Clova API 중 [CSR](https://www.ncloud.com/product/aiService/csr)과 [CPV](https://www.ncloud.com/product/aiService/cpv) 를 사용해 음성을 텍스트로 변환하고, 텍스트를 음성으로 변환하는 기능을 구현했습니다.

        Android Platform의 [MediaPlayer API](https://developer.android.com/guide/topics/media/mediaplayer?hl=ko) 를 사용해 Clova API로부터 받은 녹음 파일을 재생했습니다.
   
<br></br>

### [인턴즈](https://github.com/INTENRZ/Android_INTERNZ)

* __인턴 공고를 제공하고 인턴 경험을 공유할 수 있는 어플리케이션__

* IT 창업 동아리 SOPT 25기 활동 중 진행한 프로젝트

* 기간

  * 2019.12 ~ 2020.01
    
* 역할

    * __Bottom Navigation을 이용해 하단 탭 구현__

        Material Design의 존재를 알게 되었습니다.

        Material Design Component 중 하나인 [Bottom Navigation](https://material.io/components/bottom-navigation) 을 사용해 하단 탭을 구현했습니다.

    * __프로필 화면, 메인 홈 화면, 스토리 작성 화면 구현__

        디자이너와 협업하여 진행한 프로젝트이기에 디자이너가 요청한 디자인과 최대한 똑같이 구현하려 노력했습니다.

        디자이너와의 협업을 위해 [zeplin](https://zeplin.io/)을 사용했습니다.

        복잡한 디자인은 주로 ConstraintLayout을 사용해 구현했습니다.

    * __코틀린 확장 함수 적용__

        SOPT Android 세션 중 [확장 함수](https://choheeis.github.io/newblog//articles/2020-12/kotlin-extension-function) 에 대해 배우게 되었습니다.

        인턴즈 앱 개발시 Toast 띄우는 코드를 간결하게 하고, Retrofit2의 enqueue() 호출을 간결하게 하기 위해 [확장 함수를 적용](https://github.com/INTENRZ/Android_INTERNZ/tree/master/app/src/main/java/com/example/internz/common)했습니다.
        
<br></br>

### [스타트픽](https://github.com/choheeis/StartPick-Android)

* __서울시 사업 정보 제공 및 창업 구인/구직 어플리케이션__

* 2019 서울시 모바일 앱 공모전 출전을 위해 진행한 프로젝트

* 기간

  * 2019.08 ~ 2020.09
    
* 역할

    * __Retrofit2 라이브러리를 사용해 HTTP 통신 기능 구현__

        서버 개발자와 협업하여 진행한 프로젝트이기에 Retrofit2 라이브러리를 사용하여 HTTP 통신 기능을 구현했습니다.

        서버 개발자와 협업을 위해 [Postman](https://www.postman.com/)을 사용했습니다.

    * __Android 앱 개발 언어를 Kotlin으로 변경__

        기존에 Android 앱 개발 시 Java를 사용했었는데 이 프로젝트부터 Kotlin으로 변경하여 개발했습니다.

        사업 공고 정보 목록 화면, 필터 검색 화면, 공고 지원 글쓰기 화면 등을 구현하며 Kotlin에 익숙해지려 노력했습니다.
        
<br></br>

### [서울과학기술대학교 전화번호부 앱](https://github.com/choheeis/Seoultech_PhoneBook)

* __서울과학기술대학교 교내 부서 전화번호를 제공하는 어플리케이션__

* 모바일 앱 프로그래밍 수업에 참여하여 제출한 프로젝트

* 기간

  * 2019.06
    
* 역할

    * __RecyclerView를 사용해 교내 부서 목록 기능 구현__

        __리팩토링 할 부분__ : 교내 부서 이름과 전화번호를 배열에 저장하여 앱의 메모리 사용량이 커졌습니다. 안드로이드 로컬 데이터베이스에 저장하여 관리하는 방향으로 리팩토링할 예정입니다.

    * __전화 걸기 및 전화번호 복사 기능 구현__

## Activities

### [Prography 6기/6.5기](http://prography.org/)

* 기간 : 2020.04 ~ ing(9개월)
* 팀원 : 서버 개발자 2명, 안드로이드 개발자 2명, iOS 개발자 2명, 브랜딩 디자이너 1명
* 활동 : 안드로이드 파트 스터디 참여([트립닷컴 클론코딩](https://github.com/choheeis/prography_assignment_1), [Room 사용 스터디](https://github.com/choheeis/prography_assignment_2))
* 성과 : 구글 플레이 스토어에 배포한 [습관빵](https://play.google.com/store/apps/details?id=com.habitbread.main) 개발
* 아이디어 기획 및 디자인, 개발, 브랜딩까지 팀원 모두가 참여

### [NAVER AI Burning Day 해커톤](https://campaign.naver.com/aihackathon_ai_burning/)

* 기간 : 2020.02 (2박 3일)
* 팀원 : 서버 개발자 2명, 안드로이드 개발자 1명
* 성과 : 해커톤 본선 진출

### [SOPT 25기](http://sopt.org/wp/)

* 기간 : 2019.07 ~ 2020.01(7개월)
* 활동 : [안드로이드 파트 스터디 참여](https://github.com/choheeis/SOPT_25)
* 성과 : SOPT 내 경선 대상, [인턴즈](https://github.com/INTENRZ/Android_INTERNZ) 개발

### [Blog](https://choheeis.github.io/newblog//)

* 기간 : 2019.02 ~ ing(2년)
* 활동 : C / C++ / Algorithm / OS / 자료구조 / Conference / Books / Android / Kotlin / Database 등 공부한 내용 공유 및 정리
* 성과 : (2020.12.15 기준) 구글 총 노출 수 1480건, 클릭 수 147건 달성

## Prizes

* __대학생 IT 동아리 SOPT 내 경선 대상__
    * 수상년도 : 2020.01.18


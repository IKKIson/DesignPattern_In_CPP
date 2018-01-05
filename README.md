# DesignPattern_In_CPP
A software design pattern is a reusable solution to a reoccurring software design pattern

## Prologue
### 소프트웨어 개발?
원하는 목적을 이루기 위하여 기준이 되는 개념이나 철학, 패러다임을 바탕으로 특별한과정, 프로세스를 거쳐 소프트웨어적인 해결책, 솔루션을 만들어내는 것이라고도 애기한다.

### 소프트웨어 개발을 위한 패러다임의 관점은?
- 구조적 관점 – Structural View
    - 소프트웨어를 기능 위주로 기능 기준의 관점으로써 원하는 기능을 하향식으로 점진적으로 세분화, 구체화하여 솔루션을 만드는 것.
- 객체지향적 관점 – Object Oriented View
    - 소프트웨어를 데이터 위주로 데이터(객체) 관점으로써 구체적인 데이터들간의 상호 관계를 정의하여 원하는 목적을 달성하여 솔루션을 만들어내는 것.


    - 20180105 소프트웨어의 개발 개념


## Creational Patterns - 객체 생성을 위한 디자인패턴
- About
 소프트웨어 공학에서 Creational Pattern은 객체 생성 메커니즘을 다루는 디자인 패턴으로, 상황에 적합한 방식으로 객체를 생성하려한다. 객체 생성의 기본 형식은 설계 문제들를 야기하거나, 설계를 복잡하게 만든다. Creational Patterns은 어떻게든지 객체 생성을 제어함으로써 문제를 해결한다.

- Learn more
 생성 패턴은 객체 생성 시 인스턴스를 만드는 절차를 추상화한다. 생성 패턴들은 객체를 생성/합성하는 방법이나 객체의 표현 방법과 (소프트웨어) 시스템을 분리해주어 객체 생성 제어를 구현한다.

- 클래스 생성 패턴 - 인스턴스로 만들 클래스를 다양하게 만들기 위한 용도로 상속을 사용한다.
- 객체 생성 패턴 - 인스턴스화 작업을 다른 객체에게 떠넘긴다(의존성).
- 생성 패턴들
    -  Abstract Factory
    Creates an instance of several families of classes
    클래스의 여러 개의 패밀리의 인스턴스들을 생성한다.
    +Super – Sub : Inheritance

    - Builder
    Separates object construction from its representation
    객체 구성으로부터 표현과 분리한다.

    - Factory Method
    Creates an instance of several derived classes
    여러 파생 클래스의 인스턴스를 만든다.

    - Object Pool
    Avoid expensive acquisition and release of resources by recycling objects that are no longer in use
    더 이상 사용하지 않는 개체를 재활용하여 자원의 비싼 획득 및 해제를 방지한다.
    +It prevents and improves the overhead incurred in allocating and releasing  other resources including memory(memory pool).

    - Prototype
    A fully initialized instance to be copied or cloned
    복사 또는 복제 할 완전히 초기화된 인스턴스

    - Singleton
    A class of which only a single instance can exist
    하나의 인스턴스만 존재할 수 있는 클래스
    +Classes that must exist only programmatically





### Abstract Factory



## Structural Patterns - 구조 개선을 위한 디자인패턴
### Sample

## Behavioral Patterns - 행동 수행 개선을 위한 디자인패턴
### Sample

 

## 참고자료
### Book
- GoF의 디자인 패턴 (재사용성을 지니 객체지향 소프트웨어의 핵심 요소) [개정판]
    - 저자 : 에릭 감마 , 리처드 헬름, 랄프 존슨, 존 블리시디스 지음 | 김정아 옮김
    - 출판사 :  프로텍미디어 | 2015년 03월 26일
  <img src="https://github.com/IKKIson/DesignPattern_In_CPP/blob/master/GoF%EB%94%94%EC%9E%90%EC%9D%B8%ED%8C%A8%ED%84%B4_%ED%91%9C%EC%A7%80.jpg?raw=true" width="200" height="300" />
  

- GoF 디자인 패턴! 이렇게 활용한다: C++로 배우는 패턴의 이해와 활용
    - 저자 : 장세찬
    - 출판사 : 한빛미디어
    <img src="https://github.com/IKKIson/DesignPattern_In_CPP/blob/master/%EB%94%94%EC%9E%90%EC%9D%B8%ED%8C%A8%ED%84%B4!%EC%9D%B4%EB%A0%87%EA%B2%8C%ED%99%9C%EC%9A%A9%ED%95%9C%EB%8B%A4_%ED%91%9C%EC%A7%80.jpg?raw=true" width="200" height="300" />


### Blog&Search
[blog:코드, 패턴 그리고 소프트웨어](https://wikidocs.net/580)

[blog:소년코딩](http://boycoding.tistory.com/105)

[blog:VallistA](http://vallista.tistory.com/entry/1-Singleton-Pattern-in-C)



### WebSite
[Huston Design Pattern](http://vincehuston.org/dp/)

[SourceMaking](https://sourcemaking.com/design_patterns)

[wikipedia](https://en.wikipedia.org/wiki/Software_design_pattern)


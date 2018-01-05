# DesignPattern_In_CPP
A software design pattern is a reusable solution to a reoccurring software design pattern

## 01 Prologue
### 소프트웨어 개발?
원하는 목적을 이루기 위하여 기준이 되는 개념이나 철학, 패러다임을 바탕으로 특별한과정, 프로세스를 거쳐 소프트웨어적인 해결책, 솔루션을 만들어내는 것이라고도 애기한다.

### 소프트웨어 개발을 위한 패러다임의 관점은?
- 구조적 관점 – Structural View
    - 소프트웨어를 기능 위주로 기능 기준의 관점으로써 원하는 기능을 하향식으로 점진적으로 세분화, 구체화하여 솔루션을 만드는 것.
- 객체지향적 관점 – Object Oriented View
    - 소프트웨어를 데이터 위주로 데이터(객체) 관점으로써 구체적인 데이터들간의 상호 관계를 정의하여 원하는 목적을 달성하여 솔루션을 만들어내는 것.


    - 20180105 소프트웨어의 개발 개념

<hr/>
<hr/>

## 02 Creational Patterns - 객체 생성을 위한 디자인패턴
#### About
소프트웨어 공학에서 Creational Pattern은 객체 생성 메커니즘을 다루는 디자인 패턴으로, 상황에 적합한 방식으로 객체를 생성하려한다. 객체 생성의 기본 형식은 설계 문제들를 야기하거나, 설계를 복잡하게 만든다. Creational Patterns은 어떻게든지 객체 생성을 제어함으로써 문제를 해결한다.

#### Learn more
생성 패턴은 객체 생성 시 인스턴스를 만드는 절차를 추상화한다. 생성 패턴들은 객체를 생성/합성하는 방법이나 객체의 표현 방법과 (소프트웨어) 시스템을 분리해주어 객체 생성 제어를 구현한다.

- 클래스 생성 패턴 - 인스턴스로 만들 클래스를 다양하게 만들기 위한 용도로 상속을 사용한다.
- 객체 생성 패턴 - 인스턴스화 작업을 다른 객체에게 떠넘긴다(의존성).
- 생성 패턴들
    -  Abstract Factory
        + Creates an instance of several families of classes.
        + 클래스의 여러 개의 패밀리의 인스턴스들을 생성한다.
        + Super – Sub : Inheritance

    - Builder
        + Separates object construction from its representation.
        + 객체 구성으로부터 표현과 분리한다.

    - Factory Method
        + Creates an instance of several derived classes.
        + 여러 파생 클래스의 인스턴스를 만든다.
    
    - Object Pool
        + Avoid expensive acquisition and release of resources by recycling objects that are no longer in use.
        + 더 이상 사용하지 않는 개체를 재활용하여 자원의 비싼 획득 및 해제를 방지한다.
        + It prevents and improves the overhead incurred in allocating and releasing  other resources including memory(memory pool).
    
    - Prototype
        + A fully initialized instance to be copied or cloned.
        + 복사 또는 복제 할 완전히 초기화된 인스턴스.

    - Singleton
        + A class of which only a single instance can exist.
        + 하나의 인스턴스만 존재할 수 있는 클래스.
        + Classes that must exist only programmatically.
    
### Rules of Thumb
1. 때로는 창조적 인 패턴이 경쟁자이기도합니다. Prototype 또는 Abstract Factory가 수익성있게 사용될 수있는 경우가 있습니다. 추상 팩토리는 복제하고 제품 객체를 반환하는 프로토 타입 세트를 저장할 수도 있습니다. [GOF, p126], 빌더는 다른 패턴 중 하나를 사용하여 빌드 할 구성 요소를 구현할 수 있습니다.

2. 추상 팩토리, 빌더 및 프로토 타입은 구현시 싱글 톤을 사용할 수 있습니다. [GOF, pp 81,134]
추상 팩토리, 빌더 및 프로토 타입은 제품 객체 클래스를 알고 생성하는 책임이있는 팩토리 객체를 정의하고이를 시스템의 매개 변수로 만듭니다. Abstract Factory에는 여러 클래스의 객체를 생성하는 factory 객체가 있습니다. Builder는 복잡한 프로토콜을 사용하여 점진적으로 복잡한 제품을 구축하는 팩토리 객체를 가지고 있습니다. Prototype에는 프로토 타입 객체를 복사하여 제품을 만드는 factory 객체 (프로토 타입이라고도 함)가 있습니다. [GOF, p135]

3. Abstract Factory 클래스는 종종 Factory Methods로 구현되지만 Prototype을 사용하여 구현할 수도 있습니다. [GOF, p95]

4. Abstract Factory는 플랫폼 별 클래스를 숨기기위한 Facade의 대안으로 사용할 수 있습니다. [GOF, p193]

5. 빌더는 복잡한 객체를 단계별로 구성하는 데 중점을 둡니다. Abstract Factory는 제품 객체 제품군 (단순 또는 복합)을 강조합니다. Builder는 제품을 최종 단계로 반환하지만 Abstract Factory와 관련하여 제품은 즉시 반환됩니다. [GOF, p105]

6. 빌더는 알고리즘이 전략으로 창조하는 것입니다. [아이콘, p8-13]

7. 빌더는 종종 컴포지트를 만듭니다. [GOF, p106]

8. Factory Methods는 일반적으로 Template Methods 내에서 호출됩니다. [GOF, p116]

9. Factory Method : 상속을 통한 생성. 프로토 타입 : 위임을 통한 생성.
종종 디자이너는 Factory Method (덜 복잡하고보다 사용자 정의가 가능하며 하위 클래스가 확산 됨)를 사용하여 시작하고 디자이너가 더 많은 유연성을 필요로하는 곳에서 발견 할 때 Abstract Factory, Prototype 또는 Builder (보다 유연하고 복잡한)로 발전합니다. [GOF, p136]
11. 프로토 타입은 서브 클래 싱을 필요로하지 않지만 초기화 작업이 필요합니다. 팩토리 메소드는 하위 클래스 화가 필요하지만 초기화는 필요하지 않습니다. [GOF, p116]
12. Composite 및 Decorator 패턴을 많이 사용하는 디자인은 종종 Prototype에서도 도움이됩니다. [GOF, p126]

<hr/>

### Abstract Factory

<hr/>

### Builder

<hr/>

### Factory Method

<hr/>

### Object Pool

<hr/>

### Prototype

<hr/>

### Singleton

<hr/>
<hr/>

## 03 Structural Patterns - 구조 개선을 위한 디자인패턴
### Sample

## 04 Behavioral Patterns - 행동 수행 개선을 위한 디자인패턴
### Sample

<hr/>
<hr/>

## 05 참고자료
### Book
- GoF의 디자인 패턴 (재사용성을 지니 객체지향 소프트웨어의 핵심 요소) [개정판]
    - 저자 : 에릭 감마 , 리처드 헬름, 랄프 존슨, 존 블리시디스 지음 | 김정아 옮김
    - 출판사 :  프로텍미디어 | 2015년 03월 26일
  <img src="https://github.com/IKKIson/DesignPattern_In_CPP/blob/master/GoF%EB%94%94%EC%9E%90%EC%9D%B8%ED%8C%A8%ED%84%B4_%ED%91%9C%EC%A7%80.jpg?raw=true" width="200" height="300" />
  

- GoF 디자인 패턴! 이렇게 활용한다: C++로 배우는 패턴의 이해와 활용
    - 저자 : 장세찬
    - 출판사 : 한빛미디어
    <img src="https://github.com/IKKIson/DesignPattern_In_CPP/blob/master/%EB%94%94%EC%9E%90%EC%9D%B8%ED%8C%A8%ED%84%B4!%EC%9D%B4%EB%A0%87%EA%B2%8C%ED%99%9C%EC%9A%A9%ED%95%9C%EB%8B%A4_%ED%91%9C%EC%A7%80.jpg?raw=true" width="200" height="300" />

<hr/>

### Blog&Search

[blog:코드, 패턴 그리고 소프트웨어](https://wikidocs.net/580)

[blog:소년코딩](http://boycoding.tistory.com/105)

[blog:VallistA](http://vallista.tistory.com/entry/1-Singleton-Pattern-in-C)

<hr/>

### WebSite

[Huston Design Pattern](http://vincehuston.org/dp/)

[SourceMaking](https://sourcemaking.com/design_patterns)

[wikipedia](https://en.wikipedia.org/wiki/Software_design_pattern)

[TutorialsPoint](https://www.tutorialspoint.com/design_pattern/index.htm)

<hr/>

I would like to thank TutorialPoint, SourceMaking, Wikipedia, VinceHuston for providing me with resources to help me with my lack of study and for me to develop myself.
I want to study design patterns and use them freely and freely for those who need it.


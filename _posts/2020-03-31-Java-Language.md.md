---
layout: single
title:  "Java Language"
date:   2020-03-31 
categories: jekyll update
---

---

# JAVA LANGUAGE 변천사



### 1. JDK 1.0a

1994년 발표.

### 2. JDK 1.0a2

1995년 5월 23일 발표. 언어 자체가 정식으로 발표된 날이기도 하다.

### 3.JDK 1.0

1996년 1월 23일 발표. 발표 이전에 불렸던 이름은 Oak였으며, 안정화 작업을 거친 1.0.2 버전에서 Java로 이름이 바뀌었다.

### 4.JDK 1.1

1997년 2월 19일 발표. 이너 클래스, JavaBeans, RMI, 리플렉션, 유니코드 지원, 국제화(Internationalization) 등이 추가되었다.

### 5. J2SE 1.2

1998년 12월 8일 발표. 일반 지원은 2003년 11월에 종료되었다. 새로운 GUI, JIT, CORBA 등의 굵직한 기능이 추가되면서 2 부터 약칭을 J2SE(Java 2 Standard Edition) 로 표기하기 시작했으며, 이 표기는 5 까지 사용된다. strictfp, Swing GUI, JIT, Java Applet을 구동하는 웹 브라우저 플러그인, CORBA, Collections 등이 추가되었다. 1999년에 업데이트를 통해 HotSpot JVM이 첫 선을 보인다.

### 6. J2SE 1.3

2000년 3월 8일 발표. 일반 지원은 2006년 11월에 종료되었다. HotSpot JVM, JNDI, JPDA, JavaSound 등이 추가되었다. RMI가 CORBA를 지원하도록 변경되었다.

### 7. J2SE 1.4

2002년 2월 6일 발표. 일반 지원은 2008년 10월, 연장 지원은 2013년 2월에 종료되었다. assert, 정규표현식,IPv6, Non-Blocking IO, XML API, JCE, JSSE, JAAS, Java Web Start 등이 추가되었다.

### 8. J2SE 5

2004년 9월 30일 발표. 일반 지원은 2009년 9월, 연장 지원은 2015년 5월에 종료되었다. J2SE 5.0까지 Windows 9x와 Windows NT 4.0이 지원되었다. 이 때부터 버젼 중 앞의 1을 빼버리고 표기하기 시작했다. 그러나 내부적으로는 여전히 1.5, 1.6, 1.7 등으로 데이터가 들어있다. Generics, Annotation, Auto Boxing/Unboxing, Enumeration, 가변 길이 파라미터, Static Import, 새로운 Concurrency API 등이 추가되었다. Java는 표준 입력(stdin) 지원이 시원찮았는데, J2SE 5에 들어서 java.util.Scanner가 추가되면서 이전보다 편하게 표준 입력을 사용할 수 있게 되었다.

### 9. Java SE 6

2006년 12월 11일 발표. 일반 지원은 2013년 2월에 종료되었으며, 연장 지원은 2018년 12월에 종료되었다. 이 때부터 표기가 J2SE에서 Java SE로 바뀌었다. Scripting Language Support, JDBC 4.0, Java Compiler API, Pluggable Annotation 등이 추가되었다. 스크립팅 언어 지원과 함께 Rhino JavaScript 엔진이 기본으로 탑재되었다.

### 10. Java SE 7

2011년 7월 7일 발표. 일반 지원은 2015년 4월에 종료되었으며, 연장 지원은 2022년 7월에 종료될 예정이다. Dynamic Language 지원, switch문에서 String 사용, try문에서 자동 자원 관리, Diamond Operator <>, 이진수 리터럴, 숫자 리터럴에 _ 지원, 새로운 Concurrency API, 새로운 File NIO 라이브러리, Elliptic Curve Cryptography, Java2D를 위한 XRender, Upstream, Java Deployment Ruleset 등이 추가되었다.

### 11. Java SE 8

2014년 3월 18일 발표. 일반 지원은 2019년 1월에 종료되었고, 연장 지원은 2023년 9월에 종료될 예정이다. Lambda Expression, Rhino 대신 Nashorn JavaScript 엔진 탑재, Annotation on Java Types, Unsigned Integer 계산, Repeating Annotation, 새로운 날짜와 시간 API(사실상 JodaTime이라고 보면 된다), Static Link JNI Library, Interface Default Method, PermGen 영역 삭제, Stream API 등이 추가되었다. 본래 일반 지원은 2017년 9월 종료 예정이었으나 Java 9 발표의 지연 때문에 2018년 9월로 연장되었다가, 이후 라이선스 이관 문제로 인해 2019년 1월로 다시 연장되었다.

32비트를 지원하는 마지막 공식 Java 버전으로, 이후 버전의 32비트 지원은 오직 서드파티를 통해서만 지원된다.

### 12. Java SE 9

2017년 9월 21일 발표. 일반 지원은 2018년 3월에 종료되었다.

Project Jigsaw 기반으로 런타임이 모듈화된 것이 가장 큰 특징. 이에 따라 대부분의 콘솔 프로그램 개발에는 더 이상 AWT나 Swing 같은 불필요한 라이브러리를 끌어쓸 필요도 없이, 최상위 모듈인 Base만 사용해도 된다. 더불어 특정 프로그램에 최적화된 최소 런타임을 제작할 수 있게 되면서 패키징 역시 간편해졌다.

여기에 Java를 인터프리터 언어 셸처럼 사용할 수 있는 JShell이 추가되었으며, Java 바이트코드를 기계어로 미리 번역하는 선행 컴파일(Ahead-Of-Time Compilation) 역시 실험 기능으로 추가되었다. 또한 Deprecated 표시에는 해당 버전과 제거 예정 여부를 표시할 수 있게 되었다. 그 외에 구조적 불변 컬렉션, 통합 로깅, HTTP/2, private 인터페이스 메소드, HTML5 Javadoc 등도 지원되며, 프로퍼티 파일에 UTF-8이 지원됨에 따라 더 이상 인코딩 문제로 삽질할 필요가 없어졌다. 또한 Java Applet기능은 지원이 종료된다.

새로 적용된 버저닝 정책에 따라 이 버전부터는 더 이상 1.x 버전으로 내놓지 않고, 대신 **9.0**으로 급속한 판올림이 일어났다. 또한 제거 예정인 Deprecated API는 **다음 버전인 Java SE 10부터 완전 삭제 예정**이므로 해당 API를 쓰는 프로그램은 더 이상 이후의 버전에서 컴파일조차 불가능하게 된다. 그리고 Java SE 9부터는 6개월마다 새로운 버전이 업데이트된다.

본래는 2016년 발표 예정이었으나 2번이나 연기되어 2017년 7월 27일 발표 예정, 그나마도 한번 더 연기되어 9월 21일에 발표되었다. 가장 큰 원인은 역시 Project Jigsaw의 개발 난이도였다. 런타임의 모듈화는 하위 호환성을 어느 정도 포기하고 성능을 추구한 것이기에 아직 현장에서는 Java 9로 넘어가는 것을 꺼리는 분위기다.

이 버전부터 64비트 버전만 출시되었으며, 32비트 버전은 더 이상 공식적으로 나오지 않는다.

### 13. Java SE 10

2018년 3월 20일 발표. 일반 지원은 2018년 9월에 종료되었다. var 키워드를 이용한 지역 변수 타입 추론, 병렬 처리 가비지 컬렉션, 개별 쓰레드로 분리된 Stop-The-World, 루트 CA 목록 등이 추가되었다. 또한 JDK의 레포지토리가 하나로 통합되었으며, JVM 힙 영역을 시스템 메모리가 아닌 다른 종류의 메모리에도 할당할 수 있게 되었다. 실험 기능으로 Java 기반의 JIT 컴파일러가 추가되었고, 이전 버전에서 Deprecated 처리된 API는 Java SE 10에서 모두 삭제되었다.

### 14. Java SE 11

2018년 9월 25일 발표. 일반 지원은 2023년 9월, 연장 지원은 2026년 9월에 종료될 예정이다.이클립스 재단으로 넘어간 Java EE가 JDK에서 삭제되고, JavaFX도 JDK에서 분리되어 별도의 모듈로 제공된다. 람다 파라미터에 대한 지역 변수 문법[[8\]](https://namu.wiki/w/Java#fn-8), 엡실론 가비지 컬렉터, HTTP 클라이언트 표준화 등의 기능이 추가되었다.

가장 커다란 변화는 바로 라이선스 부분. Java SE 11부터 Oracle JDK의 독점 기능이 오픈 소스 버전인 OpenJDK에 이식된다. 이는 다시 말해 Oracle JDK와 OpenJDK가 완전히 **동일**해진다는 뜻이다. Oracle JDK는 Java SE 11부터 LTS(장기 지원) 버전으로 3년마다 출시되는데, 출시 후 5년 동안 오라클의 기술 지원이 제공되고 최대 3년까지 지원 기간을 연장할 수 있다. Oracle JDK는 이제 3년에 한 번 출시되니 Java의 실질적인 버전 업을 담당하는 것은 OpenJDK가 된 셈이다. OpenJDK는 기업들을 위한 기술 지원은 없고, 새로운 버전이 나오면 이전 버전에 대한 마이너 업데이트와 보안 업데이트는 중단된다.

그리고 Java 11과 함께 발표된 또 다른 소식은 바로 **Oracle JDK가 구독형 유료 모델로 전환된다는 점**이다. 2019년 1월부터 오라클이 제공하는 모든 Oracle JDK는 유료화되며, 구독권을 구입하지 않으면 Oracle JDK에 접근 자체가 금지된다. 기존의 일반/연장 지원 서비스는 구독권에 포함되므로 별도의 서비스로는 제공되지 않는다. **개인 사용자는 2021년 1월부터 비용을 지불해야 한다.** 이 때문에 많은 기업들이 Oracle JDK에서 발을 빼고 있으며, OpenJDK를 기반으로 한 다른 서드파티 JDK가 대안으로 떠오르고 있다. 대표적인 예로 Azul Systems에서 개발한 Zulu JDK가 있는데, Zulu JDK는 오라클의 TCK(Technology Certification Kit) 인증을 받은 구현체이다. 개인과 기업 모두 무료로 사용할 수 있고, 기술 지원에 한해서만 유료 서비스가 제공된다. 또 다른 대안으로는 AdoptOpenJDK가 있는데, AdoptOpenJDK는 HotSpot VM 대신 Eclipse OpenJ9을 탑재한 버전도 같이 제공하고 있다. 다만 아직 TCK 인증을 받지 않았기에 주의가 필요하다.

### 15.Java SE 12

2019년 3월 19일 공개. 특징 중 하나로 문법적으로 Switch문을 확장한 것이 있다.

```
switch (day) {
    case MONDAY:
    case FRIDAY:
    case SUNDAY:
        System.out.println(6);
        break;
    case TUESDAY:
        System.out.println(7);
        break;
    case THURSDAY:
    case SATURDAY:
        System.out.println(8);
        break;
    case WEDNESDAY:
        System.out.println(9);
        break;
}
```


예전에는 이렇게 써야 했던 Switch문을 아래와 같은 형식으로도 쓸 수 있게 되었다.

```
switch (day) {
    case MONDAY, FRIDAY, SUNDAY -> System.out.println(6);
    case TUESDAY                -> System.out.println(7);
    case THURSDAY, SATURDAY     -> System.out.println(8);
    case WEDNESDAY              -> System.out.println(9);
}
```

이외에 가비지 컬렉터 개선, 마이크로 벤치마크 툴 추가, 성능 개선의 변경점이 있다.

### 16.Java SE 13

2019년 9월 17일 공개. java 12에서의 스위치 개선을 이어 yield 라는 예약어가 추가되었다.

```
var a = switch (day) {
    case MONDAY, FRIDAY, SUNDAY -> yield 6;
    case TUESDAY                -> yield 7;
    case THURSDAY, SATURDAY     -> yield 8;
    case WEDNESDAY              -> yield 9;
};
```

### 17.Java SE 14

2020년 3월 18일 공개하였으며, 이전 버전이 되는 JavaSE(Standard Edition)  13과 비교하여 1,986건의 버그 픽스를 실시하고 16개의 주요 기능을 강화 및 변경했다.

또한 instance of 연산자의 패턴 매칭을 통해 간결한 코드 설명을 가능하게 하는 'JEP 305: Pattern Matching for instance of(Preview)'와 자기 완결형 자바 어플리케이션을 패키지화 하는 JEP 343: Packaging Tool(Incubator), NUMA(Non-Uniform Memory Access), 시스템의 메모리 어로케이션 구현으로 G1 퍼포먼스를 향상시키는 JEP 345: NUMA-Aware Memory Allocation for G1 등이 더해졌다.

### 18. Java SE 15

2020년 9월 공개 예정.



*출처*

1.[인공지능신문](http://www.aitimes.kr/news/articleView.html?idxno=15716)

2.[나무위키](https://namu.wiki/w/Java)








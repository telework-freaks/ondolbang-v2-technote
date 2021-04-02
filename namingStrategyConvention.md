
# Naming Strategy  Convention

## 개요
개인 개발인 경우 어떤 이름을 쓰던 간에 본인이 단번에 이해를 할 수 있기 때문에 이름 전략에 크게 중요성을 두지 않습니다. 허나 단체 프로젝트 및 협업을 하는 경우 적절한 이름 사용과 규칙을 정해 놓지 않는다면 이 객체가 어떤 기능을 하는지, 어떤 파일에서 참조 되는지 등 한눈에 파악하기가 어렵습니다.  Naming Strategy  Convention을 적절하게 세우면 코드의 시안성이 좋아질 뿐만 아니라, 정체성이 분명한 객체들끼리 모여서 자기 역할에 집중하며 서로 상호작용할때 제대로 된 OOP를 구현 할 수 있습니다.

## 이름 작명 규칙
프로젝트를 진행할때 레포지토리, 패키지, 클래스, 변수, 메소드등 이름을 정의하는 경우가 많습니다. 여러 표기법중 파스칼 표기법과 카멜 표기법 그리고 케밥 표기법 3가지를 사용하여 이름 작명 규칙을 정하고 추가로 고려해야할 규칙도 정의 했습니다. 하위 설명에 대한 첨부된 코드는 자바를 기반으로 작성 되었습니다.


### 자바 클래스 및 인터페이스, 리엑트 컴포넌트 
파스칼 표기법을 사용합니다.

    public class NamingStrategy{}
    @BookRepository


### 함수, 매개변수, 파일, 디렉토리
카멜 표기법을 사용합니다.
   
    private String findPerson(String companyName){}


### HTML ID 및 클래스, 레포지토리
케밥 표기법을 사용합니다.
   

    <div class="bar-under"></div>
    <div id="success-button"></div>
    ondolbang-v2

  
### 상수 선언
대문자 및 언더바(_)만 사용 가능합니다.
   
    public static final LIMIT_OCCUPY = 100;

    
### 단일 문자 사용
반복 문 사용시를 제외한 경우 철저히 금지합니다.
   
    // 허용
    for(int x = 0 ; x < nodeLength ; x++){}
    
    // 불가
    int a = 0;


### 어떠한 값을 얻거나 넘김
get, set을 접두어로 사용합니다.
   
    public String getCodeName(){}
    public void setCodeName(){}


### () 공백 사용 여부
for, if, switch등을 사용하는 경우 공백이 추가된다. 함수 사용시에는 공백사용이 불가능 합니다.
   
    //공백 허용
    for ()
    if ()
    switch ()
    //공백 불가
    public int count(){}

        
### 연산기호
기호 앞뒤로 공백이 추가됩니다.

    if (number == 5 && people.equals("KIM"))
    for (int i = 0 ; i < count  ; i++)

    
### 기타사항

삼항 연산자 사용을 금지합니다.

    boolean isStart = counter == 0 ? true : false;

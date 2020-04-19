---
layout: post
title: 코어자바스크립트 - 01. 데이터 할당
tags: [javascript, frontend, 코어 자바스크립트]
author: sol
---

현업에서 개발하며 사실 자바스크립트에 대해 체계적으로 공부해 본 적이 없는 것 같다. 개발을 하면서 그때 그때 구글과 동료들과 익힌 지식으로 돌아가는 코드만 짜왔고 

문제가 생기면 근본적인 원인을 찾기 보다는 이것 저것 바꿔보고 구글링하며 해결했다. 실질적인 원인보다는 단순히 "이렇게 하면 문제가 생기는구나"하고 배경지식 없는 경험만 쌓였다. 

그러다 보니 익숙하고 체계적으로 배운 백엔드와는 다르게 프론트엔드 개발을 할때에는 항상 뭔가 찝찝한 기분이 들었다.

 그래서 한번 차근차근 공부해보자 라는 생각으로 책 하나를 선정하여 읽기 시작했고 공부한 내용을 요약 겸 정리를 블로그에 써볼 생각이다.

 [코어 자바스크립트 (정재남 저)](http://www.yes24.com/Product/Goods/78586788) 도서를 참고하였습니다.
<br><br>  



# 01. 데이터 할당

#### 1-1. 변수 선언
 
예제 1-1
{% highlight js %}
var a;
{% endhighlight %}

위와 같이 변수 선언하는 방법은 기본적으로 알고 있겠지만, 방법이 아닌 동작 원리를 알아보고자 한다.

예제 1-1을 말로 풀어쓰면 "변할 수 있는 데이터를 만든다. 이 데이터의 식별자는 a로 한다" 가 된다.

결국 변수란 **변경 가능한 데이터가 담길 수 있는 공간 또는 그릇** 이라고 생각할 수 있다.<br><br>  
  
#### 1-2. 데이터 할당

예제 1-2
{% highlight js %}
var a;        //변수 a 선언
a = 'abc';    //변수 a에 데이터 할당

var a = 'abc' //변수 선언과 할당을 한 문장으로 표현
{% endhighlight %}
<br>

표 1-1<br>
{% include aligner.html images="20200419/table1.PNG" %}

예제 1-2를 표현하면 아래와 같다.
> 1. 변수 영역에서 빈 공간(@1003) 확보
> 2. 확보한 공간의 식별자를 a로 지정
> 3. 데이터 영역의 빈 공간(@5004)에 문자열 'abc'를 저장
> 4. 변수 영역에서는 a라는 식별자를 검색(@1003)
> 5. 앞서 저장한 문자열의 주소(@5004)를 @1003의 공간에 대입

<br><br>

예제 1-3
{% highlight js %}
var a = 10;
var b = 10;
{% endhighlight %}

예제 1-3의 경우에는 또 다른 변수 b를 더 선언했다. 그렇다면 b의 데이터 할당은 어떻게 될까?
여기서 중요한 것은 10이라는 값이 새로운 주소에 할당되고 b에 해당 주소가 대입되는 것이 아니라는 것이다.
b는 a의 10과 같은 주소를 참조하고 새로운 데이터 영역을 더 만들지 않는다.

결국 자바스크립트 엔진은 예제 1-3을 실행할때 다음과 같은 절차를 거친다.
> 1. 변수 영역에 빈 공간을 확보하여 식별자 a로 지정하고,
> 2. 데이터 영역에서 10이 있는지 검색한 후 10을 찾지 못했기 때문에 새로운 주소에 10을 저장하고,
> 3. a 식별자 주소에 10 데이터 주소를 대입한다.
> 4. 변수 영역에 빈 공간을 확보하여 식별자 b로 지정하고,
> 5. 데이터 영역에서 10이 있는지 검색한 후 10이 있는 것을 확인한 후,
> 6. 해당 데이터 주소를 b 식별자 주소에 대입한다.

그렇다면 object의 경우는 어떻게 데이터 할당이 이루어질까?
<br>

예제 1-4
{% highlight js %}
var obj1 = {
    a: 1,
    b: 'bbb'
};
{% endhighlight %}

표 1-2
{% include aligner.html images="20200419/table1-2.PNG" %}

> 1. 변수 영역의 빈 공간(@1003)을 확보하고, 그 주소의 이름을 obj1으로 지정
> 2. 임의의 데이터 저장공간(@5002)에 데이터를 저장하려고 보니 여러 개의 프로퍼티로 이루어진 데이터 그룹이다. 내부 프로퍼티들을 저장하기 위해 별도의 변수 영역을 마련하고, 그 영역의 주소(@7103~?)를 @5002에 저장
> 3. @7103과 @7104에 각각 a와 b라는 프로퍼티 이름 지정
> 4. 데이터 영역에서 숫자 1을 검색하고 결과가 없으므로 @5003에 저장하고 이 주소를 @7103에 저장
> 5. 문자열 'bbb' 역시 임의로 5004에 저장하고, 이 주소를 @7104에 저장


여기까지 문제없이 왔으면 전반적인 데이터 할당에 대한 내용은 이해한 것이다.
그러면 이제 자주 맞닥뜨리는 변수 복사 문제를 이해하고 해결할 수 있다.
<br><br>

### 1-3. 변수 복사 비교

예제 1-5
{% highlight js %}
var a = 10;
var b = a;

var obj1 = {c: 10, d: 'ddd'}
var obj2 = obj1;

b = 15;
obj2.c = 20;

console.log(a == b);
console.log(obj1 == obj2);
{% endhighlight %}

예제 1-5의 결과를 예측하면 어떨까?
이제는 속지 않는다. 결과부터 얘기하면 false, true이다.

이러한 결과가 왜 나오는지 아래 표를 보면서 분석해보자.

표 1-3
{% include aligner.html images="20200419/table1-3.PNG" %}

표 1-3과 같이 obj1과 obj2를 복사한 후 obj2.c의 값을 변경했을때, c의 주소만 @5001 => @5005로 변경된 것을 볼 수 있다.<br> 
obj1은 여전히 @5002를 참조하고 @5002는 c에 해당하는 @7103을 참조하고 있기 때문에 obj2.c = 20으로 인해 변경된 @7103을 똑같이 참조하여 변경된 c값을 들고 있는 것이다.<br><br>
이러한 변수 복사 원리 때문에 개발자는 이 점을 숙지하고 필요에 따라 얕은 복사(shallow copy)와 깊은 복사(deep copy)를 자유로이 활용할 수 있어야한다.
<br>
아래 깊은 복사 예제 몇가지를 소개하고 마치도록 하겠다.

예제 1-6
{% highlight js %}
// 재귀를 이용하여 모든 프로퍼티를 순회하여 복사하는 방법
var copyObjectDeep = function (target) {
    var result = {};
    if (typeof target === 'object' && target !== null) {
        for (var prop in target) {
            result[prop] = copyObjectDeep(target[prop]);
        }
    } else {
        result = target;
    }
    return result;
}

var obj = {
    a: 1,
    b: {
        c: null,
        d: [1, 2]
    }
};
var obj2 = copyObjectDeep(obj);
{% endhighlight %}

예제 1-7
{% highlight js %}
// json을 이용한 방법
var copyObjectViaJson = (target) => {
    return JSON.parse(JSON.stringify(target));
};

var obj = {
    a: 1,
    b: {
        c: null,
        d: [1,2],
        func1: () => console.log(3),
        func2: () => console.log(4)
    }
};

var obj2 = copyObjectViaJson(obj);

obj2.a = 3;
obj2.b.c = 4;
obj.b.d[1] = 3;

console.log(obj);
console.log(obj2);
{% endhighlight %}

이 외에 외부 라이브러리를 이용한 방법 등이 있음.


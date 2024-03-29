---
layout: post
title: 노이다 Workshop
description: 이번 옴니채널 프로젝트에 관련된 모든 회사의 개발자들이 노이다로 모이게 되었다.
tags: 
    - business trip
    - Omni Channel
    - India
    - Noida
    - 글로벌 로직
author: sol
image: /assets/img/20200505/globallogic.jpg
optimized_image: /assets/img/20200505/opt_globallogic.jpg
category: business trip
---

이번 옴니채널 프로젝트는 phase1, phase2, phase3로 나뉘어 릴리즈가 계획되었다. phase1은 기존 인터페이스 그대로 연계를 Hybris에서 글로벌 플랫폼으로 전환하는 것이 목표였다. phase1은 5월 말 릴리즈가 예정이었는데 3월 중순이 다 되도록 글로벌 플랫폼에서는 연락이 없었고, 그들이 알아서 다 맞춰주겠다던 호언장담은 결국 무너져 버렸다. 프로젝트의 고객은 결국 글로벌 플랫폼, 우리 회사, 프로젝트 PM(Accenture)에게 워크샵을 요청했고 마침 인도 개발자들도 많고 우리도 인도 회사 글로벌로직에 phase2 부터 외주를 맡기기로 했기 때문에 노이다에서 집결하게 되었다. 

### 나는 누구 여긴 어디..?

#### 워크샵과 Knowledge Transfer의 병행

인도 출장 멤버는 사업팀 2명, 그리고 개발리더 1명, 단말(안드로이드) 개발자 1명, 서버 개발자 1명까지 총 5명이었고 16일의 출장 일정이었다. 델리 공항에 내리자마자 나는 인도 그 특유의 냄새는 정말이지 기분이 나빴다. 이때부터 불길한 예감이 들었던 듯하다. 우리의 할일은 phase2부터 함께 진행할 외주 개발자들에게 우리 솔루션의 Knowledge Transfer(KT)를 진행하고 프로젝트 전체 PM, 글로벌 플랫폼 개발자와 인터페이스 Workshop을 진행하는 것이었다.

도착하고 다음날 글로벌로직으로 출근했다. 입구에 들어서자마자 꽃을 목에 걸어주고 입구에 썸네일 사진처럼 우리 멤버 한명 한명의 이름을 써넣어 엄청난 환영을 해주었다. 얘네 특유의 환영 문화인 것 같았는데 나름 대접을 받는 것 같아 기분은 나쁘지 않았다. 적당히 서로 소개를 하고 바로 KT를 시작했다. 오전에는 KT, 오후에는 Workshop으로 일정이 잡혔다. 부족한 영어 실력으로 처음부터 하나하나 설명을 했다. 글로벌로직 개발자들은 언제나 고개를 가로저으며(인도에선 가로젓는게 알겠다는 뜻이다. 고개를 가로저을때마다 이상하게 기분이 나빴다.) "No problem"이었다. 다 알겠다는 거다. 그때 이 친구들을 믿지 말았어야 했다.

그리고 오후에는 Workshop을 진행했다. 에스더라는 네덜란드 친구가 프로젝트 PM이었다. Accenture에서 일하는 친구였는데 나름 똑똑하고 합리적이었다. 그리고 싸이(Sai)라는 친구가 글로벌 플랫폼 대표로 왔다. 입사한지 6개월 밖에 되지 않은 23살의 파릇파릇한 신입이었다. 해볼만 하겠다!! 속으로 쾌재를 불렀다. 나도 그렇고 그 친구도 그렇고 병아리였기에 뭔가 이상하게 이길 수 있겠다(??)라는 느낌이 들었다. 총 8개의 API가 있었고 글로벌 플랫폼 쪽에서 완료된 것은 단 하나 auth API 뿐이었다. 

#### 너만 바라볼거야...

출국 전부터 단말 개발자 선배가 항상 하던 말이 있었다. 

"Sol아, 거기가면 애들이 다 너만 바라볼꺼야. 다 너한테 물어볼거거든. 우리 주문 로직이 어떻게 되어있고 어떤 정책을 가지고 있는지, 니가 통달하고 있어야 돼."

너만 바라볼꺼라는 말, 그때 당시에는 와닿지 않았다. 개발자는 코드로 얘기하니까 코드보면서 하나 하나 천천히 보면 될 것이라고 생각했다. 노이다를 가보니 정말 모두들 나만 바라봤다. KT에서는 정책이 어떻게 되는지 단말 개발자들, 서버 개발자들, 사업팀 분들 할 것 없이 모두 나에게 물어봤다. 워크샵에서는 사업팀 분들, 에스더, 싸이가 현재 API spec은 어떻고 우리 주문 정책은 어떻게 되는지, 이런 기능이 개발 가능한지 불가능한지 등 2시간 인수인계 받은 나로써는 정말이지 벅찼던 것 같다. KT때는 코드 한줄 한줄 따라가니 그나마 나았다. 하지만 워크샵은 달랐다. 일단 Order 쪽의 모든 정책을 내가 알고 있지 못했고, 사실 글로벌 플랫폼 쪽에서도 말도 안되는 요구를 했기 때문이다.

#### 다 해주기로 했잖아!!!

워크샵 첫날, 사업팀 형은 시작부터 글로벌 플랫폼 쪽에 클레임을 했다. 왜 완료된 것이 auth API 밖에 없는지, 안되었으면 왜 미리 얘기하지 않은 것인지 따졌다. 아마도 사업팀 형은 일이 잘못되었을 때 글로벌 플랫폼 쪽에 책임을 묻고 우리 쪽을 방어하기 위해 따졌던 것 같다. 사실 글로벌 플랫폼은 이전부터 우리에게 API spec 문서를 달라고 요청했었다. 우리는 그때마다 우리 쪽에는 없고 Hybris 쪽에 있다라고 답변을 했고 에스더가 Hybris와 연계할때 참여했던 유일한 사람이었기 때문에 에스더에게 리다이렉트 했었다. 에스더는 Confluence url을 글로벌 플랫폼 쪽에 던졌지만 부족했었나보다. 그도 그럴 것이 API 명세서를 보아도 우리 쪽 로직을 모르니 이해가 안되는 부분이 있었을 것이다. 그리고 글로벌 플랫폼에서 요구했다. 많은 필드들 중에서 필요한 것만 추려달라. 그리고 그 필드가 무엇을 의미하고 뭘 위해서 필요한지 설명해달라. 사업팀 형은 반발했다. 왜 우리가 그렇게까지 해줘야하냐고, 그런 계약은 한 적이 없다고... 에스더 또한 그 말에 동의했다. 하지만 설명은 해줘야한다고 했다. 일은 되게 해야하니까...

나는 아찔했다. 겁이 났다. 워크샵 일정동안 잘해낼 수 있을까? 그리고 억울했다. 아니 알아서 다 해준다고 했는데 왜 이제와서 난리지? 그리고 왜 이제야 이런 자리를 만든거지? 그리고 나는 고작 2시간 밖에 인수인계를 받지 않았는데?? 그러나 모든 직장인을 알 것이다. 회사 일에서 개인의 억울함은 전혀 고려되지 않는다는 것. 그냥 개인적으로 안타깝다고 동정해줄 수는 있지만 일을 거스르진 못한다는 것...

#### 잠시만요... 찾아볼게요...

사업팀 형은 나를 걱정해주었다. 아니, 내 도메인 지식을 걱정했다. 하지만 어쩌랴... 이미 엎질러진 물이었다. 그렇게 싸이의 엄청난 질문 공세가 시작되었다. 'isReadyForFulfilment' 필드는 뭐냐, 명세서에 이런 value들이 있던데 각각 실제로 어떤 의미가 있는 것이냐와 같은 질문들을 쏟아내었다. 나는 그때마다 코드를 분석해야했다. 물론 이전에도 코드를 분석했었고 큰 흐름은 알고 있었다. 그러나 이렇게 세부적인 로직들에 대해서는 코드를 봐야 알 수 있었다. 게다가 싸이 영어는 진짜 미치도록 알아듣기 힘들었다. 외국 유학을 다녀온 사업팀 형 또한 제발 천천히 말해달라고 할 정도였다. 매일 Workshop 시간마다 나는 진짜 영혼이 가출한 상태로 있었다. 다 원망스러웠다. 사업팀 형은 내가 대답할때마다 계속 "확실해? 너 확실하게 얘기해야된다."라며 나를 압박했고 싸이는 미친 디테일한 질문들로 나를 압박했다. 나는 매 질문마다 이 대답만했다. "잠시만요... 찾아볼게요...". 

#### 입장의 차이

이 워크샵에는 4명의 멤버가 있었다. 우리 사업팀 형, 나, PM 에스더, 글로벌 플랫폼 개발자 싸이.<br>
사업팀 형은 나를 잘 구슬려야했다. 이미 일은 이렇게까지 되었지만 계약은 되어있고 고객의 압박도 있고, 어쨌든 프로젝트는 무사히 마쳐야 하기 때문이다. 싸이는 API 스펙을 완벽하게 숙지하고 우리 솔루션의 프로세스를 완벽하게 이해해해야했다. 그래야 돌아가서 다른 동료 개발자들에게 설명을 할 수 있기 때문이다. 에스더는 고객이 요청한 모든 기능들을 최대한 구현해야만 했다. 물론 그때 당시의 나는 이러한 입장들이 있는지 전혀 생각하진 못했다. 정신이 나가있었으니까... 지금와서 생각하는 그때 나의 입장은 단순했다. 빨리 끝내고 집에 가고 싶다.

워크샵은 치열했다. 일단 글로벌 플랫폼이나 우리나 본인들의 추가 개발 공수를 최소화하기 위해 논쟁했다. 에스더는 조율을 하지만 빠지는 기능이 없도록 지속적으로 압박했다. 그렇게 치열하게 논쟁했고 모든 API들에 대해서 정리가 되었다. 싸이가 컨플루언스에 하나하나 정리하였고 그에 따라 SIT 전까지 서로의 일들을 모두 완료하기로 하였다. phase1에 우리가 추가 개발할 일은 없을 줄 알았지만 개발해야될 건들이 꽤 많이 생겨버렸다. 아마도 내가 부족했던 탓이었던 것 같다. 지금 사업팀 형과 그때 얘기를 하면 어쩔 수 없었다고 하지만 객관적으로 당시의 나는 부족했다. 

#### Order 전문가로의 발돋움 

워크샵과 KT를 마치고 우리는 한국으로 돌아왔다. 한국에 돌아와서 정리해보았다. 내가 해야할 일들, 그리고 워크샵에서 내렸던 결론들에 대해서 다시 한번 복기하고 하나하나 확인했다.

안타까웠던 점은 우리에게 있을 줄 알았지만 실제로 개발되지 않았던 기능들이 몇가지 있었는데 나는 그러한 기능들 중 몇가지를 "이미 있다"고 대답해버렸다. 그리고 싸이에게 알려준 몇가지도 틀린 정보들이 있었다. 거기에 추가로 개발되어야 할 건들까지... 내 불안감 때문에 한건 한건 확인해서 다행이지 만약 추가 개발건에 대해서만 신경을 썼다면, SIT때 난리가 났을 듯 싶다. 어쨌든 내가 뱉었던 말에 책임을 져야 해서 싸이와 컨콜로 다시 정립하고 그에 맞게 다시 개발해야 하는 것들도 생겨버렸다.

노이다 워크샵을 통해 부족했던 인수인계 기간으로 인한 구멍난 도메인 지식을 풀로 채울 수 있었다. 그 이후부터 아마 오더에 관련된 모든 내용들을 숙지하고 새로운 기능에 대해 설계까지 할 수 있었던 것 같다. 워크샵 전까지 내가 왜 완벽하게 준비할 수 없었을까를 생각해보았다. 노력이 부족했던 탓일까? 그렇다고 하기에는 정말 열심히 코드 분석하고 문서 읽고 정책을 숙지했었다. 그렇다면 무엇이 부족했던걸까? 지금 생각해보면 시야였던 것 같다. 각자의 입장과 위치에 따른 역학관계, 글로벌 플랫폼의 약속 파기 등이 복합적으로 작용했던 것 같다. 사업팀 형은 무조건적으로 나를 옹호할 순 없었으며, 글로벌 플랫폼 또한 우리가 일해야 본인들이 편하다는 것을 알았고, PM은 글로벌 플랫폼의 약속 파기에도 불구하고 무사히 프로젝트를 완료하려면 우리의 정책이나 코드를 바꿔야한다는 데에 동의했다. 기존 Order 개발자 선배의 "니가 다 하게 될거야"라는 예언은 그냥 나온 것이 아니었다.

그렇다면 이런 시야를 넓힐 수 있었을까? 솔직히 잘 모르겠다. 경험이 중요하다는 얘기가 이 때문이 아닐까 싶다. 요즘에는 나도 모르게 개발자의 시선 외의 것들을 생각한다. 사업팀과 함께 다니며 현장에서 몸으로 체득한 덕에 나도 모르는 사이 시야가 넓어진게 아닌가 싶다.

치열했던 출장이 끝나고 한국으로 돌아와 나는 SIT 전까지 해야할 개발건들을 모두 개발 완료하고 SIT를 위해 독기를 품고 준비를 했다. 그리고 SIT는 시애틀에서 하는 것으로 결정되었다. 

---
layout: post
title: "OpenGL ES \"RenderTarget\""
date: 2013-04-24 01:07:50 +0900
---

최근 게임들은 렌더타겟에 장면을 렌더링한 후에, 후처리를 하고 그 결과를 최종적으로 화면에 출력하는 것이 일반화되어 있다.<div><br/></div><div>이 방식은 모바일에서도 잘 활용된다. <span style="font-size: 9pt;">오픈지엘에서는 현재 렌더링 할 렌더타겟을 설정할 때, glBindFramebuffer를 함수를 사용하게 되는데, 문제는 glBindFramebuffer를 불필요하게 호출을 하지 않는 것이 좋다는 것이다.</span></div><div><span style="font-size: 9pt;">(사실 엄밀히 말하면, glBindFramebuffer 함수 자체를 자주 호출하는 문제라기 보다, 렌더타겟 교체를 하지 않는 편이 좋다는 것이다.)</span></div><div><span style="font-size: 9pt;"><br/></span></div><div>따라서, 이전 렌더타겟의 버퍼 ID와 비교해서 변경되었을 때에만 glBindFramebuffer를 처리하도록 하면 된다. 하지만, 여기서 주의해야 할 점은 렌더타겟이 아닌 <b>최종 백버퍼(프레임버퍼)에 렌더링할 때에는 반드시 백버퍼의 초기 버퍼 ID로 돌려줘야 한다는 점</b>이다. (일반적으로 0으로 초기화 되어 있다)</div><div><span style="font-size: 9pt;"><br/></span></div><div><span style="font-size: 9pt;">당연한 이야기 같지만, 의외로 실수하기 쉬운 문제이기 때문에, 화면에 아무것도 찍히지 않는다고 좌절하기 쉽다. ㅎㅎ </span><span style="font-size: 9pt;">(내가 그랬지.. ㅜㅜ;;) </span></div><div><span style="font-size: 9pt;"><br/></span></div><div>그래도, 아직은 렌더타겟을 많이 사용하기에는 보급된 기기들이 약간 부족한 점이 있기 때문에, 최대한 절약해서 사용하는 편이 좋다. (하지만, 나는 마구 마구 사용하고 있다지?! 에헹~ ㅎㅎ)</div>
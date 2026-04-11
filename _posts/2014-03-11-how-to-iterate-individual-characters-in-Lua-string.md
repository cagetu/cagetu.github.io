---
layout: post
title: "how to iterate individual characters in Lua string?"
date: 2014-03-11 01:50:10 +0900
---

나는 당연히 <div><br/></div><div>string = "abcd"</div><div>for i=1, string:len() do</div><div>     print(string[i])</div><div>end</div><div><br/></div><div>이게 될 줄 알았는데, 안된더라.. 이것 때문에 한 시간 개 삽질.. ㅡㅡ;;</div><div><br/></div><div>꾸역 꾸역 이것 저것 해보면서 string.sub(string, i, i) 이렇게 처리해 놓고, "되기는 하지만, 설마 이건 아닐꺼야?" 라고 생각했는데, 진짜 이렇게 하는거네??<br/></div><div><br/></div><div><a href="http://stackoverflow.com/questions/829063/how-to-iterate-individual-characters-in-lua-string" target="_blank">http://stackoverflow.com/questions/829063/how-to-iterate-individual-characters-in-lua-string</a></div><div><br/></div><div>이런 젝일!!! 루아 멋쟁이!!! ㅠㅠ</div>
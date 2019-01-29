# Regular Expression Tips

전처리를 위한 정규표현식 사용 예제

좋은 참고 사이트 : [https://www.regextester.com/](https://www.regextester.com/)

사용된 데이터 : [여성중앙21, 전자파일](https://ithub.korean.go.kr/user/total/database/corpusView.do)\(3BB00D03.txt\)

## html parser

```python
text
```

```text
<!DOCTYPE tei.2 SYSTEM "c:\sgml\dtd\tei2.dtd" [
	<!ENTITY % TEI.corpus "INCLUDE">
	<!ENTITY % TEI.extensions.ent SYSTEM "sejong1.ent">
	<!ENTITY % TEI.extensions.dtd SYSTEM "sejong1.dtd">
]>

<tei.2>
<teiHeader>
	<fileDesc>
		<titleStmt>
			<title>여성중앙21, 전자파일</title>
			<author>중앙M&amp;B</author>
			<sponsor>대한민국 문화관광부</sponsor>
			<respStmt>
				<resp>표준화, 헤더붙임</resp>
				<name>고려대학교 민족문화연구원</name>
			</respStmt>
	.......
	
<head>제목 - 《발굴스토리》국내 최장신 농구선수 김주성의 꿈과 눈물</head>
<head>"정상인 부모도 흉내 못낼 큰 사랑으로 키워주신 우리 부모님이 자랑스럽습니다"</head>
<p>서장훈에 비견되는 대학농구 최고의 센터 중앙대 농구선수 김주성. 2m 5cm로 대학농구의 최장신 센터인 그는 소아마비인 아버지 김덕환씨(51세)와 곱사등이인 어머니 이영순씨(42세) 사이에서 어렵게 자랐다. 제대로 먹지도 못하고 자랐지만 마음만큼은 늘 풍족했던 그와 부모의 힘겹게 살아온 이야기.</p>
<p>▴지난 여름 휴가 때, 온 가족이 다 놀러갔다가 어머니와 한 컷. 이상하게 아버지와 찍은 사진은 별로 없다. 역시 어머니가 아버지보다는 만만한가보다.(?)</p>
<p>지난 1월 27일, 코맥스배 2000 농구대잔치 결승 2차전이 열리고 있는 장충체육관. 중앙대와 연세대의 경기가 열띤 열기 속에 열리고 있다. 많지 않은 관중 속에 목이 터져라 응원하고 있는 중년 부부가 유난히 눈에 띈다.</p>
.......
```

```python
re.findall("(<p>|<head>)(.*?)(<\/p>|<\/head>)", text)
```

```text
[('<head>', 'Ⅰ', '</head>'), ('<head>', '1. 먼동이', '</head>'), 
('<p>', '우리 나라 그리스도교는 세계에 다시 없는 뛰어난 자랑거리 몇 가지를 지니고 있다.', '</p>'), 
('<p>', '그 특색의 하나는, 선교사가 들어와서 전도하기 전에 우리 조상들은 학문(서학―그리스도교회 교리)으로서 먼저 연구하였고, 선교사가 오기 전에 우리가 외국에 나가서 이 교를 받아들여 왔다는 점이다. 이것은 세계 어느 나라 역사에도 없는 우리만의 자랑으로 되어 있다.', '</p>')
,....]
```




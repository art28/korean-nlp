---
description: SQuAD의 한국어 버전
---

# KorQuAD

{% embed url="https://korquad.github.io/" caption="다운로드 링크" %}

{% code-tabs %}
{% code-tabs-item title="load\_json.py" %}
```python
import json

kquad = json.load(open("KorQuAD_v1.0_dev.json", "r")) # dev set
kqaud
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="output" %}
```text
{'data': [{'paragraphs': [{'context': '1989년 2월 15일 여의도 농민 폭력 시위를 주도한 혐
의(폭력행위등처벌에관한법률위반)으로 지명수배되었다. 1989년 3월 12일 서울지방검찰청 공안부는 임종석의 사전구속영장을 발부받았다. 같은 해 6월 30일 평양축전에 임수경을 대표로 파견하여 국가보안법위반 혐의가 추가되었다. 경찰은 12월 18일~20일 사이 서울 경희대학교에서 임종석이 성명 발표를 추진하고 있다는 첩보를 입수했고, 12월 18일 오전 7시 40분 경 가스총과 전자봉으로 무장한 특공조 및 대공과 직원 12명 등 22명의 사복 경찰을 승용차 8대에 나누어 경희대학교에 투입했다. 1989년 12월 18일 오전 8시 15분 경 서울청량리경찰서는 호위 학생 5명과 함께 경희대학교 학생회관 건물 계단을 내려오는 임종석을 발견, 검거해 구속을 집행했다. 임종석은 청량리경찰서에서 약 1시간 동안 조사를 받은 뒤 오전 9시 50분 경 서울 장안동의 서울지방경찰청 공안분실로 인계되었다.',
     'qas': [{'answers': [{'answer_start': 0, 'text': '1989년 2월 15일'}],
       'id': '6548850-0-0',
       'question': '임종석이 여의도 농민 폭력 시위를 주도한 혐의로 지명수배 된 날은?'},
      {'answers': [{'answer_start': 125, 'text': '임수경'}],
       'id': '6548850-0-1',
       'question': '1989년 6월 30일 평양축전에 대표로 파견 된 인물은?'},
      {'answers': [{'answer_start': 0, 'text': '1989년'}],
       'id': '6548853-0-0',
       'question': '임종석이 여의도 농민 폭력 시위를 주도한 혐의로 지명수배된 연도는?'},
    ...}
   
```
{% endcode-tabs-item %}
{% endcode-tabs %}


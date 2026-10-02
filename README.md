# ALPHA911 · 한·영 웹툰 댓글 텍스트 분석

한국어와 영어 웹툰 댓글을 수집하고, 전처리·워드클라우드·LDA 토픽 모델링으로 독자 반응을 탐색한 팀 프로젝트입니다. 같은 분석 단계에 여러 구현을 시도하고 결과를 비교하는 방식으로 진행했습니다.

## 역할 구분

파일 이름의 `_Moon`은 문영식, `_Kim`은 김예선, `_Jo`는 조인준, `_Choi`는 최희범의 작업을 나타냅니다. 문영식의 수집·한국어 전처리·토픽 모델링 실험과 팀 통합본을 함께 확인할 수 있습니다. `_Main` 파일은 팀의 통합 분석 흐름입니다.

## 분석 흐름

| 단계 | 통합 코드 |
| --- | --- |
| 댓글 수집 | [00_CommentCrawling_Main.ipynb](00_CommentCrawling_Main.ipynb) |
| 리뷰 정리·결측 처리 | [01_MakingAllReviewMVDrop_Main.ipynb](01_MakingAllReviewMVDrop_Main.ipynb) |
| 코퍼스 구성 | [02_MakingAlllReviewCorpus_Main.ipynb](02_MakingAlllReviewCorpus_Main.ipynb) |
| 전처리 | [03_preprocessing_Main.py](03_preprocessing_Main.py) |
| 워드클라우드 | [04_MakingWordCloud_Main.py](04_MakingWordCloud_Main.py) |
| 토픽 모델링 | [영어 LDA](05_MakingLDA_en_Main.ipynb), [한국어 LDA](05_MakingLDA_ko_Main.ipynb) |
| 전체 흐름 | [06_All_Main.ipynb](06_All_Main.ipynb) |

한국어 분석에서는 형태소 분석기와 전처리 방식에 따라 분석 입력이 달라지는 점을 비교했습니다. 결과는 댓글 집합의 주제와 단어 분포를 이해하기 위한 탐색 자료이며, 전체 독자의 의견이나 특정 현상의 원인을 입증하는 지표는 아닙니다.

## 실행과 자료

노트북별 로컬 데이터 경로를 수정하고 사용한 형태소 분석기·사전을 준비해야 합니다. 일부 한국어 도구에는 Java 또는 별도 설치 과정이 필요합니다. 통합된 의존성 잠금 파일은 없으므로 수집부터 일괄 실행하기보다 저장된 데이터와 각 단계의 입력·출력을 먼저 확인하는 편이 좋습니다.

발표 자료와 분석용 데이터는 [datas](datas)에 있습니다. 외부 사이트 데이터와 라이브러리에는 각각의 이용 조건이 적용됩니다.

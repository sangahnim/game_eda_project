# [**game_eda_project**](https://github.com/sangahnim/game_eda_project/blob/main/game_eda_project.ipynb)
1. **주제**: 다음 분기에 설계해야할 비디오게임에 대한 EDA Project
2. **데이터** : Kaggle의 Video Game Sales 바탕으로 변형된 csv file
> 데이터선정이유 및 문제정의
>  * 2020년 PC와 모바일 위주의 국내게임시장에서 국내콘솔게임매출액은 1조 925억원으로 57.3%가 넘는 급격한 성장률을 보였다고 문화체육관광부와 한국콘텐츠진흥원이 발간한 '2021 대한민국 게임백서'에 기록되어있다.
>  * 또한 2020년 국내게임산업 매출액은 전년대비 21.3%증가한 18조8천800억원으로 집계됐고, 게임 상장사들의 공시자료와 지난 10년간의 통계치와 전망치를 토대로 한국콘텐츠진흥원은 2022년 게임시장의 매출액이 20조원이라 예상하고 있다.
>  * 게임시장에서 가장 성장률이 높은 비디오게임의 지역별 선호하는 게임장르, 출고량이 높은 퍼블리셔에 대해 분석하여 어떤 비디오게임을 출시해야 기업매출향상에  도움이 될 지 의사결정을 하기 위한 도움이 되고자 한다.
>  * 기사참조(https://www.vop.co.kr/A00001605585.html)
>  * 기사참조(https://science.ytn.co.kr/program/program_view.php?s_mcd=0082&s_hcd=&key=202112201717236926)

3. **EDA, Data preprocessing** : 
>  1) 결측치제거 : 불필요한 'N/A'을 공란으로 만든 후, 해당내용 및 이 외의 결측치 포함된 행 제거
>  2) data type 변경 : Year 컬럼의 값들을 정수4자리로 변경
>  3) data 내용 정리 : 지역별 Sales 컬럼에 문자가 들어간 경우 삭제 후, Sales타입을 수치로 변경, Total_Sales 특성 생성, '-'->'_' 컬럼이름정리
4. **시각화**
>  1) 지역별, 게임 장르별 출고율 (북미,EU,일본,기타지역의 장르별 게임 출고량을 원그래프로 나타냄)
>>     -> 일본을 제외한 전 지역에서 Action, Shooter, Sports순으로 인기가 있고, 
>>     -> 일본은 Shooter장르 제외하고, Role-Playing을 선호하는 것을 보여줌.
>  2) 연도별 게임 장르의 출고량 시각화 (데이터의 Genre컬럼을 Year별로 구분하여 피봇테이테이블로 정리 후, 게임 장르별로 연간 출고량 변화를 선그래프로 나타냄)
>>      -> 액션과 스포츠는 2000년대 급성장을 하고, 플랫폼은 계속 꾸준히 인기있음을 확인.    
5. **출고량이 높은 게임에 대한 분석 및 시각화 프로세스**
>  1) 전체 출고량이 높은 게임에 대한 분석
>>     -> 출고량 상위 30개 중 대부분의 출고사는 닌텐도임을 확인.


6. **결론** : 
> 비디오게임 전체시장을 봤을 때, 출고량이 높은 상위 3개의 장르는 Action, Shooter, Sports로 일본시장이 목표가 아닌 이상 세 장르 중 하나를 택하여 개발하는 것이 필요하다.  
> 상위 30개 게임종류를 확인시 가장 많은 게임을 발매한 회사는 닌텐도이고, 다수의 히트작 제작경험, wii 등 안정적인 플랫폼을 보유하고 있는 회사도 닌텐도이다. 이에 비디오게임 개발 시, 닌텐도사와의 협업을 진행하는 것이 필요하다.  
> 2020년에 급격한 성장률을 보였기에 비디오게임에 대한 분석을 시작하였으나, 비디오게임은 코로나시국에 실내에서 즐기기 위한 산업으로 급성장했다고도 볼 수 있다. 
> 인간의 생활환경 변화에 따라 시장이 민감하게 변화했다고 볼 수 있기에, 비디오게임 개발 시, 앞으로의 생활패턴을 생각하여 개발에 신중할 필요가 있다 

![EDA_Project_수정 001](https://user-images.githubusercontent.com/86824895/181526181-11336cb3-1f82-402b-a6d5-7e197a786d6e.jpeg)
![EDA_Project_수정 002](https://user-images.githubusercontent.com/86824895/181526212-fc9fb713-2ff5-4620-8e0c-b3f28b0e562e.jpeg)
![EDA_Project_수정 003](https://user-images.githubusercontent.com/86824895/181526220-4e09df83-bca0-4d8e-88e7-bdda4dacdb45.jpeg)
![EDA_Project_수정 004](https://user-images.githubusercontent.com/86824895/181526233-dce9edaa-04dd-49df-b311-f9bf21672a8f.jpeg)
![EDA_Project_수정 005](https://user-images.githubusercontent.com/86824895/181526241-c775031c-c595-46f8-8f1c-66511dd61a51.jpeg)
![EDA_Project_수정 006](https://user-images.githubusercontent.com/86824895/181526246-8c44592b-d558-4a71-9109-c8ab12c52a30.jpeg)
![EDA_Project_수정 007](https://user-images.githubusercontent.com/86824895/181526255-8998a57a-51cd-4a87-81c1-2e1f25d133f3.jpeg)
![EDA_Project_수정 008](https://user-images.githubusercontent.com/86824895/181526265-6e6466d7-da8b-491a-8acf-1a45d2efd87a.jpeg)
![EDA_Project_수정 009](https://user-images.githubusercontent.com/86824895/181526274-4e9e0c07-11b3-4920-ab8d-0fdc9a0c46ec.jpeg)
![EDA_Project_수정 010](https://user-images.githubusercontent.com/86824895/181526285-49c7e4e9-f931-4b3c-ae4b-8b7999e4797f.jpeg)
![EDA_Project_수정 011](https://user-images.githubusercontent.com/86824895/181526305-337c2152-12ae-43d4-92d6-1ec63df52db3.jpeg)
![EDA_Project_수정 012](https://user-images.githubusercontent.com/86824895/181526315-f13a0d21-7173-4d81-9a84-16f43ce767ce.jpeg)
![EDA_Project_수정 013](https://user-images.githubusercontent.com/86824895/181526324-60923698-7613-4b55-89b8-05989c9a7f43.jpeg)
![EDA_Project_수정 014](https://user-images.githubusercontent.com/86824895/181526336-eca1883f-7219-4096-aa4e-58d7403c30e9.jpeg)



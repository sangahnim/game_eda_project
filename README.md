# [**game_eda_project**](https://github.com/sangahnim/game_eda_project/blob/main/game_eda_project.ipynb)
1. **주제**: 다음 분기에 설계해야할 비디오게임에 대한 EDA Project
2. **데이터** : Kaggle의 Video Game Sales 바탕으로 변형된 csv file
> 데이터선정이유 및 문제정의
>  * 2020년 PC와 모바일 위주의 국내게임시장에서 국내콘솔게임매출액은 1조 925억원으로 57.3%가 넘는 급격한 성장률을 보였다고 문화체육관광부와 한국콘텐츠진흥원이 발간한 '2021 대한민국 게임백서'에 기록되어있다.
>  * 또한 2020년 국내게임산업 매출액은 전년대비 21.3%증가한 18조8천800억원으로 집계됐고, 게임 상장사들의 공시자료와 지난 10년간의 통계치와 전망치를 토대로 한국콘텐츠진흥원은 2022년 게임시장의 매출액이 20조원이라 예상하고 있다.
>  * 게임시장에서 가장 성장률이 높은 비디오게임의 지역별 선호하는 게임장르, 출고량이 높은 퍼블리셔에 대해 분석하여 어떤 비디오게임을 출시해야 기업매출향상에  도움이 될 지 의사결정을 하기 위한 도움이 되고자 한다.
>  * 기사참조(https://www.vop.co.kr/A00001605585.html)
>  * 기사참조(https://science.ytn.co.kr/program/program_view.php?s_mcd=0082&s_hcd=&key=202112201717236926)
<img width="592" alt="스크린샷 2022-07-29 오후 2 57 02" src="https://user-images.githubusercontent.com/86824895/181692517-57425c95-914d-464d-b93c-3eea77e84fc8.png">


3. **EDA, Data preprocessing** : 
>  1) 결측치제거 : 불필요한 'N/A'을 공란으로 만든 후, 해당내용 및 이 외의 결측치 포함된 행 제거
>  2) data type 변경 : Year 컬럼의 값들을 정수4자리로 변경
>  3) data 내용 정리 : 지역별 Sales 컬럼에 문자가 들어간 경우 삭제 후, Sales타입을 수치로 변경, Total_Sales 특성 생성, '-'->'_' 컬럼이름정리
4. **시각화**
>  1) 지역별, 게임 장르별 출고율 (북미,EU,일본,기타지역의 장르별 게임 출고량을 원그래프로 나타냄)
<img width="940" alt="스크린샷 2022-07-28 오후 11 12 10" src="https://user-images.githubusercontent.com/86824895/181546062-d3b74591-5538-4947-ae4e-7efb7a0d4e00.png">

<img width="964" alt="스크린샷 2022-07-28 오후 11 12 16" src="https://user-images.githubusercontent.com/86824895/181546028-3af0b82f-f17c-4237-907e-292b20f6a715.png">

>>     -> 일본을 제외한 전 지역에서 Action, Shooter, Sports순으로 인기가 있고, 
>>     -> 일본은 Shooter장르 제외하고, Role-Playing을 선호하는 것을 보여줌.  
>  2) 연도별 게임 장르의 출고량 시각화 (데이터의 Genre컬럼을 Year별로 구분하여 피봇테이테이블로 정리 후, 게임 장르별로 연간 출고량 변화를 선그래프로 나타냄)  
<img width="820" alt="스크린샷 2022-07-28 오후 11 12 25" src="https://user-images.githubusercontent.com/86824895/181545958-5580bb07-8abd-47fa-97bf-62f092cb4fe7.png">


>>      -> 액션과 스포츠는 2000년대 급성장을 하고, 플랫폼은 계속 꾸준히 인기있음을 확인.    
>>      
5. **출고량이 높은 게임에 대한 분석 및 시각화 프로세스**
>  1) 전체 출고량이 높은 게임에 대한 분석
<img width="729" alt="스크린샷 2022-07-28 오후 11 12 35" src="https://user-images.githubusercontent.com/86824895/181545788-435cebc7-7d75-454c-9801-d5ebf6d64a23.png">
<img width="553" alt="스크린샷 2022-07-28 오후 11 12 41" src="https://user-images.githubusercontent.com/86824895/181545674-91a372eb-3608-4230-ac31-62032858ed33.png">

>>     -> 출고량 상위 30개 중 대부분의 출고사는 닌텐도임을 확인.


6. **결론** : 
> 비디오게임 전체시장을 봤을 때,  
>  출고량이 높은 상위 3개의 장르는 Action, Shooter, Sports로 일본시장이 목표가 아닌 이상 세 장르 중 하나를 택하여 개발하는 것이 필요하다.  
> 상위 30개 게임종류를 확인시 가장 많은 게임을 발매한 회사는 닌텐도이고, 다수의 히트작 제작경험, wii 등 안정적인 플랫폼을 보유하고 있는 회사또한 닌텐도이다. 이에 비디오게임 개발 시, 닌텐도사와의 협업을 진행하는 것이 필요하다.  
> 2020년에 급격한 성장률을 보였기에 비디오게임에 대한 분석을 시작하였으나, 비디오게임은 코로나시국에 실내에서 즐기기 위한 산업으로 급성장했다고도 볼 수 있다.   
> 인간의 생활환경 변화에 따라 시장이 민감하게 변화했다고 볼 수 있기에, 비디오게임 개발 시, 앞으로의 생활패턴을 생각하여 개발에 신중할 필요가 있다.  





![EDA_Project_수정 001](https://user-images.githubusercontent.com/86824895/181544596-116f62e8-31a3-4b9b-95dd-f75e639dc22b.jpeg)
![EDA_Project_수정 002](https://user-images.githubusercontent.com/86824895/181544681-9f57a361-eb14-4f85-a187-64f8d29124fd.jpeg)
![EDA_Project_수정 003](https://user-images.githubusercontent.com/86824895/181544713-80f3d577-1a2f-4233-8550-2ce3c2e42a34.jpeg)
![EDA_Project_수정 004](https://user-images.githubusercontent.com/86824895/181544761-cb2be4b5-a4e7-443d-9da0-3a63828bb7de.jpeg)
![EDA_Project_수정 005](https://user-images.githubusercontent.com/86824895/181544784-e4681069-d88e-4235-9664-3ed55361b0ce.jpeg)
![EDA_Project_수정 006](https://user-images.githubusercontent.com/86824895/181544800-d3536e86-6c5d-47ac-a678-01324bcc55d3.jpeg)
![EDA_Project_수정 007](https://user-images.githubusercontent.com/86824895/181544815-d7c98ac8-8ae3-445a-a29e-5300fcd3e79f.jpeg)
![EDA_Project_수정 008](https://user-images.githubusercontent.com/86824895/181544826-866e49ba-846e-4e0e-881e-d0860fc57f8e.jpeg)
![EDA_Project_수정 009](https://user-images.githubusercontent.com/86824895/181544838-2ea4fbc8-c555-4a16-9e1c-28925f3a2c02.jpeg)
![EDA_Project_수정 010](https://user-images.githubusercontent.com/86824895/181544849-16c525f5-c263-4e88-883c-bf83469ff437.jpeg)
![EDA_Project_수정 011](https://user-images.githubusercontent.com/86824895/181544865-cb025643-270d-4b97-94f8-77a886ff59e1.jpeg)
![EDA_Project_수정 012](https://user-images.githubusercontent.com/86824895/181544879-556d7378-7500-4098-998c-10c27c2df805.jpeg)
![EDA_Project_수정 013](https://user-images.githubusercontent.com/86824895/181545285-c4ff1878-0549-446a-b4f0-0e39283f4838.jpeg)
![EDA_Project_수정 014](https://user-images.githubusercontent.com/86824895/181545369-782f95e9-dbab-4837-b673-b62f14ee6414.jpeg)


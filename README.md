# 2021 도시문제 분석과제 
### 수원시 [스마트 버스정류장 우선 설치위치 선정](https://compas.lh.or.kr/subj/past/info?subjNo=SBJ_2102_002) 🚌 

✔️ **분석 과정**에 대해 자세하게 알고 싶으시다면, **[보고서](https://drive.google.com/file/d/1OspwQ6dWe7ulff-1m7Zm92LCkQLxjAkd/view?usp=sharing)** 를 참고해주세요! 

<p align="center"><img src="https://user-images.githubusercontent.com/43749571/115103609-364b2980-9f8e-11eb-8ec4-a8c99686afa4.jpg"></p>
<br>
                 
## 1. File Directory    

![data2](https://user-images.githubusercontent.com/43749571/115104206-dc4c6300-9f91-11eb-9fbb-8774b84d305a.jpg)


```shell
B3A1
├── 설명자료.txt
├── NanumBarunGothic.ttf   		   
│
├── 📂 data     
│   ├── GGD_RouteInfo_M.xls  		 # 경기도 버스 노선 순서 
│   ├── GGD_RouteStationInfo_M.xls  	 # 경기도 버스 노선 정보 
│   ├── suwon_weather.csv  		 # 수원시 일자별 기상 정보 
│   ├── suwon_paldal.csv 		 # 수원시 팔달구 실거래가 
│   ├── suwon_ksun.csv 			 # 수원시 권선구 실거래가 
│   ├── suwon_jangan.csv 		 # 수원시 장안구 실거래가 
│   ├── suwon_yt.csv 			 # 수원시 영통구 실거래가 
│   ├── road.shp.csv 			 # 수원시 실거래가 위경도 좌표 
│   ├── house.csv 			 # 수원시 실거래가 최종 데이터 
│   ├── store_info.xlsx 		 # 경기도 상권 데이터 
│   ├── link_filter.geojson 		 # 수원시 교통링크 필터링 데이터 (QGIS 결과물) 
│   ├── dustdf.pickle			 # 수원시 미세먼지 데이터 (에어코리아 크롤링)
│   └── microdustdf.pickle 		 # 수원시 초미세먼지 데이터 (에어코리아 크롤링)
│
├── 📂 busdata   
│   └── bus_filter_final.geojson 	 # 수원시 BIS&인도폭 버스정류장 필터링 데이터 (QGIS 결과물)
│
├── 📂 QGIS    
│   ├── bus_filter_final.qgz		 # 수원시 BIS&인도폭 버스정류장 필터링
│   └── link_filter_final.qgz 		 # 수원시 교통링크 필터링 
│
├── 1_DataPreprocessing.html     	 # 1_DataPreprocessing.ipynb 실행 결과 파일 
├── 2_SparsePCA_Clustering.html    	 # 2_SparsePCA_Clustering.ipynb 실행 결과 파일 
├── 3_PLS_Regression.html    		 # 3_PLS_Regression.ipynb 실행 결과 파일 
└── 4_Optimize_Targeting.html    	 # 4_Optimize_Targeting.ipynb 실행 결과 파일 
```

<br>

## 2. PROCESS  
![model2](https://user-images.githubusercontent.com/43749571/115104215-e40c0780-9f91-11eb-85e7-cbd9772af02a.jpg)

data, busdata 폴더 하에 데이터를 다운로드 받아주시고, 가장 상위 경로에서 ipynb 파일을 순서대로 실행해 주시기 바랍니다.  <br> 
최종 결과는 `/busdata/df_final.xlsx` 로 저장됩니다.   <br> 


1. **[Data Preprocessing](https://github.com/jbeen2/BUS/blob/main/1_DataPreprocessing.ipynb)** : 분석에 사용할 데이터를 전처리 하는 과정입니다.  <br>
2. **[Sparse PCA & Clustering](https://github.com/jbeen2/BUS/blob/main/2_SparsePCA_Clustering.ipynb)** : Sparse PCA 를 통해 데이터를 차원축소하고, Clustering 을 통해 구별 target 후보지를 선정하는 과정입니다. <br>
3. **[PLS Regression](https://github.com/jbeen2/BUS/blob/main/3_PLS_Regression.ipynb)** : 변수간의 상관관계를 고려한 PLS Regression 을 적합해, 스마트 지수를 생성하는 과정입니다. <br>
4. **[Optimize & Targeting](https://github.com/jbeen2/BUS/blob/main/4_Optimize_Targeting.ipynb)** : constraint를 부여하여 최적 스마트 버스정류장 설치위치를 찾고, 광고 타겟층을 선정하는 과정입니다.  

<br>


## 3. Members : Team B3A1  

<img src="https://user-images.githubusercontent.com/43749571/115105604-00607200-9f9b-11eb-9bc1-9b9a30d6e473.JPG" width="300">

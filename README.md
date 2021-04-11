# [LH] 수원시 스마트 버스정류장 우선 설치위치 선정

                 
## 1. File Directory    
```
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
data, busdata 폴더 하에 파일을 다운로드 받아주시고, 가장 상위 경로에서 ipynb 파일을 순서대로 실행해 주시기 바랍니다.  <br> 
최종 결과는 `/busdata/df_final.xlsx` 로 저장됩니다. 


1. `Data Preprocessing` : 1_DataPreprocessing.ipynb  <br>
2. `Sparse PCA & Clustering` : 2_SparsePCA_Clustering.ipynb <br>
3. `PLSR` : 3_PLS_Regression.ipynb <br>
4. `Location Selection` : 4_Optimize_Targeting.ipynb <br>

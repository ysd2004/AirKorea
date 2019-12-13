# Air Pollution and Weather Data by Si-Gun-Gu in South Korea (2001 - 2018)

This dataset includes the major air pollutants (PM10, NO2, SO, O3 and CO) and weather estimates by 2017 Si-Gun-Gu administrative boundaries in South Korea for year 2001 - 2008.

대한민국의 시군구별 대기오염 물질 (PM10, NO2, SO, O3, CO) 및 기상 데이터를 2017년 기준 시군구별로 추정한 2001년 - 2018년 데이타입니다.

## Author / Contributor / Developer / Maintainer

Seong Yun, Department of Agricultural Economics, Mississippi State University (seong.yun@msstate.edu)\
Seung Gyu Kim, Department of Agricultural Economics, Kyungpook National University (sgkimwin@knu.ac.kr)

윤성도, 농업경제학과, 미시시피주립대학교 (seong.yun@msstate.edu)\
김승규, 농업경제학과, 경북대학교 (sgkimwin@knu.ac.kr)

## Variables

This dataset includes the variables below.

이 데이타셋은 아래의 변수들을 포함하고 있습니다.

| NO | Variable   | Description (KOR)                                                | Description (ENG)                                                                                |
|:----:|:------------:|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 1  | SIG_CD     | 시군구코드                                                   | Si-Gun-Gu Code                                                                                   |
| 2  | SIG_ENG    | 영문 시군구명                                                | Si-Gun-Gu Name                                                                                   |
| 3  | year       | 연도                                                         | year                                                                                             |
| 4  |  COavg     | 연평균 일산화탄소 (CO) 농도 (ppm)                            | Yearly CO average (ppm)                                                                          |
| 5  | NO2avg     | 연평균 이산화질소( NO2) 농도 (ppm)                           | Yearly NO2 average (ppm)                                                                         |
| 6  | O3avg      | 연평균 오존 (O3) 농도 (ppm)                                  | Yearly O2 average (ppm)                                                                          |
| 7  | PM10avg    | 연평균  PM10 농도 (ug/m3)                                    | Yearly PM10 average (ug/m3)                                                                      |
| 8  | SO2avg     | 연평균 아황산가스 (SO2) 농도 (ppm)                           | Yearly SO2 average (ppm)                                                                         |
| 9  | PM10freq   | 한국기준 PM10 >  80 (나쁨, 매우나쁨)인   날수                | Day counts of PM10 > 80 (unhealthy and very unhealthy in the Korean   Standard)                  |
| 10 | PM10freqUS | 미국기준 PM10 >  154 (민감군 나쁨, 나쁨,   매우나쁨)인 날수  | Day counts of PM10 > 154 (S-groups unhealthy, unhealthy and very   unhealthy in the US Standard) |
| 11 | PM10xtrm   | 한국기준 PM10 >  150 (매우나쁨)인 날수                       | Day counts of PM10 > 150 (very unhealthy in Korean the Standard)                                 |
| 12 | PM10xtrmUS | 미국기준 PM10 >  354 (매우나쁨)인 날수                       | Day counts of PM10 > 354 (very unhealthy in the US Standard)                                     |
| 13 | PM10hrs    | 한국기준 PM10 > 80  (매우 나쁨) 노출시간                     | Length of hours with PM10 > 80 ( very unhealthy in the Korean   Standard)                        |
| 14 | avghrs     | 한국기준 PM10 > 80  (매우 나쁨) 일간 평균   노출시간         | Daily average exposure hours with PM10 > 80 ( very unhealthy in the   Korean Standard)           |
| 15 | tavg       | 연평균기온 (deg C)                                           | Yearly average temperature (deg C)                                                               |
| 16 | tmin       | 연평균 최저기온 (deg C)                                      | Yearly average minimum temperature (deg C)                                                       |
| 17 | tmax       | 연평균 최고기온 (deg C)                                      | Yearly average maximum temperature (deg C)                                                       |
| 18 | ppt        | 연강수량 (mm)                                                | Yearly total precipitation (mm)                                                                  |
| 19 | wmax       | 연평균 최대풍속 (m/s)                                        | Yearly average of the maximim wind speeds (m/s)                                                  |
| 20 | wmaxd      | 연평균 최대풍속 방향 (degree)                                | Yearly average of the maximim wind speed direction (degree)                                      |
| 21 | wavg       | 연평균 풍속 (m/s)                                            | Yearly average of the mean wind speed (m/s)                                                      |
| 22 | huminavg   | 연평균 상대습도 (%)                                          | Yearly average of the relative humidity (%)                                                      |
| 23 | sunsum     | 연간 일조시간 (hrs)                                          | Yearly total shunshine hours (hrs)                                                               |

## Raw Data Source

Last access @ November 25, 2019<br/>
Air pollution data: Final measurment data from **Air Korea** (https://www.airkorea.or.kr/web)<br/>
Weather data: site monitoring data from **KMA** Open Data Portal (https://data.kma.go.kr/cmmn/main.do)<br/> 
Si-Gun-Gu shapefiles: 2017 March version from **GIS Developer** (http://www.gisdeveloper.co.kr/?p=2332) 

최근 접속 @ 2019년 11월 25일<br/>
대기 오염 데이터: 에어 코리아 최종확정 측정자료 (https://www.airkorea.or.kr/web)<br/>
기상 데이터: 기상청 기상자료개방포털 기상관측 자료 (https://data.kma.go.kr/cmmn/main.do)<br/>
시군구 shapefiles: GIS Developer 2017년 3월 지도 (http://www.gisdeveloper.co.kr/?p=2332)

## Data Processing

**Air Pollution Data**

Using the hourly air pollution raw data, the ordinary kriging was applied for predicting hourly air pollution variables at each centroid of Si-Gun-Gu locations. The yearly variables defined in the table above were calculated from those hourly variables. Ulleung-Gun, Jeju-Si, and Seogwipo-Si adopted the average of their own monitoring sites.

시간별 대기오염 원자료를 이용하여, 각 시군구의 중심점 (centroid)의 시간별 데이타를 Ordinary Kriging 방법으로 추정하였습니다. 위 표에 정의된 연별 자료는 각 변수의 정의에 따라 시간별 추정치를 이용하여 계산하였습니다. 울릉군, 제주시, 서귀포시의 데이타는 해당 지역의 측정소 자료를 평균치 입니다.

**Weather Data**

Using the daily weather raw data, the nearest weather monitoring station data to the centroid was assigned to each Si-Gun-Gu. If the data is missing in the nearest station, the next closest monitoring data was selected. The yearly variables defined in the table above were calculated from those daily variables. Ulleung-Gun adopted its own station data only. 

일별 날씨 원자료를 이용하여, 각 시군구의 중심점 (centroid)에서 가장 가까운 측정소의 값을 사용하였습니다. 가장 가까운 측정값이 없는 경우에는 그 다음 가까운 측정소의 값을 사용하였습니다. 위 표에 정의된 연별 자료는 일별 자료를 이용하여 정의에 따라 계산되었습니다. 울릉군은 해당 지역의 측정소 자료 사용하였습니다.

**Warning and Note**

The estimation methods adopted in this data is one of the simplest approaches. The authors are NOT specialties in atmospheric sciences or relevant data sciences. This data could include unintended errors and unexpected outliers. Please consult with an experties if your usages require higher-level accuracy. Authors do NOT take any responsibilities for users' usages of this data.

이 자료의 추정방법은 해당 분야에서 사용되는 방법 중에서 가장 간단한 방법입니다. 이 자료의 저자들은 대기과학이나 관련 데이타 사이언스의 전문가들이 아닙니다. 본 자료는 의도하지 않은 오류나 예상치 못한 이상치를 가질 수 있습니다. 높은 수준의 정확도를 필요로 하는 경우에는 해당분야의 전문가와 상의하십시오. 이 자료의 저자들은 자료 사용자들의 자료 이용에 대한 어떠한 책임도 지지 않습니다.

The estimated hourly air pollution and daily weather data are available upon requests under the authors' permission.

저자들의 사용허가를 전제로, 시간별 대기오염 또는 일간 기상 데이타 추정치는 요청에 의해 사용 가능합니다. 


![repo-settings-image](https://user-images.githubusercontent.com/18093541/63130482-99e6ad80-bf88-11e9-99a1-d3cf1660b47e.png)

Under the **Repository Name** heading, type: `username.github.io`, where username is your username on GitHub. Then click **Rename**—and that’s it. When you’re done, click your repository name or browser’s back button to return to this page.

<img width="1039" alt="rename_screenshot" src="https://user-images.githubusercontent.com/18093541/63129466-956cc580-bf85-11e9-92d8-b028dd483fa5.png">

Once you click **Rename**, your website will automatically be published at: https://your-username.github.io/. The HTML file—called `index.html`—is rendered as the home page and you'll be making changes to this file in the next step.

Congratulations! You just launched your first GitHub Pages website. It's now live to share with the entire world

## Making your first edit

When you make any change to any file in your project, you’re making a **commit**. If you fix a typo, update a filename, or edit your code, you can add it to GitHub as a commit. Your commits represent your project’s entire history—and they’re all saved in your project’s repository.

With each commit, you have the opportunity to write a **commit message**, a short, meaningful comment describing the change you’re making to a file. So you always know exactly what changed, no matter when you return to a commit.

## Practice: Customize your first GitHub website by writing HTML code

Want to edit the site you just published? Let’s practice commits by introducing yourself in your `index.html` file. Don’t worry about getting it right the first time—you can always build on your introduction later.

Let’s start with this template:

```
<p>Hello World! I’m [username]. This is my website!</p>
```

To add your introduction, copy our template and click the edit pencil icon at the top right hand corner of the `index.html` file.

<img width="997" alt="edit-this-file" src="https://user-images.githubusercontent.com/18093541/63131820-0794d880-bf8d-11e9-8b3d-c096355e9389.png">


Delete this placeholder line:

```
<p>Welcome to your first GitHub Pages website!</p>
```

Then, paste the template to line 15 and fill in the blanks.

<img width="1032" alt="edit-githuboctocat-index" src="https://user-images.githubusercontent.com/18093541/63132339-c3a2d300-bf8e-11e9-8222-59c2702f6c42.png">

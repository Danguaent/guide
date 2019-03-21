node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t docker_test:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'jgit' -p 'Devops123' "
sh "docker tag docker_test:latest jgit/docker_test:latest"
sh "docker push jgit/docker_test:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}

.head(10)



import pandas as pd
import matplotlib.pyplot as plt
import pandas as pd
import matplotlib.pyplot as plt
df=pd.read_csv("C:\\Users\jwngugi\Desktop\Data Science\Complaints_filed_against_public_or_private_institutions_and_public_officers_since_2014.csv")
df=pd.read_csv("C:\\Users\jwngugi\Desktop\Data Science\Complaints_filed_against_public_or_private_institutions_and_public_officers_since_2014.csv")
df.sample(5)
df.info()
df.sample(5)
df.info()
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 8582 entries, 0 to 8581
Data columns (total 6 columns):
DATE_OPENED                     8551 non-null object
CATEGORY                        8573 non-null object
COUNTY/PLACE_OF_ORIGIN          8485 non-null object
NATURE_OF_COMPLAINT             8559 non-null object
PUBLIC_INSTITUTION_INVOLVED_    8566 non-null object
OBJECTID                        8582 non-null int64
dtypes: int64(1), object(5)
memory usage: 402.4+ KB

# df['CATEGORY'].replace('FEMAL E','FEMALE')
# df.groupby('CATEGORY').count()
# df[df['CATEGORY']=='FEMAL E'].count()
?
# df['CATEGORY'].replace('FEMAL E','FEMALE')
# df.groupby('CATEGORY').count()
# df[df['CATEGORY']=='FEMAL E'].count()
Cleaning dataframe
df.isnull().sum()
DATE_OPENED                     31
CATEGORY                         9
COUNTY/PLACE_OF_ORIGIN          97
NATURE_OF_COMPLAINT             23
PUBLIC_INSTITUTION_INVOLVED_    16
OBJECTID                         0
dtype: int64
#Replacing null values 
df['CATEGORY'].fillna('UNCLEAR', inplace=True)
df['DATE_OPENED'].fillna('1/1/2015', inplace=True)
df['COUNTY/PLACE_OF_ORIGIN'].fillna('KWALE', inplace=True)
df['NATURE_OF_COMPLAINT'].fillna('UNCLEAR', inplace=True)
df['PUBLIC_INSTITUTION_INVOLVED_'].fillna('UNCLEAR', inplace=True)
#rename column
df.rename(columns={'PUBLIC_INSTITUTION_INVOLVED_':'PUBLIC_INSTITUTION_INVOLVED'})
DATE_OPENED	CATEGORY	COUNTY/PLACE_OF_ORIGIN	NATURE_OF_COMPLAINT	PUBLIC_INSTITUTION_INVOLVED	OBJECTID
0	2/13/2015	MALE	MURANGA	UNCLEAR	YOUTH ENTERPRISE DEVT FUND	0
1	7/23/2014	FEMALE	NAIROBI	UNRESPONSIVENESS	YOUTH ENT DEVT FUND	1
2	1/25/2016	UNCLEAR	UNCLEAR	DELAY	WATER RESOURCE MANAGEMENT AUTHORITY	2
3	5/23/2016	MALE	NAIROBI	MALADMINISTRATION	WATER RESOURCE MANAGEMENT AUTHORITY	3
4	9/14/2016	MALE	BOMET	ADMINISTRATIVE INJUSTICE	WATER RESOURCE MANAGEMENT AUTHORITY	4
5	4/15/2015	MALE	NAIROBI	DELAY	WOMEN ENTERPRISE FUND	5
6	7/8/2016	FEMALE	NAIROBI	UNRESPONSIVE OFFICIAL CONDUCT	WOMEN ENTERPRIC EFUND	6
7	10/6/2016	FEMALE	KIRINYAGA	INACTION	WITTNESS PROTECTION AGENCY	7
8	1/14/2016	MALE	NAIROBI	MALADMINISTRATION	WITNESS PROTECTION PROGRAMME	8
9	2/16/2016	MALE	KIAMBU	INACTION	WITNESS PROTECTION AGENCY	9
10	11/16/2015	MALE	NAIROBI	UNRESPONSIVE OFFICIAL CONDUCT	WIBA	10
11	2/25/2016	UNCLEAR	NAIROBI	MALADMINISTRATION	WATER RESOURCE MANAGEMENT AUTHORITY	11
12	10/14/2015	MALE	NAIROBI	DELAY	WATER APPEAL BOARD	12
13	7/13/2015	UNCLEAR	UNCLEAR	MALADMINISTRATION	WATER SERVICES TRUST FUND	13
14	6/23/2015	MALE	NAIROBI	UNFAIR TREATMENT	VILLA FRANCA POLICE POST	14
15	6/4/2014	UNCLEAR	VIHIGA	CORRUPTION	VIHIGA COUNTY GOVERNOR	15
16	11/13/2014	UNCLEAR	UNCLEAR	UNCLEAR	VIHIGA COUNTY ASSEMBLY	16
17	2/5/2014	MALE	UNCLEAR	ADMINISTRATIVE INJUSTICE	VICTORY CHILDREN'S HOME FOUNDATION	17
18	5/25/2016	MALE	NYANDARUA	INJUSTICE	VETERINART AT KIPIPILI SUB COUNTY	18
19	7/25/2014	MALE	UNCLEAR	UNCLEAR	UNIVERSITY OF RWANDA	19
20	1/31/2014	FEMALE	KIAMBU	DELAY	UNIVERSITY OF NAIROBI	20
21	1/31/2014	FEMALE	KIAMBU	DELAY	UNIVERSITY OF NAIROBI	21
22	8/28/2014	MALE	HOMABAY	MALADMINISTRATION	UNIVERSITY OF NAIROBI	22
23	9/29/2014	FEMALE	UNCLEAR	MALADMINISTRATION	UNIVERSITY OF NAIROBI	23
24	9/17/2014	MALE	UNCLEAR	UNCLEAR	UNIVERSITY OF NAIROBI	24
25	9/24/2014	MALE	KAKAMEGA	UNFAIR TREATMENT	UNIVERSITY OF NAIROBI	25
26	2/17/2014	MALE	UNCLEAR	ABUSE OF POWER/UNFAIR TREATMENT	UNIVERSITY OF NAIROBI	26
27	11/11/2014	MALE	NAIROBI	UNFAIR TREATMENT	UNIVERSITY OF NAIROBI	27
28	1/31/2014	FEMALE	KIAMBU	DELAY	UNIVERSITY OF NAIROBI	28
29	1/31/2014	FEMALE	KIAMBU	DELAY	UNIVERSITY OF NAIROBI	29
...	...	...	...	...	...	...
8552	3/3/2015	MALE	UNCLEAR	UNRESPONSIVE OFFICIAL CONDUCT	AFRICAN CONSERVATION CENTER (ACC)	8552
8553	4/1/2015	MALE	UNCLEAR	DELAY	AFRICAN CONSERVATION CENTER (ACC)	8553
8554	4/10/2015	MALE	NAIROBI	DELAY	AFRICAN CONSERVATION CENTER (ACC)	8554
8555	4/14/2015	MALE	EMBU	UNFAIR TREATMENT	AFRICAN CONSERVATION CENTER (ACC)	8555
8556	5/22/2015	UNCLEAR	MURANGA	DELAY	AFRICAN CONSERVATION CENTER (ACC)	8556
8557	5/14/2015	MALE	KIRINYAGA	UNFAIR TREATMENT	AFRICAN CONSERVATION CENTER (ACC)	8557
8558	6/9/2015	MALE	KIMILILI	UNRESPONSIVE OFFICIAL CONDUCT	AFRICAN CONSERVATION CENTER (ACC)	8558
8559	8/7/2015	UNCLEAR	CHOGORIA	UNRESPONSIVE OFFICIAL CONDUCT	AFRICAN CONSERVATION CENTER (ACC)	8559
8560	9/9/2015	FEMALE	UNCLEAR	UNFAIR TREATMENT	AFRICAN CONSERVATION CENTER (ACC)	8560
8561	10/1/2015	MALE	KAJIADO	UNRESPONSIVE OFFICIAL CONDUCT	AFRICAN CONSERVATION CENTER (ACC)	8561
8562	12/21/2015	MALE	KIAMBU	UNRESPONSIVE OFFICIAL CONDUCT	AFRICAN CONSERVATION CENTER (ACC)	8562
8563	1/28/2016	MALE	NAIROBI	INEFFICIENCY	AFRICAN CONSERVATION CENTER (ACC)	8563
8564	9/24/2015	FEMALE	KWALE	UNRESPONSIVE OFFICIA L CONDUCT	ADVOCATES COMPLAINT COMMISSION	8564
8565	7/15/2014	FEMALE	SIAYA	DELAY	NATIONAL SOCIAL SECURITY FUND	8565
8566	3/19/2015	MALE	MOMBASA	MALADMINISTRATION	UNCLEAR	8566
8567	1/15/2015	MALE	MAKUENI	UNCLEAR	UNCLEAR	8567
8568	9/24/2015	MALE	N /A	UNRESPONSIVE CONDUCT	UNCLEAR	8568
8569	9/25/2015	FEMALE	KWALE	INACTION POLICE	UNCLEAR	8569
8570	9/29/2015	MALE	NAIROBI	INACTION	UNCLEAR	8570
8571	10/1/2015	MALE	SIAYA	UNFAIR TREATMENT	UNCLEAR	8571
8572	10/30/2015	UNCLEAR	NAIROBI	ABUSE OF POWER	UNCLEAR	8572
8573	3/31/2016	UNCLEAR	NAIROBI	UNCLEAR	UNCLEAR	8573
8574	5/27/2016	HUD/GPO	UNCLEAR	UNCLEAR	UNCLEAR	8574
8575	7/8/2016	UNCLEAR	KWALE	UNCLEAR	UNCLEAR	8575
8576	8/17/2016	MALE	UASIN GISHU	UNFAIR TREATMENT	UNCLEAR	8576
8577	9/27/2016	MALE	COUNTY GOVERNMENT OF TRANA ZOIA	COUNTY GOVERNMENT OF TRANS ZOIA	UNCLEAR	8577
8578	10/7/2016	UNCLEAR	KWALE	UNCLEAR	UNCLEAR	8578
8579	1/1/2015	UNCLEAR	KWALE	UNCLEAR	UNCLEAR	8579
8580	1/1/2015	UNCLEAR	KWALE	UNCLEAR	UNCLEAR	8580
8581	1/1/2015	UNCLEAR	KWALE	UNCLEAR	UNCLEAR	8581
8582 rows × 6 columns

df.isnull().sum()
DATE_OPENED                     0
CATEGORY                        0
COUNTY/PLACE_OF_ORIGIN          0
NATURE_OF_COMPLAINT             0
PUBLIC_INSTITUTION_INVOLVED_    0
OBJECTID                        0
dtype: int64
#Cleanup CATEGORY column
# df['CATEGORY'].str.replace('MAL E','MALE')
?
# df['CATEGORY'].replace('ORGAMISATION ','ORGANIZATION')
?
?
# df[df['CATEGORY']=='ORGAMISATION ']
# # df['CATEGORY'][316] = 'ORGANIZATION '
# # df[df['CATEGORY']=='ORGAMISATION ']
df['CATEGORY'].replace(to_replace=['ORGAMISATION ', 'ORGANIZATION ','ORGANISATION '], value='ORGANIZATION',inplace=True)
df['CATEGORY'].replace(to_replace=['MAL E', 'MALE ',' MALE','`MALE'], value='MALE',inplace=True)
df['CATEGORY'].replace(to_replace=['FAMALE', 'FAMALE ','FEMAL E','FEMALE '], value='FEMALE',inplace=True)
df['CATEGORY'].replace(to_replace=['UNCLAER', 'UNCLEA R','UNCLEAR ','UNLEAR '], value='UNCLEAR',inplace=True)
?
?
df.CATEGORY.value_counts().plot(kind = "bar")
<matplotlib.axes._subplots.AxesSubplot at 0x27b79c13b70>

import seaborn as sns
df.columns
Index(['DATE_OPENED', 'CATEGORY', 'COUNTY/PLACE_OF_ORIGIN',
       'NATURE_OF_COMPLAINT', 'PUBLIC_INSTITUTION_INVOLVED_', 'OBJECTID'],
      dtype='object')
data = df.groupby('PUBLIC_INSTITUTION_INVOLVED_').count()
?
data1= data.sort_values('CATEGORY', ascending=False).head(10)
sns.barplot(x= data1.index , y='NATURE_OF_COMPLAINT', data=data1)
plt.xticks(rotation=90)
plt.ylabel('Y')
plt.savefig("test.jpg")
?

cat_of_interest = ['MALE','FEMALE']
df_gender = df[df['CATEGORY'].isin(cat_of_interest)]
# df['CATEGORY'].sample(6)
df_gender.groupby(['CATEGORY']).count().plot.pie(y='OBJECTID')
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-4-1875be291dd4> in <module>
      1 cat_of_interest = ['MALE','FEMALE']
----> 2 df_gender = df[df['CATEGORY'].isin(cat_of_interest)]
      3 # df['CATEGORY'].sample(6)
      4 df_gender.groupby(['CATEGORY']).count().plot.pie(y='OBJECTID')

NameError: name 'df' is not defined

top_five = df_gender.groupby(['NATURE_OF_COMPLAINT']).count().sort_values('OBJECTID', ascending=False).head(5)
df_gender
# df_gender['DATE_OPENED'] = pd.to_datetime(df_gender['DATE_OPENED'])
# # df_gender['DATE_OPENED'].dt.month_name()
# df_gender.dtypes
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-3-90dd489edc5c> in <module>
----> 1 top_five = df_gender.groupby(['NATURE_OF_COMPLAINT']).count().sort_values('OBJECTID', ascending=False).head(5)
      2 df_gender
      3 # df_gender['DATE_OPENED'] = pd.to_datetime(df_gender['DATE_OPENED'])
      4 # # df_gender['DATE_OPENED'].dt.month_name()
      5 # df_gender.dtypes

NameError: name 'df_gender' is not defined

df.dtypes
DATE_OPENED                     object
CATEGORY                        object
COUNTY/PLACE_OF_ORIGIN          object
NATURE_OF_COMPLAINT             object
PUBLIC_INSTITUTION_INVOLVED_    object
OBJECTID                         int64
dtype: object

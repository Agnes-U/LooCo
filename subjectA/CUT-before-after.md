

## 2



### 2-Cut1 

```
2-Cut1-before
django-elasticsearch-dsl-drf
| +-django-elasticsearch-dsl(version range:>=0.3, <=0.4.4)
| | +-elasticsearch-dsl(version range:>=2.0.0,<6.0.0)
| +-elasticsearch-dsl(version range:*)
```



```
2-Cut1-after
django-elasticsearch-dsl-drf
| +-django-elasticsearch-dsl(version range:>=0.3, <=0.4.4)
| | +-elasticsearch-dsl(version range:>=2.0.0,<6.0.0)
| +-elasticsearch-dsl(version range:*)
```





### 2-Cut2 

```
2-Cut2-before
django-elasticsearch-dsl-drf
| +-django-elasticsearch-dsl(version range:>=0.4.5, <=0.5.1, !=0.5.0)
| | +-elasticsearch-dsl(version range:>=2.1.0,<6.0.0)
| +-elasticsearch-dsl(version range:*)
```



```
2-Cut2-after
django-elasticsearch-dsl-drf
| +-django-elasticsearch-dsl(version range:>=0.4.5, <=0.5.1, !=0.5.0)
| | +-elasticsearch-dsl(version range:>=2.1.0,<6.0.0)
| +-elasticsearch-dsl(version range:*)
```



### 2-Cut3 

```
2-Cut3-before
django-elasticsearch-dsl-drf
| +-django-elasticsearch-dsl(version range:==0.5.0)
| | +-elasticsearch-dsl(version range:>=2.1.0,<7.0.0)
| +-elasticsearch-dsl(version range:*)
```



```
2-Cut3-after
django-elasticsearch-dsl-drf
| +-django-elasticsearch-dsl(version range:==0.5.0)
| | +-elasticsearch-dsl(version range:>=2.1.0,<7.0.0)
| +-elasticsearch-dsl(version range:*)
```



### (issue) 2-Cut4 

```
2-Cut4-before
django-elasticsearch-dsl-drf
| +-django-elasticsearch-dsl(version range:>=6.4.0,<7.0.0)
| | +-elasticsearch-dsl(version range:>=6.4.0,<7.0.0)
| +-elasticsearch-dsl(version range:*)
```



```
2-Cut4-after
django-elasticsearch-dsl-drf
| +-django-elasticsearch-dsl(version range:>=6.4.0,<7.0.0)
| | +-elasticsearch-dsl(version range:>=6.4.0,<7.0.0)
| +-elasticsearch-dsl(version range:*)
```





### 2-Cut5 

```
2-Cut5-before
django-elasticsearch-dsl-drf
| +-django-elasticsearch-dsl(version range:>=7.0.0,<=7.1.4)
| | +-elasticsearch-dsl(version range:>=7.0.0,<8.0.0)
| +-elasticsearch-dsl(version range:*)
```



```
2-Cut5-after
django-elasticsearch-dsl-drf
| +-django-elasticsearch-dsl(version range:>=7.0.0,<=7.1.4)
| | +-elasticsearch-dsl(version range:>=7.0.0,<8.0.0)
| +-elasticsearch-dsl(version range:*)
```



### 2-Cut6 

```
2-Cut6-before
django-elasticsearch-dsl-drf
| +-django-elasticsearch-dsl(version range:>=7.2.0,<=7.2.2)
| | +-elasticsearch-dsl(version range:>=7.2.0,<8.0.0)
| +-elasticsearch-dsl(version range:*)
```



```
2-Cut6-after
django-elasticsearch-dsl-drf
| +-django-elasticsearch-dsl(version range:>=7.2.0,<=7.2.2)
| | +-elasticsearch-dsl(version range:>=7.2.0,<8.0.0)
| +-elasticsearch-dsl(version range:*)
```







## 3



### (issue) 3-Cut1 

```
3-Cut1-before
aucome
| +-docopt<version range:*>
| +-padmet<version range:>=2.6.8,<=4.0>
| | +- docopt<version range:==0.6.2>
```



```
3-Cut1-after
aucome
| +-docopt<version range:*>
| +-padmet<version range:>=2.6.8,<=4.0>
| | +- docopt<version range:>=0.6.1, <=0.6.2>
```





### 3-Cut2 

```
3-Cut2-before
aucome
| +-docopt<version range:*>
| +-padmet<version range:==5.0.1>
| | +- docopt<version range:>=0.6.2>
```



```
3-Cut2-after
aucome
| +-docopt<version range:*>
| +-padmet<version range:==5.0.1>
| | +- docopt<version range:>=0.6.1>
```





### 3-Cut3 

```
3-Cut3-before
aucome
| +-docopt<version range:*>
| +-padmet<version range:>=2.5.0,<=2.6.7>
| | +- docopt<version range:*> 
```



```
3-Cut3-after
aucome
| +-docopt<version range:*>
| +-padmet<version range:>=2.5.0,<=2.6.7>
| | +- docopt<version range:*>
```







## 5

### (issue) 5-Cut1 

```
5-Cut1-before
kindred
| +-bioc<version range:==1.2.3>
| | +-lxml<version range:==4.2.1>
| +-lxml<version range: *>
```



```
5-Cut1-after
kindred
| +-bioc<version range:==1.2.3> 
| | +-lxml<version range:>=4.0.0, <=4.3.5> 
| +-no call to lxml, the dependency can be removed
```



## 7



### (issue) 7-Cut1 

```
7-Cut1-before
crypto-whale-watching-app
| +-requests(version range:==2.21.0)
| | +-urllib3(version range:>=1.21.1,<1.25)
| +-urllib3(version range:>=1.24.2)
```



```
7-Cut1-after
crypto-whale-watching-app
| +- no call to requests, the dependency can be removed
| +- no call to urllib3, the dependency can be removed
```





## 8



```
8-Cut0
orcasong
| +-km3pipe<version range:>=0.0.1,<=0.1.1>
| | +- no dependency on numpy
| +-numpy<version range:*>
```



### (issue) 8-Cut1 

```
8-Cut1-before
orcasong
| +-km3pipe<version range:>=8.18.1,<=8.20.0>
| | +- numpy<version range:==1.16.2>
| +-numpy<version range:*>
```



```
8-Cut1-after
orcasong
| +-km3pipe<version range:>=8.18.1,<=8.20.0>
| | +- numpy<version range:>=1.16.1,<=1.16.2>
| +-numpy<version range:*>
```



### 8-Cut2 

```
8-Cut2-before
orcasong
| +-km3pipe<version range:(>=6.4,<=7.14)U(>=8.0,<=8.18.0)>
| | +- numpy<version range:>=1.12>
| +-numpy<version range:*>
```



```
8-Cut2-after
orcasong
| +-km3pipe<version range:(>=6.4,<=7.14)U(>=8.0,<=8.18.0)>
| | +- numpy<version range:>=1.12>
| +-numpy<version range:*>
```





### 8-Cut3 

```
8-Cut3-before
orcasong
| +-km3pipe<version range:>=8.27.5,<=8.27.12>
| | +- numpy<version range:==1.16.6>
| +-numpy<version range:*>
```



```
8-Cut3-after
orcasong
| +-km3pipe<version range:>=8.27.5,<=8.27.12>
| | +- numpy<version range:==1.16.6>
| +-numpy<version range:*>
```





### 8-Cut4 

```
8-Cut4-before
orcasong
| +-km3pipe<version range:(>=0.1.3, <=6.1.1)U(>=7.14.1,<=7.18.2)>
| | +- numpy<version range: *>
| +-numpy<version range:*>
```



```
8-Cut4-after
orcasong
| +-km3pipe<version range:(>=0.1.3, <=6.1.1)U(>=7.14.1,<=7.18.2)>
| | +- numpy<version range: *>
| +-numpy<version range:*>
```



### 8-Cut5 

```
8-Cut5-before
orcasong
| +-km3pipe<version range:>=6.2,<=6.3>
| | +- numpy<version range: <=1.11>
| +-numpy<version range:*>
```



```
8-Cut5-after
orcasong
| +-km3pipe<version range:>=6.2,<=6.3>
| | +- numpy<version range: <=1.11>
| +-numpy<version range:*>
```





### 8-Cut6 

```
8-Cut6-before
orcasong
| +-km3pipe<version range:==0.0.0U(>=8.21.2,<=9.13.9)>
| | +- numpy<version range:>=1.17.0>
| +-numpy<version range:*>
```



```
8-Cut6-after
orcasong
| +-km3pipe<version range:==0.0.0U(>=8.21.2,<=9.13.9)>
| | +- numpy<version range:>=1.17.0>
| +-numpy<version range:*>
```







## 9





### (issue) 9-Cut1 

```
9-Cut1-before
pypmml-spark
| +-py4j<version range:*>
| +-pyspark<version range:>=2.4.0, <=2.4.8>
| | +- py4j<version range:==0.10.7>
```



```
9-Cut1-after
pypmml-spark
| +-py4j<version range:*>
| +-pyspark<version range:>=2.4.0, <=2.4.8>
| | +- py4j<version range:==0.10.7>
```



### 9-Cut2 

```
9-Cut2-before
pypmml-spark
| +-py4j<version range:*>
| +-pyspark<version range:>=3.0.0,<=3.1.3>
| | +- py4j<version range:==0.10.9>
```



```
9-Cut2-after
pypmml-spark
| +-py4j<version range:*>
| +-pyspark<version range:>=3.0.0,<=3.1.3>
| | +- py4j<version range:>=0.10.9,<=0.10.9.1>
```





### 9-Cut3 

```
9-Cut3-before
pypmml-spark
| +-py4j<version range:*>
| +-pyspark<version range:==3.2.0>
| | +- py4j<version range:==0.10.9.2>
```



```
9-Cut3-after
pypmml-spark
| +-py4j<version range:*>
| +-pyspark<version range:==3.2.0> 
| | +- py4j<version range:>=0.10.9.2, <=0.10.9.5> 
```





### 9-Cut4 

```
9-Cut4-before
pypmml-spark
| +-py4j<version range:*>
| +-pyspark<version range:==3.2.1>
| | +- py4j<version range:==0.10.9.3>
```



```
9-Cut4-after
pypmml-spark
| +-py4j<version range:*>
| +-pyspark<version range:==3.2.1> 
| | +- py4j<version range:>=0.10.9.2, <=0.10.9.5>
```



### 9-Cut5 

```
9-Cut5-before
pypmml-spark
| +-py4j<version range:*>
| +-pyspark<version range:>=3.2.2,<=3.3.1>
| | +- py4j<version range:==0.10.9.5>
```



```
9-Cut5-after
pypmml-spark
| +-py4j<version range:*>
| +-pyspark<version range:>=3.2.2,<=3.3.1>
| | +- py4j<version range:>=0.10.9.2, <=0.10.9.5>
```



## 10



### 10-Cut1 

```
10-Cut1-before
toolium
| +-appium-python-client<version range:>=0.24,<=0.28>
| | +- selenium<version range:>=2.47.0>
| +-selenium<version range:>=2.53.6>
```



```
10-Cut1-after
toolium
| +-appium-python-client<version range:>=0.24,<=0.28>
| | +- selenium<version range:>=2.47.0>
| +-selenium<version range:>=2.53.6>
```





### 10-Cut2 

```
10-Cut2-before
toolium
| +-appium-python-client<version range:>=0.29,<=0.43>
| | +- selenium<version range:>=3.14.1,<4>
| +-selenium<version range:>=2.53.6>
```



```
10-Cut2-after
toolium
| +-appium-python-client<version range:>=0.29,<=0.43>
| | +- selenium<version range:>=3.14.1,<4>
| +-selenium<version range:>=2.53.6>
```



### (issue) 10-Cut3 

```
10-Cut3-before
toolium
| +-appium-python-client<version range:>=0.44,<=1.3.0>
| | +- selenium<version range:>=3.14.1,< 4>
| +-selenium<version range:>=2.53.6>
```



```
10-Cut3-after
toolium
| +-appium-python-client<version range:>=0.44,<=1.3.0>
| | +- selenium<version range:>= 3.14.1,< 4>
| +-selenium<version range:>=2.53.6>
```



### 10-Cut4 

```
10-Cut4-before
toolium
| +-appium-python-client<version range:==2.0.0a0>
| | +- selenium<version range:== 4.0.0.a7>
| +-selenium<version range:>=2.53.6>
```



```
10-Cut4-after
toolium
| +-appium-python-client<version range:==2.0.0a0>
| | +- selenium<version range:== 4.0.0.a7>
| +-selenium<version range:>=2.53.6>
```



### 10-Cut5 

```
10-Cut5-before
toolium
| +-appium-python-client<version range:<=2.0.0b5,>=2.0.0b4>
| | +- selenium<version range:== 4.0.0.b4>
| +-selenium<version range:>=2.53.6>
```



```
10-Cut5-after
toolium
| +-appium-python-client<version range:<=2.0.0b5,>=2.0.0b4>
| | +- selenium<version range:== 4.0.0.b4>
| +-selenium<version range:>=2.53.6>
```

### 10-Cut6 

```
10-Cut6-before
toolium
| +-appium-python-client<version range:==2.0.0b3>
| | +- selenium<version range:== 4.0.0.b3>
| +-selenium<version range:>=2.53.6>
```



```
10-Cut6-after
toolium
| +-appium-python-client<version range:==2.0.0b3>
| | +- selenium<version range:== 4.0.0.b3>
| +-selenium<version range:>=2.53.6>
```

### 10-Cut7 

```
10-Cut7-before
toolium
| +-appium-python-client<version range:<=2.0.0b2, >=2.0.0b1>
| | +- selenium<version range:== 4.0.0.b2.post1>
| +-selenium<version range:>=2.53.6>
```



```
10-Cut7-after
toolium
| +-appium-python-client<version range:<=2.0.0b2, >=2.0.0b1>
| | +- selenium<version range:== 4.0.0.b2.post1>
| +-selenium<version range:>=2.53.6>
```

### 10-Cut8 

```
10-Cut8-before
toolium
| +-appium-python-client<version range:(>=2.0.0rc4,<=2.0.0) U ==2.1.4>
| | +- selenium<version range:~= 4.0.0>
| +-selenium<version range:>=2.53.6>
```



```
10-Cut8-after
toolium
| +-appium-python-client<version range:(>=2.0.0rc4,<=2.0.0) U ==2.1.4>
| | +- selenium<version range:~= 4.0.0>
| +-selenium<version range:>=2.53.6>
```

### 10-Cut9 

```
10-Cut9-before
toolium
| +-appium-python-client<version range:==2.0.0rc2>
| | +- selenium<version range:== 4.0.0rc2>
| +-selenium<version range:>=2.53.6>
```



```
10-Cut9-after
toolium
| +-appium-python-client<version range:==2.0.0rc2>
| | +- selenium<version range:== 4.0.0rc2>
| +-selenium<version range:>=2.53.6>
```

### 10-Cut10 

```
10-Cut10-before
toolium
| +-appium-python-client<version range:==2.0.0rc1>
| | +- selenium<version range:== 4.0.0.rc1>
| +-selenium<version range:>=2.53.6>
```



```
10-Cut10-after
toolium
| +-appium-python-client<version range:==2.0.0rc1>
| | +- selenium<version range:== 4.0.0.rc1>
| +-selenium<version range:>=2.53.6>
```

### 10-Cut11 

```
10-Cut11-before
toolium
| +-appium-python-client<version range:>=2.1.0,<=2.1.2>
| | +- selenium<version range:~= 4.0>
| +-selenium<version range:>=2.53.6>
```



```
10-Cut11-after
toolium
| +-appium-python-client<version range:>=2.1.0,<=2.1.2>
| | +- selenium<version range:~= 4.0>
| +-selenium<version range:>=2.53.6>
```



### 10-Cut12  

```
10-Cut12-before
toolium
| +-appium-python-client<version range:>=2.2.0,<=2.7.1>
| | +- selenium<version range:~= 4.1>
| +-selenium<version range:>=2.53.6>
```



```
10-Cut12-after
toolium
| +-appium-python-client<version range:>=2.2.0,<=2.7.1>
| | +- selenium<version range:~= 4.1>
| +-selenium<version range:>=2.53.6>
```





## 11

### 11-Cut1 



```
11-Cut1-before
WavesGatewayFramework-master
| +-base58(version range:>=0.2.5)
| +-pywaves(version range:>=0.8.8,<0.8.12)
| | +- base58(version range:*)
```



```
11-Cut1-after
WavesGatewayFramework-master
| +-base58(version range:>=0.2.5)
| +-pywaves(version range:>=0.8.8,<0.8.12)
| | +- base58(version range:*)
```



### (issue) 11-Cut2 

```
11-Cut2-before
WavesGatewayFramework-master
| +-base58(version range:>=0.2.5)
| +-pywaves(version range:>=0.8.12,<=0.8.57.post3)
| | +- base58(version range:==0.2.5)
```



```
11-Cut2-after
WavesGatewayFramework-master
| +-base58(version range:>=0.2.5)
| +-pywaves(version range:>=0.8.12,<=0.8.57.post3)
| | +- base58(version range:==0.2.5)
```



## 12

### (issue) 12-Cut1 

```
12-Cut1-before
twitterbots-master
| +-requests(version range:==2.21.0)
| | +-urllib3(version range:>=1.21.1,<1.25)
| +-urllib3(version range:>=1.24.2)
```



```
12-Cut1-after
twitterbots-master
| +- no call to requests, the dependency can be removed
| +- no call to urllib3, the dependency can be removed
```



## 15

### (issue) 15-Cut1 

```
15-Cut1-before
AWSBucketDump-master
| +-requests(version range:==2.20.0)
| | +-urllib3(version range:>=1.21.1,<1.25)
| +- urllib3(version range:*)
```



```
15-Cut1-after
AWSBucketDump-master
| +-requests(version range:>=2.20.0,<=2.21.0) 
| | +-urllib3(version range:>=1.21, <1.25) 
| +- no call to urllib3, the dependency can be removed
```

## 18

### 18-Cut1 

```
18-Cut1-before
scrapy-redis-bloomfilter-block-cluster-1.0.1
| +-redis(version range:>=2.10)
| +-redis-py-cluster(version range:==1.3.4)
| | +- redis(version range:>=2.10.2)
```



```
18-Cut1-after
scrapy-redis-bloomfilter-block-cluster-1.0.1
| +-redis(version range:>=2.10)
| +-redis-py-cluster(version range:==1.3.4)
| | +- redis(version range:>=2.10.2)
```



### 18-Cut2 

```
18-Cut2-before
scrapy-redis-bloomfilter-block-cluster-1.0.1
| +-redis(version range:>=2.10)
| +-redis-py-cluster(version range:==1.3.5)
| | +- redis(version range:>=2.10.6)
```



```
18-Cut2-after
scrapy-redis-bloomfilter-block-cluster-1.0.1
| +-redis(version range:>=2.10)
| +-redis-py-cluster(version range:==1.3.5)
| | +- redis(version range:>=2.10.6)
```



### (issue) 18-Cut3 

```
18-Cut3-before
scrapy-redis-bloomfilter-block-cluster-1.0.1
| +-redis(version range:>=2.10)
| +-redis-py-cluster(version range:==1.3.6)
| | +- redis(version range:==2.10.6)
```



```
18-Cut3-after
scrapy-redis-bloomfilter-block-cluster-1.0.1
| +-redis(version range:>=2.10)
| +-redis-py-cluster(version range:==1.3.6)
| | +- redis(version range:==2.10.6)
```





### 18-Cut4 

```
18-Cut4-before
scrapy-redis-bloomfilter-block-cluster-1.0.1
| +-redis(version range:>=2.10)
| +-redis-py-cluster(version range:==2.0.0)
| | +- redis(version range:<3.1.0,>=3.0.0)
```



```
18-Cut4-after
scrapy-redis-bloomfilter-block-cluster-1.0.1
| +-redis(version range:>=2.10)
| +-redis-py-cluster(version range:==2.0.0)
| | +- redis(version range:<3.1.0,>=3.0.0)
```





### 18-Cut5 

```
18-Cut5-before
scrapy-redis-bloomfilter-block-cluster-1.0.1
| +-redis(version range:>=2.10)
| +-redis-py-cluster(version range:>=2.1.0, <=2.1.3)
| | +- redis(version range:>=3.0.0,<4.0.0)
```



```
18-Cut5-after
scrapy-redis-bloomfilter-block-cluster-1.0.1
| +-redis(version range:>=2.10)
| +-redis-py-cluster(version range:>=2.1.0, <=2.1.3)
| | +- redis(version range:>=3.0.0,<4.0.0)
```



## 19

### (issue) 19-Cut1 

```
19-Cut1-before
unblock-youku-gateway-master
| +-requests(version range:==2.20.0)
| | +-urllib3(version range:>=1.21.1,<1.25)
| +-urllib3(version range:>=1.24.2)
```



```
19-Cut1-after
unblock-youku-gateway-master
| +-requests(version range:>=2.20.0, <=2.21.0)
| | +-urllib3(version range:>=1.21, <1.25)
| +- no call to urllib3, the dependency can be removed
```



## 20

### (issue) 20-Cut1 

```
20-Cut1-before
auto-crawler-ptt-beauty-image-master
| +-requests(version range:==2.21.0)
| | +-urllib3(version range:>=1.21.1,<1.25)
| +-urllib3(version range:*)
```



```
20-Cut1-after
auto-crawler-ptt-beauty-image-master
| +-requests(version range:>=2.20.0, <=2.21.0) 
| | +-urllib3(version range:>=1.21, <1.25)
| +-urllib3(version range:*)
```



## 22

### (issue) 22-Cut1 

```
22-Cut1-before
indy-node
| +-indy-plenum<version range:==1.8.1>
| | +-python-dateutil<version range:==2.6.1>
| +-python-dateutil<version range:*>
```



```
22-Cut1-after
indy-node
| +-indy-plenum<version range:>=1.8.0.dev801,<=1.8.1>
| | +-python-dateutil<version range:==2.6.1>
| +-python-dateutil<version range:*>
```



## 23



### 23-Cut1 

```
23-Cut1-before
runcible-0.0.5
| +-cryptography<version range:==2.4.2>
| +-paramiko<version range:>=2.4.2,<=2.4.3>
| | +- cryptography<version range:>=1.5>
```



```
23-Cut1-after
runcible-0.0.5
| +-no call to cryptography, the dependency can be removed
| +-paramiko<version range:>=2.4.2,<=2.4.3>
| | +- cryptography<version range:>=1.5>
```



### (issue) 23-Cut2 

```
23-Cut2-before
runcible-0.0.5
| +-cryptography<version range:==2.4.2>
| +-paramiko<version range:>=2.5.0,<=2.12.0>
| | +-cryptography<version range:>=2.5>
```



```
23-Cut2-after
runcible-0.0.5
| +-no call to cryptography, the dependency can be removed
| +-paramiko<version range:>=2.5.0,<=2.12.0>
| | +-cryptography<version range:>=2.5>
```



## 35

### (issue) 35-Cut1 

```
35-Cut1-before
cert-issuer
| +-chainpoint(version range:==0.0.2)
| | +-merkletools(version range:==1.0.2)
| | | +-pysha3(version range:==1.0b1)
| +-pysha3(version range:>=1.0.2)
```



```
35-Cut1-after
cert-issuer
| +-chainpoint(version range:==0.0.2)
| | +-merkletools(version range:==1.0.2)
| | | +-pysha3(version range:*)
| +-no call to pysha3, the dependency can be removed
```





## 37

### 37-Cut1 

```
37-Cut1-before
crema
| +-librosa<version range:==0.5>
| +-pumpp<version range: >=0.3.2,<=0.3.3>
| | +-librosa<version range:>=0.5.0>
```



```
37-Cut1-after
crema
| +-librosa<version range:>=0.2.0, <=0.5.0> 
| +-pumpp<version range:>=0.3.1,<=0.3.3>
| | +-librosa<version range:>=0.5.0rc0>
```





### (issue) 37-Cut2 

```
37-Cut2-before
crema
| +-librosa<version range:==0.5>
| +-pumpp<version range:>=0.4.0,<=0.5.0>
| | +- librosa<version range:>=0.6.2>
```



```
37-Cut2-after
crema
| +-librosa<version range:>=0.2.0, <=0.5.0> 
| +-pumpp<version range:>=0.4.0,<=0.5.0>
| | +- librosa<version range:>=0.6.2> 
```



### 37-Cut3 

```
37-Cut3-before
crema
| +-librosa<version range:==0.5>
| +-pumpp<version range:==0.6.0>
| | +- librosa<version range:>=0.8.0>
```



```
37-Cut3-after
crema
| +-librosa<version range:>=0.2.0, <=0.5.0>
| +-pumpp<version range:==0.6.0>
| | +- librosa<version range:>=0.8.0>
```







## 40



### (issue) 40-Cut1 

```
40-Cut1-before
whats-bot-master
| +-chatterbot-corpus(version range:==1.1.4)
| | +-pyyaml(version range:>=3.12,<4.0)
| +-pyyaml(version range:>=4.2b1)
```



```
40-Cut1-after
whats-bot-master
| +-no call to chatterbot-corpus, the dependency can be removed
| +-no call to pyyaml, the dependency can be removed
```



## 41

### (issue) 41-Cut1 

```
41-Cut1-before
zarp-0.1.8
| +-netlib(version range:==0.11.1)
| | +-pyopenssl(version range:>=0.14)
| +-pyopenssl(version range:==0.13.1)
```



```
41-Cut1-after
zarp-0.1.8
| +-netlib(version range:>=0.11.1, <=0.11.2) 
| | +-pyopenssl(version range:>=0.14) 
| +-pyopenssl(version range:==0.13.1) 
```



## 46

### (issue) 46-Cut1 

```
46-Cut1-before
Hidden-Friends-Finder-master
| +-requests(version range:==2.21.0)
| | +-urllib3(version range:>=1.21.1,<1.25)
| +-urllib3(version range:>=1.24.2)
```



```
46-Cut1-after
Hidden-Friends-Finder-master
| +-no call to requests, the dependency can be removed
| +-no call to urllib3, the dependency can be removed
```





## 50

### (issue) 50-Cut1 

```
50-Cut1-before
discord-wow-armory-bot-4.0.5
| +-aiohttp(version range:==3.5.4)
| +-discord-py(version range:==0.16.12)
| | +-aiohttp(version range:>=1.0.0,<1.1.0)
```



```
50-Cut1-after
discord-wow-armory-bot-4.0.5
| +-aiohttp(version range:>=3.5.2, <=3.5.4) 
| +-discord-py(version range:>=0.6.8, <=0.16.12) 
| | +-aiohttp(version range:>=1.0.0,<1.1.0)
```



## 52

### (issue) 52-Cut1 

```
52-Cut1-before
CoinMarketCap-Historical-Prices-master
| +-requests(version range:==2.21.0)
| | +-urllib3(version range:>=1.21.1,<1.25)
| +-urllib3(version range:==1.25)
```



```
52-Cut1-after
CoinMarketCap-Historical-Prices-master
| +-requests(version range:>=2.20.0, <=2.21.0) 
| | +-urllib3(version range:>=1.21,<1.25)
| +-no call to urllib3, the dependency can be removed
```



## 55 

### (issue) 55-Cut1 

```
55-Cut1-before
COCO-Style-Dataset-Generator-GUI-master
| +-jedi(version range:==0.11.1)
| | +-parso(version range:==0.1.1)
| +-parso(version range:==0.5.1)
```



```
55-Cut1-after
COCO-Style-Dataset-Generator-GUI-master
| +-no call to jedi, the dependency can be removed
| +-no call to parso, the dependency can be removed
```



## 56

### (issue) 56-Cut1 

```
56-Cut1-before
api-indotel-master
| +-requests(version range:==2.21.0)
| | +-urllib3(version range:>=1.21.1,<1.25)
| +-urllib3(version range:==1.25.2)
```



```
56-Cut1-after
api-indotel-master
| +-requests(version range:>=2.20.0, <=2.21.0)
| | +-urllib3(version range:>=1.21,<1.25)
| +-no call to urllib3, the dependency can be removed
```





## 58



### 58-Cut1 

```
58-Cut1-before
jawfish-master
| +-flask(version range:>=0.12.3,<=0.12.4)
| | +- werkzeug(version range:>=0.7)
| +- werkzeug(version range:==0.11.11)
```



```
58-Cut1-after
jawfish-master
| +-flask(version range:>=0.12.3,<=0.12.4)
| | +- werkzeug(version range:>=0.7) 
| +- no call to werkzeug, the dependency can be removed
```



### 58-Cut2 

```
58-Cut2-before
jawfish-master
| +-flask(version range:==0.12.5)
| | +- werkzeug(version range:>=0.7,<1.0)
| +- werkzeug(version range:==0.11.11)
```



```
58-Cut2-after
jawfish-master
| +-flask(version range:==0.12.5) 
| | +-  werkzeug(version range:>=0.7,<1.0) 
| +- no call to werkzeug, the dependency can be removed
```



### 58-Cut3 

```
58-Cut3-before
jawfish-master
| +-flask(version range:>=1.0,<1.1.0)
| | +- werkzeug(version range:>=0.14)
| +- werkzeug(version range:==0.11.11)
```



```
58-Cut3-after
jawfish-master
| +-flask(version range:>=1.0,<1.1.0) 
| | +-  werkzeug(version range:>=0.14) 
| +- no call to werkzeug, the dependency can be removed
```



### (issue) 58-Cut4 

```
58-Cut4-before
jawfish-master
| +-flask(version range:>=1.1.0,<=1.1.2)
| | +- werkzeug(version range:>=0.15)
| +- werkzeug(version range:==0.11.11)
```



```
58-Cut4-after
jawfish-master
| +-flask(version range:>=1.1.0,<=1.1.2)
| | +- werkzeug(version range:>=0.15) 
| +- no call to werkzeug, the dependency can be removed
```



### 58-Cut5 

```
58-Cut5-before
jawfish-master
| +-flask(version range:>=2.0.0rc1, <=2.0.0rc2)
| | +- werkzeug(version range:>=2.0.0rc4)
| +- werkzeug(version range:==0.11.11)
```



```
58-Cut5-after
jawfish-master
| +-flask(version range:>=2.0.0rc1, <=2.0.0rc2)
| | +- werkzeug(version range:>=2.0.0rc4)
| +- no call to werkzeug, the dependency can be removed
```



### 58-Cut6 

```
58-Cut6-before
jawfish-master
| +-flask(version range:>=2.0.0,<=2.1.3)
| | +- werkzeug(version range:>=2.0)
| +- werkzeug(version range:==0.11.11)
```



```
58-Cut6-after
jawfish-master
| +-flask(version range:>=2.0.0,<=2.1.3)
| | +- werkzeug(version range:>=2.0)
| +- no call to werkzeug, the dependency can be removed
```



### 58-Cut7  

```
58-Cut7-before
jawfish-master
| +-flask(version range:>=2.2.0,<=2.2.1)
| | +- werkzeug(version range:>=2.2.0)
| +- werkzeug(version range:==0.11.11)
```



```
58-Cut7-after
jawfish-master
| +-flask(version range:>=2.2.0,<=2.2.1)
| | +- werkzeug(version range:>=2.2.0)
| +- no call to werkzeug, the dependency can be removed
```





### 58-Cut8  

```
58-Cut8-before
jawfish-master
| +-flask(version range:==2.2.2)
| | +- werkzeug(version range:>=2.2.2)
| +- werkzeug(version range:==0.11.11)
```



```
58-Cut8-after
jawfish-master
| +-flask(version range:==2.2.2)
| | +- werkzeug(version range:>=2.2.2)
| +- no call to werkzeug, the dependency can be removed
```





## 59

````
59-Cut0
ltiauthenticator-0.3
| +-jupyterhub(version range:>=0.8, <=0.9.6)
| | +-no dependency on oauthlib
| +-oauthlib(version range:==2.*)
````





### 59-Cut1 

```
59-Cut1-before
ltiauthenticator-0.3
| +-jupyterhub(version range:==1.0.0b1)
| | +- oauthlib(version range:>=2.0,<3) 
| +-oauthlib(version range:==2.*)
```



```
59-Cut1-after
ltiauthenticator-0.3
| +-jupyterhub(version range:==1.0.0b1)
| | +- oauthlib(version range:>=2.0,<3) 
| +-oauthlib(version range:>=1.0,<3) 
```





### (issue) 59-Cut2 

```
59-Cut2-before
ltiauthenticator-0.3
| +-jupyterhub(version range:>=1.0.0b2,<=3.1.0)
| | +-oauthlib(version range:>=3.0)
| +-oauthlib(version range:==2.*)
```



```
59-Cut2-after
ltiauthenticator-0.3
| +-jupyterhub(version range:>=1.0.0b2,<=3.1.0)
| | +- oauthlib(version range:>=3.0)
| +-oauthlib(version range:>=1.0,<3)
```





## 65

### 65-Cut1 

```
65-Cut1-before
dedis-cluster - 1.0.2
| +- redis(version range:>=2.10.5)
| +- redis-py-cluster(version range:>=1.2.0, <=1.3.4)
| | +- redis(version range:>=2.10.2)
```



```
65-Cut1-after
dedis-cluster - 1.0.2
| +- redis(version range:>=0.6.0)
| +- redis-py-cluster(version range:>=1.2.0, <=1.3.4)
| | +- redis(version range:>=2.10.2)
```





### 65-Cut2 

```
65-Cut2-before
dedis-cluster - 1.0.2
| +- redis(version range:>=2.10.5)
| +- redis-py-cluster(version range:==1.3.5)
| | +- redis(version range:>=2.10.6)
```



```
65-Cut2-after
dedis-cluster - 1.0.2
| +- redis(version range:>=0.6.0)
| +- redis-py-cluster(version range:==1.3.5)
| | +- redis(version range:>=2.10.6)
```





### 65-Cut3 

```
65-Cut3-before
dedis-cluster - 1.0.2
| +- redis(version range:>=2.10.5)
| +- redis-py-cluster(version range:==1.3.6)
| | +- redis(version range:==2.10.6)
```



```
65-Cut3-after
dedis-cluster - 1.0.2
| +- redis(version range:>=0.6.0)
| +- redis-py-cluster(version range:==1.3.6)
| | +- redis(version range:==2.10.6)
```





### (issue) 65-Cut4 

```
65-Cut4-before
dedis-cluster - 1.0.2
| +- redis(version range:>=2.10.5)
| +- redis-py-cluster(version range:==2.0.0)
| | +- redis(version range:<3.1.0,>=3.0.0)
```



```
65-Cut4-after
dedis-cluster - 1.0.2
| +- redis(version range:>=0.6.0)
| +- redis-py-cluster(version range:==2.0.0)
| | +- redis(version range:<3.1.0,>=3.0.0)
```





### 65-Cut5 

```
65-Cut5-before
dedis-cluster - 1.0.2
| +- redis(version range:>=2.10.5)
| +- redis-py-cluster(version range:>=2.1.0, <=2.1.3)
| | +- redis(version range:>=3.0.0,<4.0.0)
```



```
65-Cut5-after
dedis-cluster - 1.0.2
| +- redis(version range:>=0.6.0)
| +- redis-py-cluster(version range:>=2.1.0, <=2.1.3)
| | +- redis(version range:>=3.0.0,<4.0.0)
```



## 66

### 66-Cut1 

```
66-Cut1-before
python-novaclient 2.27.0
| +- oslo-serialization(version range:>=1.4.0,<=1.5.0)
| | +- pbr(version range:>=0.6,!=0.7,<1.0)
| +- pbr(version range:>=1.6,<2.0)
```



```
66-Cut1-after
python-novaclient 2.27.0
| +- oslo-serialization(version range:>=1.2.0,<=1.5.0)
| | +- no call to pbr, the dependency can be removed
| +- pbr(version range:>=1.6,<2.0) 
```



### 66-Cut2 

```
66-Cut2-before
python-novaclient 2.27.0
| +- oslo-serialization(version range:>=1.6.0,<=1.7.0)
| | +- pbr(version range:>=0.11,<2.0)
| +- pbr(version range:>=1.6,<2.0)
```



```
66-Cut2-after
python-novaclient 2.27.0
| +- oslo-serialization(version range:>=1.6.0,<=1.7.0)
| | +- no call to pbr, the dependency can be removed
| +- pbr(version range:>=1.6,<2.0) 
```





### 66-Cut3 

```
66-Cut3-before
python-novaclient 2.27.0
| +- oslo-serialization(version range:==1.8.0)
| | +- pbr(version range:<2.0,>=1.3)
| +- pbr(version range:>=1.6,<2.0)
```



```
66-Cut3-after
python-novaclient 2.27.0
| +- oslo-serialization(version range:==1.8.0)
| | +- no call to pbr, the dependency can be removed
| +- pbr(version range:>=1.6,<2.0)
```





### 66-Cut4 

```
66-Cut4-before
python-novaclient 2.27.0
| +- oslo-serialization(version range:==1.9.0)
| | +- pbr(version range:<2.0,>=1.6)
| +- pbr(version range:>=1.6,<2.0)
```



```
66-Cut4-after
python-novaclient 2.27.0
| +- oslo-serialization(version range:==1.9.0)
| | +- no call to pbr, the dependency can be removed
| +- pbr(version range:>=1.6,<2.0)
```





### 66-Cut5 

```
66-Cut5-before
python-novaclient 2.27.0
| +- oslo-serialization(version range:>=1.10.0, <=2.14.0)
| | +- pbr(version range:>=1.6)
| +- pbr(version range:>=1.6,<2.0)
```



```
66-Cut5-after
python-novaclient 2.27.0
| +- oslo-serialization(version range:>=1.10.0, <=2.14.0)
| | +- no call to pbr, the dependency can be removed
| +- pbr(version range:>=1.6,<2.0)
```



### 66-Cut6 

```
66-Cut6-before
python-novaclient 2.27.0
| +- oslo-serialization(version range:>=2.15.0, <=2.16.1)
| | +- pbr(version range:>=1.8)
| +- pbr(version range:>=1.6,<2.0)
```



```
66-Cut6-after
python-novaclient 2.27.0
| +- oslo-serialization(version range:>=2.15.0, <=2.16.1)
| | +- no call to pbr, the dependency can be removed
| +- pbr(version range:>=1.6,<2.0)
```



### 66-Cut7 

```
66-Cut7-before
python-novaclient 2.27.0
| +- oslo-serialization(version range:>=2.17.0, <=2.18.0)
| | +- pbr(version range:>=2.0.0)
| +- pbr(version range:>=1.6,<2.0)
```



```
66-Cut7-after
python-novaclient 2.27.0
| +- oslo-serialization(version range:>=2.17.0, <=2.18.0)
| | +- no call to pbr, the dependency can be removed
| +- pbr(version range:>=1.6,<2.0)
```





### (issue) 66-Cut8 

```
66-Cut8-before
python-novaclient 2.27.0
| +- oslo-serialization(version range:>=2.19.0,<=5.0.0)
| | +- pbr(version range:!=2.1.0,>=2.0.0)
| +- pbr(version range:>=1.6,<2.0)
```



```
66-Cut8-after
python-novaclient 2.27.0
| +- oslo-serialization(version range:>=2.19.0,<=5.0.0)
| | +- no call to pbr, the dependency can be removed
| +- pbr(version range:>=1.6,<2.0)
```





## 73



````
73-Cut0
flask-mongokat - 1.0
| +- mongokat(version range:==0.1.0)
| | +- no dependency on pymongo
| +- pymongo(version range:*)
````





### 73-Cut1 


```
73-Cut1-before
flask-mongokat - 1.0
| +- mongokat(version range:>=0.1.1,<=0.1.4)
| | +- pymongo (version range:==3.0.2)
| +- pymongo(version range:*)
```




```
73-Cut1-after
flask-mongokat - 1.0
| +- mongokat(version range:>=0.1.1,<=0.1.4)
| | +- pymongo (version range:>=3.0, <=3.3.1)
| +- pymongo(version range:*)
```







### (issue) 73-Cut2 


```
73-Cut2-before
flask-mongokat - 1.0
| +- mongokat(version range:==0.2.0)
| | +- pymongo (version range:==3.0.3)
| +- pymongo(version range:*)
```




```
73-Cut2-after
flask-mongokat - 1.0
| +- mongokat(version range:==0.2.0)
| | +- pymongo (version range:>=3.0, <=3.3.1)
| +- pymongo(version range:*)
```



## 77



```
77-Cut0
imgsync - 1.1.3
| +- python-glanceclient(version range:>=0.1.1,<=0.9.0)
| | +- no dependency on pbr
| +- pbr(version range:<1.0,>=0.6)
```






### 77-Cut1 

```
77-Cut1-before
imgsync - 1.1.3
| +- python-glanceclient(version range:==0.10.0)
| | +- pbr(version range:>=0.5,<0.6)
| +- pbr(version range:<1.0,>=0.6)
```



```
77-Cut1-after
imgsync - 1.1.3
| +- python-glanceclient(version range:==0.10.0)
| | +- pbr(version range:>=0.5,<0.6)
| +- pbr(version range:<1.0,>=0.6)
```





### 77-Cut2 

```
77-Cut2-before
imgsync - 1.1.3
| +- python-glanceclient(version range:>=0.11.0,<=0.12.0)
| | +- pbr(version range:>=0.5.21,<1.0)
| +- pbr(version range:<1.0,>=0.6)
```



```
77-Cut2-after
imgsync - 1.1.3
| +- python-glanceclient(version range:>=0.11.0,<=0.12.0)
| | +- pbr(version range:>=0.5.21,<1.0) 
| +- pbr(version range:<1.0,>=0.6) 
```





### 77-Cut3 

```
77-Cut3-before
imgsync - 1.1.3
| +- python-glanceclient(version range:>=0.13.1, <=0.19.0)
| | +- pbr(version range:*) 
| +- pbr(version range:<1.0,>=0.6)
```



```
77-Cut3-after
imgsync - 1.1.3
| +- python-glanceclient(version range:>=0.13.1, <=0.19.0)
| | +- pbr(version range:*) 
| +- pbr(version range:<1.0,>=0.6)
```





### 77-Cut4 

```
77-Cut4-before
imgsync - 1.1.3
| +- python-glanceclient(version range:>=1.0.0,<=1.1.0)
| | +- pbr(version range:>=1.3)
| +- pbr(version range:<1.0,>=0.6)
```



```
77-Cut4-after
imgsync - 1.1.3
| +- python-glanceclient(version range:>=1.0.0,<=1.1.0)
| | +- pbr(version range:>=1.0) 
| +- pbr(version range:<1.0,>=0.6)
```





### 77-Cut5  

```
77-Cut5-before
imgsync - 1.1.3
| +- python-glanceclient(version range:>=1.1.1,<=2.6.0)
| | +- pbr(version range:>=1.8)
| +- pbr(version range:<1.0,>=0.6)
```



```
77-Cut5-after
imgsync - 1.1.3
| +- python-glanceclient(version range:>=1.1.1,<=2.6.0)
| | +- pbr(version range:>=1.6)
| +- pbr(version range:<1.0,>=0.6)
```





### (issue) 77-Cut6 

```
77-Cut6-before
imgsync - 1.1.3
| +- python-glanceclient(version range:>=2.7.0,<=4.2.0)
| | +- pbr(version range:>=2.0.0)
| +- pbr(version range:<1.0,>=0.6)
```



```
77-Cut6-after
imgsync - 1.1.3
| +- python-glanceclient(version range:>=2.7.0,<=4.2.0)
| | +- pbr(version range:>=2.0.0)
| +- pbr(version range:<1.0,>=0.6)
```



## 78 

### 78-Cut1 

```
78-Cut1-before
iprange-python - 0.0.8
| +- redis(version range:>=2.10.6)
| +- redis-py-cluster(version range:==1.3.4)
| | +- redis(version range:>=2.10.2)
```



```
78-Cut1-after
iprange-python - 0.0.8
| +- redis(version range:>=2.10.6)
| +- redis-py-cluster(version range:==1.3.4)
| | +- redis(version range:>=2.10.2)
```





### 78-Cut2 


```
78-Cut2-before
iprange-python - 0.0.8
| +- redis(version range:>=2.10.6)
| +- redis-py-cluster(version range:==1.3.5)
| | +- redis(version range:>=2.10.6)
```




```
78-Cut2-after
iprange-python - 0.0.8
| +- redis(version range:>=2.10.6)
| +- redis-py-cluster(version range:==1.3.5)
| | +- redis(version range:>=2.10.6)
```



### 78-Cut3 


```
78-Cut3-before
iprange-python - 0.0.8
| +- redis(version range:>=2.10.6)
| +- redis-py-cluster(version range: ==1.3.6)
| | +- redis(version range:==2.10.6)
```




```
78-Cut3-after
iprange-python - 0.0.8
| +- redis(version range:>=2.10.6)
| +- redis-py-cluster(version range: ==1.3.6)
| | +- redis(version range:==2.10.6)
```





### (issue) 78-Cut4 


```
78-Cut4-before
iprange-python - 0.0.8
| +- redis(version range:>=2.10.6)
| +- redis-py-cluster(version range:==2.0.0)
| | +- redis(version range:<3.1.0,>=3.0.0)
```




```
78-Cut4-after
iprange-python - 0.0.8
| +- redis(version range:>=2.10.6)
| +- redis-py-cluster(version range:==2.0.0)
| | +- redis(version range:<3.1.0,>=3.0.0)
```





### 78-Cut5 


```
78-Cut5-before
iprange-python - 0.0.8
| +- redis(version range:>=2.10.6)
| +- redis-py-cluster(version range:>=2.1.0, <=2.1.3)
| | +- redis(version range:>=3.0.0,<4.0.0)
```




```
78-Cut5-after
iprange-python - 0.0.8
| +- redis(version range:>=2.10.6)
| +- redis-py-cluster(version range:>=2.1.0, <=2.1.3)
| | +- redis(version range:>=3.0.0,<4.0.0)
```



## 82 



### (issue) 82-Cut1 



```
82-Cut1-before
musco-tf - 1.0.2
| +- numpy(version range:*)
| +- scikit-tensor-py3(version range:==0.4.1)
| | +- numpy(version range:==1.16.*)
```



```
82-Cut1-after
musco-tf - 1.0.2
| +- numpy(version range:*)
| +- scikit-tensor-py3(version range:==0.4.1)
| | +- numpy(version range:==1.16.*)
```



### 82-Cut2 


```
82-Cut2-before
musco-tf - 1.0.2
| +- numpy(version range:*)
| +- scikit-tensor-py3(version range:>=0.2.0,<=0.2.1)
| | +- numpy(version range:*)
```




```
82-Cut2-after
musco-tf - 1.0.2
| +- numpy(version range:*)
| +- scikit-tensor-py3(version range:>=0.2.0,<=0.2.1)
| | +- numpy(version range:*)
```



## 83

### (issue) 83-Cut1 

```
83-Cut1-before
musco-pytorch - 1.0.3
| +- numpy(version range:*)
| +- scikit-tensor-py3(version range:0.4.1)
| | +- numpy(version range:==1.16.*)
```



```
83-Cut1-after
musco-pytorch - 1.0.3
| +- numpy(version range:*)
| +- scikit-tensor-py3(version range:0.4.1)
| | +- numpy(version range:==1.16.*)
```



### 83-Cut2 


```
83-Cut2-before
musco-pytorch - 1.0.3
| +- numpy(version range:*)
| +- scikit-tensor-py3(version range:>=0.2.0,<=0.2.1)
| | +- numpy(version range:*)
```




```
83-Cut2-after
musco-pytorch - 1.0.3
| +- numpy(version range:*)
| +- scikit-tensor-py3(version range:>=0.2.0,<=0.2.1)
| | +- numpy(version range:*)
```





## 86



### (issue) 86-Cut1 

```
86-Cut1-before
programy - 3.9.1
| +- tweepy(version range:==3.8.0)
| | +- six(version range:>=1.10.0)
| +- kik(version range:==1.5.0)
| | +- six(version range:==1.10.0)
```



```
86-Cut1-after
programy - 3.9.1
| +- tweepy(version range:==3.8.0)
| | +- six(version range:>=1.8.0)
| +- kik(version range:==1.5.0) 
| | +- six(version range:>=1.10.0, <=1.16.0)
```



## 92



### 92-Cut1 

```
92-Cut1-before
pyclics-clustering - 1.0.0
| +- networkx(version range:*)
| +- pyclics(version range:==2.0.0)
| | +- networkx(version range:*)
```



```
92-Cut1-after
pyclics-clustering - 1.0.0
| +- networkx(version range:*)
| +- pyclics(version range:==2.0.0)
| | +- networkx(version range:*)
```



### (issue) 92-Cut2 

```
92-Cut2-before
pyclics-clustering - 1.0.0
| +- networkx(version range:*)
| +- pyclics(version range:>=3.0.0,<=3.0.1)
| | +- networkx(version range:==2.1)
```



```
92-Cut2-after
pyclics-clustering - 1.0.0
| +- networkx(version range:*)
| +- pyclics(version range:>=3.0.0,<=3.0.1)
| | +- networkx(version range:==2.1)
```





### 92-Cut3 

```
92-Cut3-before
pyclics-clustering - 1.0.0
| +- networkx(version range:*)
| +- pyclics(version range:==3.0.2)
| | +- networkx(version range:>=2.1)
```



```
92-Cut3-after
pyclics-clustering - 1.0.0
| +- networkx(version range:*)
| +- pyclics(version range:==3.0.2)
| | +- networkx(version range:>=2.1)
```



## 96



### 96-Cut1 

```
96-Cut1-before
quantadex - 1.2.1
| +- graphenelib(version range:==1.1.2)
| | +- pycryptodome(version range:==3.7.3)
| +- pycryptodome(version range:*)
```



```
96-Cut1-after
quantadex - 1.2.1
| +- graphenelib(version range:==1.1.2)
| | +- pycryptodome(version range:>=3.2, <=3.14.1)
| +- pycryptodome(version range:*)
```





### 96-Cut2 


```
96-Cut2-before
quantadex - 1.2.1
| +- graphenelib(version range:>=1.1.13,<=1.1.17)
| | +- pycryptodome(version range:==3.8.0)
| +- pycryptodome(version range:*)
```




```
96-Cut2-after
quantadex - 1.2.1
| +- graphenelib(version range:>=1.1.13,<=1.1.17)
| | +- pycryptodome(version range:>=3.2, <=3.14.1)
| +- pycryptodome(version range:*)
```





### 96-Cut3 


```
96-Cut3-before
quantadex - 1.2.1
| +- graphenelib(version range:==1.1.18)
| | +- pycryptodome(version range:==3.8.1)
| +- pycryptodome(version range:*)
```




```
96-Cut3-after
quantadex - 1.2.1
| +- graphenelib(version range:==1.1.18)
| | +- pycryptodome(version range:>=3.2, <=3.14.1)
| +- pycryptodome(version range:*)
```





### (issue) 96-Cut4 


```
96-Cut4-before
quantadex - 1.2.1
| +- graphenelib(version range:>=1.1.19,<=1.2.0)
| | +- pycryptodome(version range:==3.8.2)
| +- pycryptodome(version range:*)
```




```
96-Cut4-after
quantadex - 1.2.1
| +- graphenelib(version range:>=1.1.19,<=1.2.0)
| | +- pycryptodome(version range:>=3.2, <=3.14.1)
| +- pycryptodome(version range:*)
```







### 96-Cut5 

```
96-Cut5-before
quantadex - 1.2.1
| +- graphenelib(version range:>=1.3.0,<=1.3.1)
| | +- pycryptodome(version range:==3.9.1)
| +- pycryptodome(version range:*)
```



```
96-Cut5-after
quantadex - 1.2.1
| +- graphenelib(version range:>=1.3.0,<=1.3.1)
| | +- pycryptodome(version range:>=3.2, <=3.14.1)
| +- pycryptodome(version range:*)
```





### 96-Cut6 

```
96-Cut6-before
quantadex - 1.2.1
| +- graphenelib(version range:>=1.3.2,<=1.5.4)
| | +- pycryptodome(version range:>=3.9.1, <4)
| +- pycryptodome(version range:*)
```



```
96-Cut6-after
quantadex - 1.2.1
| +- graphenelib(version range:>=1.3.2,<=1.5.4)
| | +- pycryptodome(version range:>=3.2, <4)
| +- pycryptodome(version range:*)
```



### 96-Cut7 

```
96-Cut7-before
quantadex - 1.2.1
| +- graphenelib(version range:>=1.0.1,<=1.1.11)
| | +- pycryptodome(version range:*)
| +- pycryptodome(version range:*)
```



```
96-Cut7-after
quantadex - 1.2.1
| +- graphenelib(version range:>=1.0.1,<=1.1.11)
| | +- pycryptodome(version range:*)
| +- pycryptodome(version range:*)
```





## 98



### 98-Cut1 

```
98-Cut1-before
redis-pubsub-dict - 0.0.2
| +- redis(=version range:*)
| +- redis-py-cluster(=version range:==0.1.0)
| | +- redis(version range:>=2.9.1)
```



```
98-Cut1-after
redis-pubsub-dict - 0.0.2
| +- redis(=version range:*)
| +- redis-py-cluster(=version range:==0.1.0)
| | +- redis(version range:>=2.9.0)
```





### 98-Cut2 


```
98-Cut2-before
redis-pubsub-dict - 0.0.2
| +- redis(=version range:*)
| +- redis-py-cluster(version range:>=0.2.0, <=1.3.4)
| | +- redis(version range:>=2.10.2)
```




```
98-Cut2-after
redis-pubsub-dict - 0.0.2
| +- redis(=version range:*)
| +- redis-py-cluster(version range:>=0.2.0, <=1.3.4)
| | +- redis(version range:>=2.10.2)
```





### 98-Cut3 


```
98-Cut3-before
redis-pubsub-dict - 0.0.2
| +- redis(=version range:*)
| +- redis-py-cluster(version range:==1.3.5)
| | +- redis(version range:>=2.10.6)
```




```
98-Cut3-after
redis-pubsub-dict - 0.0.2
| +- redis(=version range:*)
| +- redis-py-cluster(version range:==1.3.5)
| | +- redis(version range:>=2.10.6)
```





### 98-Cut4 


```
98-Cut4-before
redis-pubsub-dict - 0.0.2
| +- redis(=version range:*)
| +- redis-py-cluster(version range:==1.3.6)
| | +- redis(version range:==2.10.6)
```




```
98-Cut4-after
redis-pubsub-dict - 0.0.2
| +- redis(=version range:*)
| +- redis-py-cluster(version range:==1.3.6)
| | +- redis(version range:==2.10.6)
```



### (issue) 98-Cut5 


```
98-Cut5-before
redis-pubsub-dict - 0.0.2
| +- redis(=version range:*)
| +- redis-py-cluster(version range:==2.0.0)
| | +- redis(version range:<3.1.0,>=3.0.0)
```




```
98-Cut5-after
redis-pubsub-dict - 0.0.2
| +- redis(=version range:*)
| +- redis-py-cluster(version range:==2.0.0)
| | +- redis(version range:<3.1.0,>=3.0.0)
```



### 98-Cut6 


```
98-Cut6-before
redis-pubsub-dict - 0.0.2
| +- redis(=version range:*)
| +- redis-py-cluster(version range:>=2.1.0, <=2.1.3)
| | +- redis(version range:>=3.0.0,<4.0.0)
```




```
98-Cut6-after
redis-pubsub-dict - 0.0.2
| +- redis(=version range:*)
| +- redis-py-cluster(version range:>=2.1.0, <=2.1.3)
| | +- redis(version range:>=3.0.0,<4.0.0)
```



## 99



### 99-Cut1 

```
99-Cut1-before
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<6)
| +- elasticsearch-dsl(version range:==0.0.2)
| | +- elasticsearch(version range:>=1.0.0)
```



```
99-Cut1-after
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<=6.1.1)
| +- elasticsearch-dsl(version range:==0.0.2)
| | +- no call to elasticsearch, the dependency can be removed
```





### 99-Cut2 

```
99-Cut2-before
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<6)
| +- elasticsearch-dsl(version range:>0.0.2,<0.0.10)
| | +- elasticsearch(version range:>=1.0.0)
```



```
99-Cut2-after
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<=6.1.1)
| +- elasticsearch-dsl(version range:>0.0.2,<0.0.10)
| | +- elasticsearch(version range:>=1.0.0)
```



### 99-Cut3 

```
99-Cut3-before
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<6)
| +- elasticsearch-dsl(version range:>=0.0.10,<=0.0.11)
| | +- elasticsearch(version range:>=1.0.0, <2.0.0)
```



```
99-Cut3-after
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<=6.1.1)
| +- elasticsearch-dsl(version range:>=0.0.10,<=0.0.11)
| | +- elasticsearch(version range:>=1.0.0, <=2.1.0)
```





### 99-Cut4 

```
99-Cut4-before
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<6)
| +- elasticsearch-dsl(version range:>=2.0.0,<=2.2.0)
| | +- elasticsearch(version range: >=2.0.0,<3.0.0)
```



```
99-Cut4-after
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<=6.1.1)
| +- elasticsearch-dsl(version range:>=2.0.0,<=2.2.0)
| | +- elasticsearch(version range: >=1.8.0,<3.0.0)
```





### 99-Cut5 

```
99-Cut5-before
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<6)
| +- elasticsearch-dsl(version range:>=5.0.0,<6)
| | +- elasticsearch(version range:>=5.0.0,<6.0.0)
```



```
99-Cut5-after
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<=6.1.1)
| +- elasticsearch-dsl(version range:>=5.0.0,<6)
| | +- elasticsearch(version range:>=5.0.0,<=6.1.1)
```





### 99-Cut6 

```
99-Cut6-before
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<6)
| +- elasticsearch-dsl(version range:>=6.0.0,<7)
| | +- elasticsearch(version range:>=6.0.0,<7.0.0)
```



```
99-Cut6-after
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<=6.1.1)
| +- elasticsearch-dsl(version range:>=6.0.0,<7)
| | +- elasticsearch(version range:>=5.5.1,<7.0.5)
```





### (issue) 99-Cut7 

```
99-Cut7-before
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<6)
| +- elasticsearch-dsl(version range:>=7.0.0,<=7.4.0)
| | +- elasticsearch(version range:>=7.0.0,<8.0.0)
```



```
99-Cut7-after
rdfframework - 0.0.38
| +- elasticsearch(version range:>5.4.0,<=6.1.1)
| +- elasticsearch-dsl(version range:>=7.0.0,<=7.4.0)
| | +- elasticsearch(version range:>=6.8.0,<8.0.0)
```



## 107




```
107-Cut0
scvelo - 0.1.24
| +- matplotlib(version range:>=2.2)
| +- scanpy(version range:>=1.8.0,<=1.9.1,!=1.8.2)
| | +- no dependency on matplotlib
```



### 107-Cut1 

```
107-Cut1-before
scvelo - 0.1.24
| +- matplotlib(version range:>=2.2)
| +- scanpy(version range:==1.4)
| | +- matplotlib(version range:>=2.2)
```



```
107-Cut1-after
scvelo - 0.1.24
| +- matplotlib(version range:>=2.2)
| +- scanpy(version range:==1.4)
| | +- matplotlib(version range:>=2.2)
```





### 107-Cut2 


```
107-Cut2-before
scvelo - 0.1.24
| +- matplotlib(version range:>=2.2)
| +- scanpy(version range:>=1.4.1,<=1.4.3)
| | +- matplotlib(version range:>=3.0.0)
```




```
107-Cut2-after
scvelo - 0.1.24
| +- matplotlib(version range:>=2.2)
| +- scanpy(version range:>=1.4.1,<=1.4.3)
| | +- matplotlib(version range:>=3.0.0)
```





### (issue) 107-Cut3 

```
107-Cut3-before
scvelo - 0.1.24
| +- matplotlib(version range:>=2.2)
| +- scanpy(version range:>=1.4.4,<1.4.5.1)
| | +- matplotlib(version range:==3.0.*)
```




```
107-Cut3-after
scvelo - 0.1.24
| +- matplotlib(version range:>=2.2)
| +- scanpy(version range:>=1.4.4,<1.4.5.1)
| | +- matplotlib(version range:==3.0.*)
```





### 107-Cut4 


```
107-Cut4-before
scvelo - 0.1.24
| +- matplotlib(version range:>=2.2)
| +- scanpy(version range:==1.4.5.1)
| | +- matplotlib(version range:>=3.1)
```




```
107-Cut4-after
scvelo - 0.1.24
| +- matplotlib(version range:>=2.2)
| +- scanpy(version range:==1.4.5.1)
| | +- matplotlib(version range:>=3.1)
```





### 107-Cut5 


```
107-Cut5-before
scvelo - 0.1.24
| +- matplotlib(version range:>=2.2)
| +- scanpy(version range:(>=1.4.6,<=1.7.2)U==1.8.2)
| | +- matplotlib(version range:>=3.1.2)
```




```
107-Cut5-after
scvelo - 0.1.24
| +- matplotlib(version range:>=2.2)
| +- scanpy(version range:(>=1.4.6,<=1.7.2)U==1.8.2)
| | +- matplotlib(version range:>=3.1.2)
```







## 108 

### (issue) 108-Cut1 

```
108-Cut1-before
servos-framework - 0.0.1.dev6
| +- pbr(version range:>=1.8)
| +- jsonpath-rw-ext(version range:==1.0.0)
| | +- pbr(version range:>=1.4,<2.0)
```



```
108-Cut1-after
servos-framework - 0.0.1.dev6
| +- no call to pbr, the dependency can be removed
| +- no call to jsonpath-rw-ext, the dependency can be removed
```



## 111

### (issue) 111-Cut1 

```
111-Cut1-before
sockeye - 1.18.106
| +- mxnet-mkl(version range:==1.4.1)
| | +- numpy(version range:<1.15.0,>=1.8.2)
| +- numpy(version range:>=1.14)
```



```
111-Cut1-after
sockeye - 1.18.106
| +- mxnet-mkl(version range:==1.4.1)
| | +- numpy(version range:<1.15.0,>=1.8.2)
| +- numpy(version range:>=1.14)
```





## 114 

### 114-Cut1 

```
114-Cut1-before
target-datadotworld - 1.0.1
| +- backoff(version range:<2.0a,>=1.3.0)
| +- singer-python(version range:>=5.0.4,<=5.6.1)
| | +- backoff(version range:==1.3.2)
```



```
114-Cut1-after
target-datadotworld - 1.0.1
| +- backoff(version range:<2.0a,>=1.3.0)
| +- singer-python(version range:>=5.0.3,<=5.6.1)
| | +- backoff(version range:>=1.3.0,<=1.3.2)
```



### (issue) 114-Cut2 


```
114-Cut2-before
target-datadotworld - 1.0.1
| +- backoff(version range:<2.0a,>=1.3.0)
| +- singer-python(version range:>=5.7.0,<=5.13.0)
| | +- backoff(version range:==1.8.0)
```




```
114-Cut2-after
target-datadotworld - 1.0.1
| +- backoff(version range:<2.0a,>=1.3.0)
| +- singer-python(version range:>=5.7.0,<=5.13.0)
| | +- backoff(version range:>=1.8.0,<=1.9.2)
```



## 116



```
116-Cut0
television - 0.1.1
| +- django(version range:>=1.11, <=2.2.28)
| | +- no dependency on asgiref
| +- channels(version range:==1.1.8)
| | +- asgiref(version range:~=1.1)
```



### 116-Cut1 

```
116-Cut1-before
television - 0.1.1
| +- django(version range:>=3.0a1,<=3.0rc1)
| | +- asgiref(version range:*)
| +- channels(version range:==1.1.8)
| | +- asgiref(version range:~=1.1)
```



```
116-Cut1-after
television - 0.1.1
| +- no call to django, the dependency can be removed
| +- no call to channels, the dependency can be removed
```



### (issue) 116-Cut2 

```
116-Cut2-before
television - 0.1.1
| +- django(version range:>=3.0, <=3.0.14)
| | +- asgiref(version range:~=3.2)
| +- channels(version range:==1.1.8)
| | +- asgiref(version range:~=1.1)
```



```
116-Cut2-after
television - 0.1.1
| +- no call to django, the dependency can be removed
| +- no call to channels, the dependency can be removed
```



### 116-Cut3 

```
116-Cut3-before
television - 0.1.1
| +- django(version range:>=3.1a1,<=3.1b1)
| | +- asgiref(version range:>=3.2)
| +- channels(version range:==1.1.8)
| | +- asgiref(version range:~=1.1)
```



```
116-Cut3-after
television - 0.1.1
| +- no call to django, the dependency can be removed
| +- no call to channels, the dependency can be removed
```



### 116-Cut4 

```
116-Cut4-before
television - 0.1.1
| +- django(version range:>=3.1rc1,<=3.1.2)
| | +- asgiref(version range:~=3.2.10)
| +- channels(version range:==1.1.8)
| | +- asgiref(version range:~=1.1)
```



```
116-Cut4-after
television - 0.1.1
| +- no call to django, the dependency can be removed
| +- no call to channels, the dependency can be removed
```



### 116-Cut5 

```
116-Cut5-before
television - 0.1.1
| +- django(version range:>=3.1.3,<=3.1.14)
| | +- asgiref(version range:<4,>=3.2.10)
| +- channels(version range:==1.1.8)
| | +- asgiref(version range:~=1.1)
```



```
116-Cut5-after
television - 0.1.1
| +- no call to django, the dependency can be removed
| +- no call to channels, the dependency can be removed
```



### 116-Cut6 

```
116-Cut6-before
television - 0.1.1
| +- django(version range:>=3.2a1,<=3.2rc1)
| | +- asgiref(version range:>=3.2.10)
| +- channels(version range:==1.1.8)
| | +- asgiref(version range:~=1.1)
```



```
116-Cut6-after
television - 0.1.1
| +- no call to django, the dependency can be removed
| +- no call to channels, the dependency can be removed
```



### 116-Cut7 

```
116-Cut7-before
television - 0.1.1
| +- django(version range:>=3.2,<=3.2.16)
| | +- asgiref(version range:<4,>=3.3.2)
| +- channels(version range:==1.1.8)
| | +- asgiref(version range:~=1.1)
```



```
116-Cut7-after
television - 0.1.1
| +- no call to django, the dependency can be removed
| +- no call to channels, the dependency can be removed
```



### 116-Cut8 

```
116-Cut8-before
television - 0.1.1
| +- django(version range:>=4.0a1,<=4.0rc1)
| | +- asgiref(version range:>=3.3.2)
| +- channels(version range:==1.1.8)
| | +- asgiref(version range:~=1.1)
```



```
116-Cut8-after
television - 0.1.1
| +- no call to django, the dependency can be removed
| +- no call to channels, the dependency can be removed
```



### 116-Cut9 

```
116-Cut9-before
television - 0.1.1
| +- django(version range:>=4.0,<=4.0.8)
| | +- asgiref(version range:<4,>=3.4.1)
| +- channels(version range:==1.1.8)
| | +- asgiref(version range:~=1.1)
```



```
116-Cut9-after
television - 0.1.1
| +- no call to django, the dependency can be removed
| +- no call to channels, the dependency can be removed
```



### 116-Cut10 

```
116-Cut10-before
television - 0.1.1
| +- django(version range:==4.0a1)
| | +- asgiref(version range:>=3.4.1)
| +- channels(version range:==1.1.8)
| | +- asgiref(version range:~=1.1)
```



```
116-Cut10-after
television - 0.1.1
| +- no call to django, the dependency can be removed
| +- no call to channels, the dependency can be removed
```



### 116-Cut11 

```
116-Cut11-before
television - 0.1.1
| +- django(version range:>=3.0a1,<=3.0rc1)
| | +- asgiref(version range:<4,>=3.5.2)
| +- channels(version range:==1.1.8)
| | +- asgiref(version range:~=1.1)
```



```
116-Cut11-after
television - 0.1.1
| +- no call to django, the dependency can be removed
| +- no call to channels, the dependency can be removed
```









## 117

### 117-Cut1 

```
117-Cut1-before
textxls - 1.0.1
| +- arpeggio(version range:==1.7)
| +- textx(version range:>=0.1.1, <1.8.0)
| | +- arpeggio(version range:*)
```



```
117-Cut1-after
textxls - 1.0.1
| +- arpeggio(version range:>=1.7, <=1.7.1)
| +- textx(version range:>=0.1.1, <1.8.0)
| | +- arpeggio(version range:*) 
```





### (issue) 117-Cut2 

```
117-Cut2-before
textxls - 1.0.1
| +- arpeggio(version range:==1.7)
| +- textx(version range:>=1.8.0, <3)
| | +- arpeggio(version range:>=1.9.0)
```



```
117-Cut2-after
textxls - 1.0.1
| +- arpeggio(version range:>=1.7, <=1.7.1)
| +- textx(version range:>=1.8.0, <3)
| | +- arpeggio(version range:>=1.8.0)
```





### 117-Cut3 

```
117-Cut3-before
textxls - 1.0.1
| +- arpeggio(version range:==1.7)
| +- textx(version range:==3.0.0)
| | +- arpeggio(version range:>=2.0.0)
```



```
117-Cut3-after
textxls - 1.0.1
| +- arpeggio(version range:>=1.7, <=1.7.1)
| +- textx(version range:==3.0.0)
| | +- arpeggio(version range:>=1.10.0)
```



## 118

### (issue) 118-Cut1 

```
118-Cut1-before
twitter-markov - 0.5.1
| +- pyyaml(version range:*)
| +- twitter-bot-utils(version range:<0.12,>=0.11.6.post1)
| | +- pyyaml(version range:==3.11)
```



```
118-Cut1-after
twitter-markov - 0.5.1
| +- no call to pyyaml, the dependency can be removed
| +- twitter-bot-utils(version range:<0.12,>=0.11.6.post1)
| | +- pyyaml(version range:>=3.10, <=3.13)
```



## 120



```
120-Cut0
django-glitter - 0.2.10
| +- django(version range:<1.10,>=1.8)
| +- django-mptt(version range:(>=0.8.5,<=0.9.0) U (>=0.13.0,<=0.14.0))
| | +- no dependency on django
```



### 120-Cut1 

```
120-Cut1-before
django-glitter - 0.2.10
| +- django(version range:<1.10,>=1.8)
| +- django-mptt(version range:>=0.7,<=0.7.4)
| | +- django(version range:>=1.4.2) 
```



```
120-Cut1-after
django-glitter - 0.2.10
| +- django(version range:<1.10,>=1.8)
| +- django-mptt(version range:>=0.7,<=0.7.4)
| | +- django(version range:>=1.4.2) 
```





### 120-Cut2 

```
120-Cut2-before
django-glitter - 0.2.10
| +- django(version range:<1.10,>=1.8)
| +- django-mptt(version range: >=0.8.0,<0.9.0)
| | +- django(version range:>=1.8) 
```



```
120-Cut2-after
django-glitter - 0.2.10
| +- django(version range:<1.10,>=1.8)
| +- django-mptt(version range: >=0.8.0,<0.9.0)
| | +- django(version range:>=1.8) 
```





### (issue) 120-Cut3 

```
120-Cut3-before
django-glitter - 0.2.10
| +- django(version range:<1.10,>=1.8)
| +- django-mptt(version range:>=0.9.1,<=0.12.0)
| | +- django(version range:>=1.11)
```



```
120-Cut3-after
django-glitter - 0.2.10
| +- django(version range:<1.10,>=1.8)
| +- django-mptt(version range:>=0.9.1,<=0.12.0)
| | +- django(version range:>=1.11)
```





## 121

```
121-Cut0
django-glitter-events - 0.1.7
| +- django-glitter(install version:0.2.10 version range:*)
| | +- django(install version:1.9.13 version range:<1.10,>=1.8)
| +- django-taggit(version range:>=0.21.3, <=0.22.2)
| | +- no dependency on django
```



### 121-Cut1 

```
121-Cut1-before
django-glitter-events - 0.1.7
| +- django-glitter(version range:>=0.1,<=0.1.14)
| | +- django(version range:<1.9,>=1.8)
| +- django-taggit(version range:>=0.23.0,<=1.4.0)
| | +- django(version range:>=1.11)
```



```
121-Cut1-after
django-glitter-events - 0.1.7
| +- django-glitter(version range:>=0.1,<=0.1.14)
| | +- django(version range:<1.9,>=1.8)
| +- django-taggit(version range:>=0.23.0,<=1.4.0)
| | +- django(version range:>=1.11rc1)
```





### 121-Cut2 

```
121-Cut2-before
django-glitter-events - 0.1.7
| +- django-glitter(version range:>=0.1,<=0.1.14)
| | +- django(version range:<1.9,>=1.8)
| +- django-taggit(version range:>=1.5.0,<=2.1.0)
| | +- django(version range:>=2.2) 
```



```
121-Cut2-after
django-glitter-events - 0.1.7
| +- django-glitter(version range:>=0.1,<=0.1.14)
| | +- django(version range:<1.9,>=1.8)
| +- django-taggit(version range:>=1.5.0,<=2.1.0)
| | +- django(version range:>=2.2) 
```



### 121-Cut3 

```
121-Cut3-before
django-glitter-events - 0.1.7
| +- django-glitter(version range:>=0.1,<=0.1.14)
| | +- django(version range:<1.9,>=1.8)
| +- django-taggit(version range:>=3.0.0,<=3.1.0)
| | +- django(version range:>=3.2)
```



```
121-Cut3-after
django-glitter-events - 0.1.7
| +- django-glitter(version range:>=0.1,<=0.1.14)
| | +- django(version range:<1.9,>=1.8)
| +- django-taggit(version range:>=3.0.0,<=3.1.0)
| | +- django(version range:>=3.2)
```







### (issue) 121-Cut4 

```
121-Cut4-before
django-glitter-events - 0.1.7
| +- django-glitter(version range:>=0.2,<=0.2.10)
| | +- django(version range:<1.10,>=1.8)
| +- django-taggit(version range:>=0.23.0,<=1.4.0)
| | +- django(version range:>=1.11)
```



```
121-Cut4-after
django-glitter-events - 0.1.7
| +- django-glitter(version range:>=0.2,<=0.2.10)
| | +- django(version range:<1.10,>=1.8)
| +- django-taggit(version range:>=0.23.0,<=1.4.0)
| | +-  django(version range:>=1.11rc1)
```







### 121-Cut5 

```
121-Cut5-before
django-glitter-events - 0.1.7
| +- django-glitter(version range:>=0.2,<=0.2.10)
| | +- django(version range:<1.10,>=1.8)
| +- django-taggit(version range:>=1.5.0,<=2.1.0)
| | +- django(version range:>=2.2) 
```



```
121-Cut5-after
django-glitter-events - 0.1.7
| +- django-glitter(version range:>=0.2,<=0.2.10)
| | +- django(version range:<1.10,>=1.8)
| +- django-taggit(version range:>=1.5.0,<=2.1.0)
| | +- django(version range:>=2.2) 
```







### 121-Cut6 

```
121-Cut6-before
django-glitter-events - 0.1.7
| +- django-glitter(version range:>=0.2,<=0.2.10)
| | +- django(version range:<1.10,>=1.8)
| +- django-taggit(version range:>=3.0.0,<=3.1.0)
| | +- django(version range:>=3.2)
```



```
121-Cut6-after
django-glitter-events - 0.1.7
| +- django-glitter(version range:>=0.2,<=0.2.10)
| | +- django(version range:<1.10,>=1.8)
| +- django-taggit(version range:>=3.0.0,<=3.1.0)
| | +- django(version range:>=3.2)
```





## 122

```
122-Cut0
django-glitter-news - 0.3.3
| +- django-glitter(install version:0.2.10 version range:*)
| | +- django(install version:1.9.13 version range:<1.10,>=1.8)
| +- django-taggit(version range:>=0.21.3, <=0.22.2)
| | +- no dependency on django
```





### 122-Cut1 

```
122-Cut1-before
django-glitter-news - 0.3.3
| +- django-glitter(version range:>=0.1,<=0.1.14)
| | +- django(version range:<1.9,>=1.8)
| +- django-taggit(version range:>=0.23.0,<=1.4.0)
| | +- django(version range:>=1.11)
```



```
122-Cut1-after
django-glitter-news - 0.3.3
| +- django-glitter(version range:>=0.1,<=0.1.14)
| | +- django(version range:<1.9,>=1.8)
| +- django-taggit(version range:>=0.23.0,<=1.4.0)
| | +- django(version range:>=1.11rc1)
```





### 122-Cut2 

```
122-Cut2-before
django-glitter-news - 0.3.3
| +- django-glitter(version range:>=0.1,<=0.1.14)
| | +- django(version range:<1.9,>=1.8)
| +- django-taggit(version range:>=1.5.0,<=2.1.0)
| | +- django(version range:>=2.2) 
```



```
122-Cut2-after
django-glitter-news - 0.3.3
| +- django-glitter(version range:>=0.1,<=0.1.14)
| | +- django(version range:<1.9,>=1.8)
| +- django-taggit(version range:>=1.5.0,<=2.1.0)
| | +- django(version range:>=2.2) 
```



### 122-Cut3 

```
122-Cut3-before
django-glitter-news - 0.3.3
| +- django-glitter(version range:>=0.1,<=0.1.14)
| | +- django(version range:<1.9,>=1.8)
| +- django-taggit(version range:>=3.0.0,<=3.1.0)
| | +- django(version range:>=3.2)
```



```
122-Cut3-after
django-glitter-news - 0.3.3
| +- django-glitter(version range:>=0.1,<=0.1.14)
| | +- django(version range:<1.9,>=1.8)
| +- django-taggit(version range:>=3.0.0,<=3.1.0)
| | +- django(version range:>=3.2)
```







### (issue) 122-Cut4 

```
122-Cut4-before
django-glitter-news - 0.3.3
| +- django-glitter(version range:>=0.2,<=0.2.10)
| | +- django(version range:<1.10,>=1.8)
| +- django-taggit(version range:>=0.23.0,<=1.4.0)
| | +- django(version range:>=1.11)
```



```
122-Cut4-after
django-glitter-news - 0.3.3
| +- django-glitter(version range:>=0.2,<=0.2.10)
| | +- django(version range:<1.10,>=1.8)
| +- django-taggit(version range:>=0.23.0,<=1.4.0)
| | +-  django(version range:>=1.11rc1)
```







### 122-Cut5 

```
122-Cut5-before
django-glitter-news - 0.3.3
| +- django-glitter(version range:>=0.2,<=0.2.10)
| | +- django(version range:<1.10,>=1.8)
| +- django-taggit(version range:>=1.5.0,<=2.1.0)
| | +- django(version range:>=2.2) 
```



```
122-Cut5-after
django-glitter-news - 0.3.3
| +- django-glitter(version range:>=0.2,<=0.2.10)
| | +- django(version range:<1.10,>=1.8)
| +- django-taggit(version range:>=1.5.0,<=2.1.0)
| | +- django(version range:>=2.2) 
```







### 122-Cut6  

```
122-Cut6-before
django-glitter-news - 0.3.3
| +- django-glitter(version range:>=0.2,<=0.2.10)
| | +- django(version range:<1.10,>=1.8)
| +- django-taggit(version range:>=3.0.0,<=3.1.0)
| | +- django(version range:>=3.2)
```



```
122-Cut6-after
django-glitter-news - 0.3.3
| +- django-glitter(version range:>=0.2,<=0.2.10)
| | +- django(version range:<1.10,>=1.8)
| +- django-taggit(version range:>=3.0.0,<=3.1.0)
| | +- django(version range:>=3.2)
```





## 124

```
124-Cut0
mockerena - 1.2.0
| +- eve(version range:>=1.0,<=2.0.4)
| | +- no dependency on werkzeug
| +- flask(install version:1.1.1 version range:>=1.1.0)
| | +- werkzeug(install version:0.16.0 version range:>=0.15)
```





### 124-Cut1 

```
124-Cut1-before
mockerena - 1.2.0
| +- eve(version range:==0.9.0)
| | +- werkzeug(version range:>=0.15.1)
| +- flask(version range:>=1.1.0,<=1.1.2)
| | +- werkzeug(version range:>=0.15)
```



```
124-Cut1-after
mockerena - 1.2.0
| +- eve(version range:==0.9.0)
| | +- werkzeug(version range:>=0.15.0)
| +- flask(version range:>=1.1.0,<=1.1.2)
| | +- werkzeug(version range:>=0.15)
```





### 124-Cut2 


```
124-Cut2-before
mockerena - 1.2.0
| +- eve(version range:==0.9.0)
| | +- werkzeug(version range:>=0.15.1)
| +- flask(version range:>=2.0.0rc1,<=2.0.0rc2)
| | +- werkzeug(version range:>=2.0.0rc4)
```




```
124-Cut2-after
mockerena - 1.2.0
| +- eve(version range:==0.9.0)
| | +- werkzeug(version range:>=0.15.0)
| +- flask(version range:>=2.0.0rc1,<=2.0.0rc2)
| | +- werkzeug(version range:>=2.0.0rc4)
```



### 124-Cut3 

```
124-Cut3-before
mockerena - 1.2.0
| +- eve(version range::==0.9.0)
| | +- werkzeug(version range:>=0.15.1)
| +- flask(version range:>=2.0.0,<=2.1.3)
| | +- werkzeug(version range:>=2.0)
```



```
124-Cut3-after
mockerena - 1.2.0
| +- eve(version range:==0.9.0)
| | +- werkzeug(version range:>=0.15.0)
| +- flask(version range:>=2.0.0,<=2.1.3)
| | +- werkzeug(version range:>=2.0)
```



### 124-Cut4 

```
124-Cut4-before
mockerena - 1.2.0
| +- eve(version range::==0.9.0)
| | +- werkzeug(version range:>=0.15.1)
| +- flask(version range:>=2.2.0,<=2.2.1)
| | +- werkzeug(version range:>=2.2.0)
```



```
124-Cut4-after
mockerena - 1.2.0
| +- eve(version range::==0.9.0)
| | +- werkzeug(version range:>=0.15.0)
| +- flask(version range:>=2.2.0,<=2.2.1)
| | +- werkzeug(version range:>=2.2.0)
```



### 124-Cut5 

```
124-Cut5-before
mockerena - 1.2.0
| +- eve(version range::==0.9.0)
| | +- werkzeug(version range:>=0.15.1)
| +- flask(version range:==2.2.2)
| | +- werkzeug(version range:>=2.2.2)
```



```
124-Cut5-after
mockerena - 1.2.0
| +- eve(version range::==0.9.0)
| | +- werkzeug(version range:>=0.15.0)
| +- flask(version range:==2.2.2)
| | +- werkzeug(version range:>=2.2.2)
```







### (issue) 124-Cut6 

```
124-Cut6-before
mockerena - 1.2.0
| +- eve(version range:>=0.9.1,<=0.9.2)
| | +- werkzeug(version range:==0.15.4)
| +- flask(version range:>=1.1.0,<=1.1.2)
| | +- werkzeug(version range:>=0.15)
```



```
124-Cut6-after
mockerena - 1.2.0
| +- eve(version range:>=0.9.1,<=0.9.2)
| | +- werkzeug(version range:>=0.15.0,<=0.15.4)
| +- flask(version range:>=1.1.0,<=1.1.2)
| | +- werkzeug(version range:>=0.15)
```



### 124-Cut7 

```
124-Cut7-before
mockerena - 1.2.0
| +- eve(version range:>=0.9.1,<=0.9.2)
| | +- werkzeug(version range:==0.15.4)
| +- flask(version range:>=2.0.0rc1, <=2.0.0rc2)
| | +- werkzeug(version range:>=2.0.0rc4)
```



```
124-Cut7-after
mockerena - 1.2.0
| +- eve(version range:>=0.9.1,<=0.9.2)
| | +- werkzeug(version range:>=0.15.0,<=0.15.4)
| +- flask(version range:>=2.0.0rc1, <=2.0.0rc2)
| | +- werkzeug(version range:>=2.0.0rc4)
```



### 124-Cut8 

```
124-Cut8-before
mockerena - 1.2.0
| +- eve(version range:>=0.9.1,<=0.9.2)
| | +- werkzeug(version range:==0.15.4)
| +- flask(version range:>=2.0.0,<=2.1.3)
| | +- werkzeug(version range:>=2.0)
```



```
124-Cut8-after
mockerena - 1.2.0
| +- eve(version range:>=0.9.1,<=0.9.2)
| | +- werkzeug(version range:>=0.15.0,<=0.15.4)
| +- flask(version range:>=2.0.0,<=2.1.3)
| | +- werkzeug(version range:>=2.0)
```



### 124-Cut9 

```
124-Cut9-before
mockerena - 1.2.0
| +- eve(version range:>=0.9.1,<=0.9.2)
| | +- werkzeug(version range:==0.15.4)
| +- flask(version range:>=2.2.0,<=2.2.1)
| | +- werkzeug(version range:>=2.2.0)
```



```
124-Cut9-after
mockerena - 1.2.0
| +- eve(version range:>=0.9.1,<=0.9.2)
| | +- werkzeug(version range:>=0.15.0,<=0.15.4)
| +- flask(version range:>=2.2.0,<=2.2.1)
| | +- werkzeug(version range:>=2.2.0)
```





### 124-Cut10 

```
124-Cut10-before
mockerena - 1.2.0
| +- eve(version range:>=0.9.1,<=0.9.2)
| | +- werkzeug(version range:==0.15.4)
| +- flask(version range:==2.2.2)
| | +- werkzeug(version range:>=2.2.2)
```



```
124-Cut10-after
mockerena - 1.2.0
| +- eve(version range:>=0.9.1,<=0.9.2)
| | +- werkzeug(version range:>=0.15.0,<=0.15.4)
| +- flask(version range:==2.2.2)
| | +- werkzeug(version range:>=2.2.2)
```





## 125



```
125-Cut0
nornir - 2.3.0
| +- junos-eznc(version range:>=2.2,<3.0)
| +- napalm(version range:>=2.0.0, <=2.1.0)
| | +- no dependency on junos-eznc
```





### 125-Cut1 


```
125-Cut1-before
nornir - 2.3.0
| +- junos-eznc(version range:>=2.2,<3.0)
| +- napalm(version range:>=2.2.0,<=2.3.3)
| | +- junos-eznc(version range:>=2.1.5)
```




```
125-Cut1-after
nornir - 2.3.0
| +- no call to junos-eznc, the dependency can be removed
| +- napalm(version range:>=2.2.0,<=2.3.3)
| | +- junos-eznc(version range:>=2.1.5)
```



### 125-Cut2 

```
125-Cut2-before
nornir - 2.3.0
| +- junos-eznc(version range:>=2.2,<3.0)
| +- napalm(version range:==2.4.0)
| | +- junos-eznc(version range:>=2.2.0)
```



```
125-Cut2-after
nornir - 2.3.0
| +- no call to junos-eznc, the dependency can be removed
| +- napalm(version range:==2.4.0)
| | +- junos-eznc(version range:>=2.2.0)
```



### (issue) 125-Cut3 

```
125-Cut3-before
nornir - 2.3.0
| +- junos-eznc(version range:>=2.2,<3.0)
| +- napalm(version range:==2.5.0)
| | +- junos-eznc(version range:==2.2.1)
```



```
125-Cut3-after
nornir - 2.3.0
| +- no call to junos-eznc, the dependency can be removed
| +- napalm(version range:==2.5.0)
| | +- junos-eznc(version range:==2.2.1)
```





## 128



### (issue) 128-Cut1 

```
128-Cut1-before
reana-cluster - 0.5.0
| +- kubernetes(version range:==9.0.1 U (>=10.0.1,<=25.3.0))
| | +- urllib3(version range:>=1.24.2)
| +- urllib3(version range:==1.24.1)
```



```
128-Cut1-after
reana-cluster - 0.5.0
| +- kubernetes(version range:==9.0.1 U (>=10.0.1,<=25.3.0))
| | +- urllib3(version range:>=1.21)
| +- no call to urllib3, the dependency can be removed
```





### 128-Cut2 


```
128-Cut2-before
reana-cluster - 0.5.0
| +- kubernetes(version range:9.0.0, 10.0.0a1, 10.0.0)
| | +-  urllib3(version range:>=1.23)
| +- urllib3(version range:==1.24.1)
```




```
128-Cut2-after
reana-cluster - 0.5.0
| +- kubernetes(version range:9.0.0, 10.0.0a1, 10.0.0)
| | +- urllib3(version range:>=1.21)
| +- no call to urllib3, the dependency can be removed
```





## 130

### 130-Cut1 

```
130-Cut1-before
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range:>=0.0.6,<=0.1.0)
| | +- openpyxl(version range:==2.2.2)
```



```
130-Cut1-after
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range:>=0.0.6,<=0.1.0)
| | +- openpyxl(version range:>=2.2.1,<=2.2.2)
```





### 130-Cut2 


```
130-Cut2-before
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range:>=0.2.0,<=0.3.0)
| | +- openpyxl(version range:>=2.2.2)
```




```
130-Cut2-after
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range:>=0.2.0,<=0.3.0)
| | +- openpyxl(version range:>=2.2.1)
```



### 130-Cut3 

```
130-Cut3-before
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range:>=0.4.0,<=0.5.5)
| | +- openpyxl(version range:>=2.4.4)
```



```
130-Cut3-after
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range:>=0.4.0,<=0.5.5)
| | +- openpyxl(version range:>=2.4.4)
```





### 130-Cut4 

```
130-Cut4-before
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range:==0.5.6)
| | +- openpyxl(version range:>=2.5.0)
```



```
130-Cut4-after
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range:==0.5.6)
| | +- openpyxl(version range:>=2.5.0)
```



### (issue) 130-Cut5 

```
130-Cut5-before
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range: ==0.5.7)
| | +- openpyxl(version range:>=2.5.0,<2.6.0)
```



```
130-Cut5-after
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range: ==0.5.7)
| | +- openpyxl(version range:>=2.5.0,<2.6.0)
```



### 130-Cut6 

```
130-Cut6-before
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range:>=0.5.8,<=0.6.0)
| | +- openpyxl(version range:>=2.6.1)
```




```
130-Cut6-after
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range:>=0.5.8,<=0.6.0)
| | +- openpyxl(version range:>=2.6.1)
```



### 130-Cut7 

```
130-Cut7-before
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range:>=0.0.1,<=0.0.5)
| | +- openpyxl(version range:*)
```




```
130-Cut7-after
Spartacus - 3.36
| +- openpyxl(version range:*)
| +- pyexcel-xlsx(version range:>=0.0.1,<=0.0.5)
| | +- openpyxl(version range:*)
```









## 131 



### 131-Cut1 

```
131-Cut1-before
ssmash - 2.0.1
| +- flying-circus(version range:>=0.7.0,<=0.7.1)
| | +- pyyaml(version range:==5.1.1)
| +- pyyaml(version range:>=5.1,<6)
```



```
131-Cut1-after
ssmash - 2.0.1
| +- flying-circus(version range:>=0.7.0,<=0.7.1)
| | +- pyyaml(version range:>=5.1, <=5.3.1)
| +- pyyaml(version range:>=5.1,<6)
```



### (issue) 131-Cut2 


```
131-Cut2-before
ssmash - 2.0.1
| +- flying-circus(version range:>=0.7.2,<=0.7.3)
| | +- pyyaml(version range:<5.2.0,>=5.1.1)
| +- pyyaml(version range:>=5.1,<6)
```




```
131-Cut2-after
ssmash - 2.0.1
| +- flying-circus(version range:>=0.7.2,<=0.7.3)
| | +- pyyaml(version range:>=5.1, <=5.3.1)
| +- pyyaml(version range:>=5.1,<6)
```



## 133



### (issue) 133-Cut1 

```
133-Cut1-before
TMO4CT - 0.6
| +- dcm2hdr(version range:>=1.0.2,<=1.1.0)
| | +- tifffile(version range: >=0.14.0,<1.0)
| +- tifffile(version range:*)
```



```
133-Cut1-after
TMO4CT - 0.6
| +- no call to dcm2hdr, the dependency can be removed
| +- tifffile(version range:*)
```



### 133-Cut2 

```
133-Cut2-before
TMO4CT - 0.6
| +- dcm2hdr(version range:==1.1.1)
| | +- tifffile(version range: >=0.14.0)
| +- tifffile(version range:*)
```



```
133-Cut2-after
TMO4CT - 0.6
| +- dcm2hdr(version range:==1.1.1)
| +- no call to dcm2hdr, the dependency can be removed
| +- tifffile(version range:*)
```







## 257

```
257-Cut0
bakerydemo-master
| +-aws-requests-auth(version range:==0.4.0)
| | +-requests(version range:>=0.14.0,<=2.15.1)
| | | +- no dependency on urllib3
| +-elasticsearch(version range:==2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```



### 257-Cut1 

```
257-Cut1-before
bakerydemo-master
| +-aws-requests-auth(version range:==0.4.0)
| | +-requests(version range:>=2.16.0,<=2.18.1)
| | | +- urllib3(version range:<1.22,>=1.21.1)
| +-elasticsearch(version range:==2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```



```
257-Cut1-after
bakerydemo-master
| +-aws-requests-auth(version range:>=0.4.0, <=0.4.3)
| | +-requests(version range:>=2.16.0,<=2.18.1) 
| | | +- urllib3(version range:<1.22,>=1.21)
| +-elasticsearch(version range:>=2.4.0,<=2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```





### 257-Cut2 

```
257-Cut2-before
bakerydemo-master
| +-aws-requests-auth(version range:==0.4.0)
| | +-requests(version range:>=2.18.2, <=2.18.4)
| | | +- urllib3(version range:<1.23,>=1.21.1)
| +-elasticsearch(version range:==2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```



```
257-Cut2-after
bakerydemo-master
| +-aws-requests-auth(version range:>=0.4.0, <=0.4.3) 
| | +-requests(version range:>=2.18.2, <=2.18.4) 
| | | +- urllib3(version range:<1.23,>=1.21) 
| +-elasticsearch(version range:>=2.4.0,<=2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```



### 257-Cut3 

```
257-Cut3-before
bakerydemo-master
| +-aws-requests-auth(version range:==0.4.0)
| | +-requests(version range:>=2.19.0,<=2.19.1)
| | | +- urllib3(version range:<1.24,>=1.21.1)
| +-elasticsearch(version range:==2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```



```
257-Cut3-after
bakerydemo-master
| +-aws-requests-auth(version range:>=0.4.0, <=0.4.3) 
| | +-requests(version range:>=2.19.0,<=2.19.1)
| | | +- urllib3(version range:<1.24,>=1.21)
| +-elasticsearch(version range:>=2.4.0,<=2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```





### 257-Cut4 

```
257-Cut4-before
bakerydemo-master
| +-aws-requests-auth(version range:==0.4.0)
| | +-requests(version range:>=2.20.0, <=2.21.0)
| | | +- urllib3(version range:<1.25,>=1.21.1)
| +-elasticsearch(version range:==2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```



```
257-Cut4-after
bakerydemo-master
| +-aws-requests-auth(version range:>=0.4.0, <=0.4.3)
| | +-requests(version range:>=2.20.0, <=2.21.0) 
| | | +- urllib3(version range:<1.25,>=1.21)
| +-elasticsearch(version range:>=2.4.0,<=2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```





### (issue) 257-Cut5 

```
257-Cut5-before
bakerydemo-master
| +-aws-requests-auth(version range:==0.4.0)
| | +-requests(version range:>=2.22.0, <=2.24.0)
| | | +- urllib3(version range:<1.26,>=1.21.1)
| +-elasticsearch(version range:==2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```



```
257-Cut5-after
bakerydemo-master
| +-aws-requests-auth(version range:>=0.4.0, <=0.4.3) 
| | +-requests(version range:>=2.22.0, <=2.24.0) 
| | | +- urllib3(version range:<1.26,>=1.21) 
| +-elasticsearch(version range:>=2.4.0,<=2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```



### 257-Cut6 

```
257-Cut6-before
bakerydemo-master
| +-aws-requests-auth(version range:==0.4.0)
| | +-requests(version range:>=2.25.0,<=2.28.1) 
| | | +- urllib3(version range:<1.27,>=1.21.1)
| +-elasticsearch(version range:==2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```



```
257-Cut6-after
bakerydemo-master
| +-aws-requests-auth(version range:>=0.4.0, <=0.4.3) 
| | +-requests(version range:>=2.25.0,<=2.28.1) 
| | | +- urllib3(version range:<1.27,>=1.21) 
| +-elasticsearch(version range:>=2.4.0,<=2.4.1)
| | +-urllib3(version range:>=1.8,<2.0)
```



## 260

### (issue) 260-Cut1 

```
260-Cut1-before
osmedeus-1.4
| +-flask-jwt(version range:==0.3.2)
| | +-pyjwt(version range:>=1.4.0,<1.5.0)
| +-flask-jwt-extended(version range:==3.18.1)
| | +-pyjwt(version range:>=1.6.4)
```



```
260-Cut1-after
osmedeus-1.4
| +-no call to flask-jwt, the dependency can be removed
| +-flask-jwt-extended(version range:>=3.18.1,<=3.18.2)
| | +-pyjwt(version range:>=1.6.4)
```





## 261



### 261-Cut1 

```
261-Cut1-before
dork-compose - 1.13.0.0.0.1
| +- docker-compose(version range:==1.13.0)
| | +- requests(version range:>=2.6.1,<2.12)
| +- hvac(version range:>=0.0.1,<=0.2.5)
| | +- requests(version range:*)
```



```
261-Cut1-after
dork-compose - 1.13.0.0.0.1
| +- docker-compose(version range:{1.13.0, 1.13.0rc1}) 
| | +- requests(version range:>=2.3.0, <=2.27.1) 
| +- hvac(version range:>=0.0.1,<=0.2.5)
| | +-requests(version range:*) 
```





### 261-Cut2 

```
261-Cut2-before
dork-compose - 1.13.0.0.0.1
| +- docker-compose( version range:==1.13.0)
| | +- requests(version range:>=2.6.1,<2.12)
| +- hvac(version range:>=0.2.6,<=0.7.1)
| | +- requests(version range:>=2.7.0) 
```



```
261-Cut2-after
dork-compose - 1.13.0.0.0.1
| +- docker-compose(version range:<=1.13.0,>=1.13.0rc1) 
| | +- requests(version range:>=2.3.0, <=2.27.1) 
| +- hvac(version range:>=0.2.6,<=0.7.1)
| | +- requests(version range:>=2.7.0)
```





### (issue) 261-Cut3 

```
261-Cut3-before
dork-compose - 1.13.0.0.0.1
| +- docker-compose(version range:==1.13.0)
| | +- requests(version range:>=2.6.1,<2.12)
| +- hvac(version range:>=0.7.2,<=0.11.2,!=0.11.1)
| | +- requests(version range:>=2.21.0)
```



```
261-Cut3-after
dork-compose - 1.13.0.0.0.1
| +- docker-compose(version range:<=1.13.0,>=1.13.0rc1) 
| | +- requests(version range:>=2.3.0, <=2.27.1) 
| +- hvac(version range:>=0.7.2,<=0.11.2,!=0.11.1)
| | +- requests(version range:>=2.21.0)
```





### 261-Cut4 

```
261-Cut4-before
dork-compose - 1.13.0.0.0.1
| +- docker-compose(ersion range:==1.13.0)
| | +- requests(version range:>=2.6.1,<2.12)
| +- hvac(version range:==0.11.1)
| | +- requests(version range:>=2.25.1)
```



```
261-Cut4-after
dork-compose - 1.13.0.0.0.1
| +- docker-compose(version range:<=1.13.0,>=1.13.0rc1) 
| | +- requests(version range:>=2.3.0, <=2.27.1) 
| +- hvac(version range:==0.11.1)
| | +- requests(version range:>=2.25.1)
```





### 261-Cut5 

```
261-Cut5-before
dork-compose - 1.13.0.0.0.1
| +- docker-compose(version range:==1.13.0)
| | +- requests(version range:>=2.6.1,<2.12)
| +- hvac(version range:>=1.0.0,<=1.0.1)
| | +- requests(version range:==2.27.1)
```



```
261-Cut5-after
dork-compose - 1.13.0.0.0.1
| +- docker-compose(version range:<=1.13.0,>=1.13.0rc1) 
| | +- requests(version range:>=2.3.0, <=2.27.1)
| +- hvac(version range:>=1.0.0,<=1.0.1)
| | +- requests(version range:==2.27.1)
```



### 261-Cut6 

```
261-Cut6-before
dork-compose - 1.13.0.0.0.1
| +- docker-compose(version range:==1.13.0)
| | +- requests(version range:>=2.6.1,<2.12)
| +- hvac(version range:==1.0.2)
| | +- requests(version range:>=2.27.1,<3.0.0)
```



```
261-Cut6-after
dork-compose - 1.13.0.0.0.1
| +- docker-compose(version range:<=1.13.0,>=1.13.0rc1) 
| | +- requests(version range:>=2.3.0, <=2.27.1)
| +- hvac(version range:==1.0.2)
| | +- requests(version range:>=2.27.1,<3.0.0)
```



## 266



### (issue) 266-Cut1 

```
266-Cut1-before
pymacaron 1.0.213
| +- pymacaron-core(version range:>=1.0.146, <=1.0.171)
| | +- PyYAML(version range:==5.1.2)
| +- PyYAML(version range:>=5.1.2)
```



```
266-Cut1-after
pymacaron 1.0.213
| +- pymacaron-core(version range:>=1.0.146, <=1.0.171)
| | +- PyYAML(version range:>=5.1, <5.3.1)
| +- PyYAML(version range:>=5.1) 
```



### 266-Cut2 

```
266-Cut2-before
pymacaron 1.0.213
| +- pymacaron-core(version range:>=1.0.172,<=1.0.174)
| | +- PyYAML(version range:>=5.1.2)
| +- PyYAML(version range:>=5.1.2)
```



```
266-Cut2-after
pymacaron 1.0.213
| +- pymacaron-core(version range:>=1.0.172,<=1.0.174)
| | +- PyYAML(version range:>=5.1) 
| +- PyYAML(version range:>=5.1) 
```





## 270



```
270-Cut0
scriptax-jupyter-kernel - 0.1.3
| +- jupyter-client(version range:>=4.0.0, <5.0.0)
| | +-  no dependency on python-dateutil
| +- scriptax-runtime(version range:==0.2.1)
| | +- apitaxcore(version range:==3.0.9)
| | | +- python-dateutil(version range:==2.6.0)
```





### (issue) 270-Cut1 

```
270-Cut1-before
scriptax-jupyter-kernel - 0.1.3
| +- jupyter-client(version range:>=5.0.0, <=7.2.0)
| | +-  python-dateutil(version range:>=2.1）
| +- scriptax-runtime(version range:==0.2.1)
| | +- apitaxcore(version range:==3.0.9)
| | | +- python-dateutil(version range:==2.6.0)
```



```
270-Cut1-after
scriptax-jupyter-kernel - 0.1.3
| +- jupyter-client(version range:>=5.0.0, <=7.2.0)
| | +-  python-dateutil(version range:>=2.1）
| +- scriptax-runtime(version range:==0.2.1)
| | +- apitaxcore(version range:>=3.0.6,<=3.0.9)
| | | +- no call to python-dateutil, the dependency can be removed
```





### 270-Cut2 

```
270-Cut2-before
scriptax-jupyter-kernel - 0.1.3
| +- jupyter-client(version range:>=7.2.1,<=8.0.0rc0)
| | +- python-dateutil(version range:>=2.8.2)
| +- scriptax-runtime(version range:==0.2.1)
| | +- apitaxcore(version range:==3.0.9)
| | | +- python-dateutil(version range:==2.6.0)
```



```
270-Cut2-after
scriptax-jupyter-kernel - 0.1.3
| +- jupyter-client(version range:>=7.2.1,<=8.0.0rc0)
| | +- python-dateutil(version range:>=2.8.2)
| +- scriptax-runtime(version range:==0.2.1)
| | +- apitaxcore(version range:>=3.0.6,<=3.0.9)
| | | +- no call to python-dateutil, the dependency can be removed
```



## 271

```
271-Cut0
1a23-telemetry - 1.0.0 
| +- requests(version range:>=0.2.0,<=2.15.1)
| | +- no dependency on urllib3
| +- sentry-sdk(version range:==0.6.9)
| | +- urllib3(version range:*)
```





### 271-Cut1 

```
271-Cut1-before
1a23-telemetry - 1.0.0 
| +- requests(version range:>=2.16.0, <=2.18.1)
| | +- urllib3(version range:<1.22,>=1.21.1)
| +- sentry-sdk(version range:==0.6.9)
| | +- urllib3(version range:*)
```



```
271-Cut1-after
1a23-telemetry - 1.0.0 
| +- requests(version range:>=2.16.0, <=2.18.1)
| | +- urllib3(version range:<1.22,>=1.21)
| +- sentry-sdk(version range:>=0.6.5, <=0.7.3)
| | +- urllib3(version range:*)
```





### 271-Cut2 

```
271-Cut2-before
1a23-telemetry - 1.0.0 
| +- requests(version range:>=2.18.2, <=2.18.4)
| | +- urllib3(version range:<1.23,>=1.21.1)
| +- sentry-sdk(version range:==0.6.9)
| | +- urllib3(version range:*)
```



```
271-Cut2-after
1a23-telemetry - 1.0.0 
| +- requests(version range:>=2.18.2, <=2.18.4)
| | +- urllib3(version range:<1.23,>=1.21) 
| +- sentry-sdk(version range:>=0.6.5, <=0.7.3)
| | +- urllib3(version range:*)
```





### 271-Cut3 

```
271-Cut3-before
1a23-telemetry - 1.0.0 
| +- requests(version range:>=2.19.0, <=2.19.1)
| | +- urllib3(version range:<1.24,>=1.21.1)
| +- sentry-sdk(version range:==0.6.9)
| | +- urllib3(version range:*)
```



```
271-Cut3-after
1a23-telemetry - 1.0.0 
| +- requests(version range:>=2.19.0, <=2.19.1)
| | +- urllib3(version range:<1.24,>=1.21) 
| +- sentry-sdk(version range:>=0.6.5, <=0.7.3)
| | +- urllib3(version range:*)
```





### 271-Cut4 

```
271-Cut4-before
1a23-telemetry - 1.0.0 
| +- requests(version range:>=2.20.0, <=2.21.0)
| | +- urllib3(version range:<1.25,>=1.21.1)
| +- sentry-sdk(version range:==0.6.9)
| | +- urllib3(version range:*)
```



```
271-Cut4-after
1a23-telemetry - 1.0.0 
| +- requests(version range:s>=2.20.0, <=2.21.0)
| | +- urllib3(version range:<1.25,>=1.21)
| +- sentry-sdk(version range:>=0.6.5, <=0.7.3)
| | +- urllib3(version range:*)
```





### (issue) 271-Cut5 

```
271-Cut5-before
1a23-telemetry - 1.0.0 
| +- requests(version range:>=2.22.0, <=2.24.0)
| | +- urllib3(version range:<1.26,>=1.21.1)
| +- sentry-sdk(version range:==0.6.9)
| | +- urllib3(version range:*)
```



```
271-Cut5-after
1a23-telemetry - 1.0.0 
| +- requests(version range:>=2.22.0, <=2.24.0)
| | +- urllib3(version range:<1.26,>=1.21) 
| +- sentry-sdk(version range:>=0.6.5, <=0.7.3) 
| | +- urllib3(version range:*)
```





### 271-Cut6 

```
271-Cut6-before
1a23-telemetry - 1.0.0 
| +- requests(version range:>=2.25.0)
| | +- urllib3(version range:<1.27,>=1.21.1)
| +- sentry-sdk(version range:==0.6.9)
| | +- urllib3(version range:*)
```



```
271-Cut6-after
1a23-telemetry - 1.0.0 
| +- requests(version range:>=2.25.0)
| | +- urllib3(version range:<1.27,>=1.21) 
| +- sentry-sdk(version range:>=0.6.5,<=0.7.3)
| | +- urllib3(version range:*)
```





## 272



### 272-Cut1 

```
272-Cut1-before
grimoire-elk 0.63.0
| +- kingarthur(version range:>=0.1.1,<=0.1.12)
| | +- redis(version range:>=2.10.0)
| +- redis(version range:<=2.10.6,>=2.10.0)
```



```
272-Cut1-after
grimoire-elk 0.63.0
| +- kingarthur(version range:>=0.1.1,<=0.1.12)
| | +- redis(version range:>=0.6.0, <=4.3.1)
| +- redis(version range:<=2.10.6,>=2.10.0)
```





### 272-Cut2 


```
272-Cut2-before
grimoire-elk 0.63.0
| +- kingarthur(version range:>=0.1.14,<=0.1.15)
| | +- redis(version range:>=2.10.0, <=2.10.6)
| +- redis(version range:<=2.10.6,>=2.10.0)
```




```
272-Cut2-after
grimoire-elk 0.63.0
| +- kingarthur(version range:>=0.1.14,<=0.1.15)
| | +- redis(version range:>=0.6.0, <=4.3.1)
| +- redis(version range:<=2.10.6,>=2.10.0)
```





### (issue) 272-Cut3 


```
272-Cut3-before
grimoire-elk 0.63.0
| +- kingarthur(version range:>=0.1.17,<=0.2.5)
| | +- redis(version range:==3.0.0)
| +- redis(version range:<=2.10.6,>=2.10.0)
```




```
272-Cut3-after
grimoire-elk 0.63.0
| +- kingarthur(version range:>=0.1.17,<=0.2.5)
| | +- redis(version range:>=0.6.0, <=4.3.1)
| +- redis(version range:<=2.10.6,>=2.10.0)
```



## 278



### 278-Cut1 

```
278-Cut1-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.18.0, <=2.18.1)
| | +- urllib3(version range:<1.22,>=1.21.1)
| +- transifex-client(version range:>=0.13,<=0.13.4)
| | +- urllib3(version range:*)
```



```
278-Cut1-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.16.0, <=2.18.1)
| | +- urllib3(version range:<1.22,>=1.21)
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut2 

```
278-Cut2-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.18.2, <=2.18.4)
| | +- urllib3(version range:<1.23,>=1.21.1)
| +- transifex-client(version range:>=0.13,<=0.13.4)
| | +- urllib3(version range:*)
```



```
278-Cut2-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.18.2, <=2.18.4)
| | +- urllib3(version range:<1.23,>=1.21) 
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut3 

```
278-Cut3-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.19.0,<=2.19.1)
| | +- urllib3(version range:<1.24,>=1.21.1)
| +- transifex-client(version range:>=0.13,<=0.13.4)
| | +- urllib3(version range:*)
```



```
278-Cut3-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.19.0,<=2.19.1)
| | +- urllib3(version range:<1.24,>=1.21) 
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut4 

```
278-Cut4-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.20.0, <=2.21.0)
| | +- urllib3(version range:<1.25,>=1.21.1)
| +- transifex-client(version range:>=0.13,<=0.13.4)
| | +- urllib3(version range:*)
```



```
278-Cut4-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.20.0, <=2.21.0)
| | +- urllib3(version range:<1.25,>=1.21) 
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut5 

```
278-Cut5-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.22.0, <=2.24.0)
| | +- urllib3(version range:<1.26,>=1.21.1)
| +- transifex-client(version range:>=0.13,<=0.13.4)
| | +- urllib3(version range:*)
```



```
278-Cut5-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.22.0, <=2.24.0)
| | +- urllib3(version range:<1.26,>=1.21)
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut6 

```
278-Cut6-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.25.0,<=2.28.1)
| | +- urllib3(version range:<1.27,>=1.21.1)
| +- transifex-client(version range:>=0.13,<=0.13.4)
| | +- urllib3(version range:*)
```



```
278-Cut6-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.25.0,<=2.28.1)
| | +- urllib3(version range:<1.27,>=1.21)
| +- no call to transifex-client, the dependency can be removed
```





### 278-Cut7 

```
278-Cut7-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.18.0, <=2.18.1)
| | +- urllib3(version range:<1.22,>=1.21.1)
| +- transifex-client(version range:>=0.13.5, <=0.13.6)
| | +- urllib3(version range:<1.24)
```



```
278-Cut7-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.16.0, <=2.18.1)
| | +- urllib3(version range:<1.22,>=1.21)
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut8 

```
278-Cut8-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.18.2, <=2.18.4)
| | +- urllib3(version range:<1.23,>=1.21.1)
| +- transifex-client(version range:>=0.13.5, <=0.13.6)
| | +- urllib3(version range:<1.24)
```



```
278-Cut8-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.18.2, <=2.18.4)
| | +- urllib3(version range:<1.23,>=1.21) 
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut9 

```
278-Cut9-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.19.0,<=2.19.1)
| | +- urllib3(version range:<1.24,>=1.21.1)
| +- transifex-client(version range:>=0.13.5, <=0.13.6)
| | +- urllib3(version range:<1.24)
```



```
278-Cut9-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.19.0,<=2.19.1)
| | +- urllib3(version range:<1.24,>=1.21) 
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut10 

```
278-Cut10-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.20.0, <=2.21.0)
| | +- urllib3(version range:<1.25,>=1.21.1)
| +- transifex-client(version range:>=0.13.5, <=0.13.6)
| | +- urllib3(version range:<1.24)
```



```
278-Cut10-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.20.0, <=2.21.0)
| | +- urllib3(version range:<1.25,>=1.21) 
| +- no call to transifex-client, the dependency can be removed
```



### (issue) 278-Cut11 

```
278-Cut11-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.22.0, <=2.24.0)
| | +- urllib3(version range:<1.26,>=1.21.1)
| +- transifex-client(version range:>=0.13.5, <=0.13.6)
| | +- urllib3(version range:<1.24)
```



```
278-Cut11-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.22.0, <=2.24.0)
| | +- urllib3(version range:<1.26,>=1.21)
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut12 

```
278-Cut12-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.25.0,<=2.28.1)
| | +- urllib3(version range:<1.27,>=1.21.1)
| +- transifex-client(version range:>=0.13.5, <=0.13.6)
| | +- urllib3(version range:<1.24)
```



```
278-Cut12-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.25.0,<=2.28.1)
| | +- urllib3(version range:<1.27,>=1.21)
| +- no call to transifex-client, the dependency can be removed
```





### 278-Cut13 

```
278-Cut13-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.18.0, <=2.18.1)
| | +- urllib3(version range:<1.22,>=1.21.1)
| +- transifex-client(version range:>=0.13.7, <14)
| | +- urllib3(version range:<2.0.0,>=1.24.2)
```



```
278-Cut13-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.16.0, <=2.18.1)
| | +- urllib3(version range:<1.22,>=1.21)
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut14 

```
278-Cut14-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.18.2, <=2.18.4)
| | +- urllib3(version range:<1.23,>=1.21.1)
| +- transifex-client(version range:>=0.13.7, <14)
| | +- urllib3(version range:<2.0.0,>=1.24.2)
```



```
278-Cut14-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.18.2, <=2.18.4)
| | +- urllib3(version range:<1.23,>=1.21) 
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut15 

```
278-Cut15-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.19.0,<=2.19.1)
| | +- urllib3(version range:<1.24,>=1.21.1)
| +- transifex-client(version range:>=0.13.7, <14)
| | +- urllib3(version range:<2.0.0,>=1.24.2)
```



```
278-Cut15-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.19.0,<=2.19.1)
| | +- urllib3(version range:<1.24,>=1.21) 
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut16 

```
278-Cut16-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.20.0, <=2.21.0)
| | +- urllib3(version range:<1.25,>=1.21.1)
| +- transifex-client(version range:>=0.13.7, <14)
| | +- urllib3(version range:<2.0.0,>=1.24.2)
```



```
278-Cut16-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.20.0, <=2.21.0)
| | +- urllib3(version range:<1.25,>=1.21) 
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut17 

```
278-Cut17-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.22.0, <=2.24.0)
| | +- urllib3(version range:<1.26,>=1.21.1)
| +- transifex-client(version range:>=0.13.7, <14)
| | +- urllib3(version range:<2.0.0,>=1.24.2)
```



```
278-Cut17-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.22.0, <=2.24.0)
| | +- urllib3(version range:<1.26,>=1.21)
| +- no call to transifex-client, the dependency can be removed
```



### 278-Cut18 

```
278-Cut18-before
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.25.0,<=2.28.1)
| | +- urllib3(version range:<1.27,>=1.21.1)
| +- transifex-client(version range:>=0.13.7, <14)
| | +- urllib3(version range:<2.0.0,>=1.24.2)
```



```
278-Cut18-after
money-to-prisoners-common - 9.16.0
| +- requests(version range:>=2.25.0,<=2.28.1)
| | +- urllib3(version range:<1.27,>=1.21)
| +- no call to transifex-client, the dependency can be removed
```



## 329

### (issue) 329-Cut1 

```
329-Cut1-before
fossor - 1.1.2
| +- asciietch(version range:>=1.0.2,<=1.0.6)
| | +- parsedatetime(version range:==2.4)
| +- parsedatetime(version range:>=2.4)
```



```
329-Cut1-after
fossor - 1.1.2
| +- asciietch(version range:>=1.0.0,<=1.0.6) 
| | +- no call to parsedatetime, the dependency can be removed
| +- parsedatetime(version range:>=2.1)
```



## 330

```
330-Cut0
xontrib-readable-traceback - 0.3.2
| +- backtrace(version range:==0.1.0)
| | +- no dependency on colorama
| +- colorama(version range:>=0.3.7)
```



### (issue) 330-Cut1 

```
330-Cut1-before
xontrib-readable-traceback - 0.3.2
| +- backtrace(version range:>=0.1.1,<=0.2.1)
| | +- colorama(version range:==0.3.7)
| +- colorama(version range:>=0.3.7)
```



```
330-Cut1-after
xontrib-readable-traceback - 0.3.2
| +- backtrace(version range:>=0.1.1,<=0.2.1)
| | +- colorama(version range:==0.3.7)
| +- colorama(version range:>=0.3.7)
```



## 331

```
331-Cut0
Browsercookie<0.7.0
   no dependency on keyring
pycookiecheat>=0.1.0,<=0.1.3
   no dependency on keyring
```



### 331-Cut1 

```
331-Cut1-before
video-funnel - 0.3.1
| +- browsercookie(version range:>=0.7.0,<=0.7.7)
| | +- keyring(version range:*)
| +- pycookiecheat(version range:>=0.1.4, <=0.2.0)
| | +- keyring(version range:>=5.0)
```



```
331-Cut1-after
video-funnel - 0.3.1
| +- browsercookie(version range:>=0.7.0,<=0.7.7)
| | +- keyring(version range:*)
| +- pycookiecheat(version range:>=0.1.4, <=0.2.0)
| | +- keyring(version range:>=0.1) 
```



### 331-Cut2 

```
331-Cut2-before
video-funnel - 0.3.1
| +- browsercookie(version range:>=0.7.0,<=0.7.7)
| | +- keyring(version range:*)
| +- pycookiecheat(version range:>=0.3.1, <=0.3.3)
| | +- keyring(version range:==8.7)
```



```
331-Cut2-after
video-funnel - 0.3.1
| +- browsercookie(version range:>=0.7.0,<=0.7.7)
| | +- keyring(version range:*)
| +- pycookiecheat(version range:>=0.3.1, <=0.3.3)
| | +- keyring(version range:>=0.1, <=21.3.1)
```



### 331-Cut3 

```
331-Cut3-before
video-funnel - 0.3.1
| +- browsercookie(version range:>=0.7.0,<=0.7.7)
| | +- keyring(version range:*)
| +- pycookiecheat(version range:>=0.3.4, <=0.4.3)
| | +- keyring(version range:==10.3.2)
```



```
331-Cut3-after
video-funnel - 0.3.1
| +- browsercookie(version range:>=0.7.0,<=0.7.7)
| | +- keyring(version range:*)
| +- pycookiecheat(version range:>=0.3.4, <=0.4.3)
| | +- keyring(version range:>=0.1, <=21.3.1)
```



### (issue) 331-Cut4 

```
331-Cut4-before
video-funnel - 0.3.1
| +- browsercookie(version range:>=0.7.0,<=0.7.7)
| | +- keyring(version range:*)
| +- pycookiecheat(version range:==0.4.5)
| | +- keyring(version range:==19.1.0)
```



```
331-Cut4-after
video-funnel - 0.3.1
| +- browsercookie(version range:>=0.7.0,<=0.7.7)
| | +- keyring(version range:*)
| +- pycookiecheat(version range:==0.4.5)
| | +- keyring(version range:>=1.2, <=21.3.1)
```



### 331-Cut5 

```
331-Cut5-before
video-funnel - 0.3.1
| +- browsercookie(version range:>=0.7.0,<=0.7.7)
| | +- keyring(version range:*)
| +- pycookiecheat(version range:==0.4.7)
| | +- keyring(version range:==23.0.0)
```



```
331-Cut5-after
video-funnel - 0.3.1
| +- browsercookie(version range:>=0.7.0,<=0.7.7)
| | +- keyring(version range:*)
| +- pycookiecheat(version range:==0.4.7)
| | +- keyring(version range:==23.0.0)
```



## 335

### (issue) 335-Cut1 

```
335-Cut1-before
tensor2tensor  - 1.15.5
| +- gym(version range:==0.14.0)
| | +- cloudpickle(version range:~=1.2.0)
| +- tensorflow-probability(version range:==0.7.0)
| | +- cloudpickle(version range:>0.6.1)
```



```
335-Cut1-after
tensor2tensor  - 1.15.5
| +- gym(version range:>=0.14.0, <=0.15.4)
| | +- cloudpickle(version range:~=1.2.0)
| +- tensorflow-probability(version range:==0.7.0) 
| | +- cloudpickle(version range:>0.6.1) 
```



## 337



```
337-Cut0
flask-oauthlib 0.9.5
| +- oauthlib(version range:>=1.1.2,<3.0.0)
| +- requests-oauthlib(version range:>=0.6.2,<1)
| | +- no dependency on oauthlib
```



### 337-Cut1 

```
337-Cut1-before
flask-oauthlib 0.9.5
| +- oauthlib(version range:>=1.1.2,<3.0.0)
| +- requests-oauthlib(version range:==1.0.0)
| | +- oauthlib(version range:>=0.6.2)
```



```
337-Cut1-after
flask-oauthlib  0.9.5
| +- oauthlib(version range:>=1.1.0,<3.0.0)
| +- requests-oauthlib(version range:==1.0.0)
| | +- oauthlib(version range:>=0.6.2) 
```



### 337-Cut2 

```
337-Cut2-before
flask-oauthlib 0.9.5
| +- oauthlib(version range:>=1.1.2,<3.0.0)
| +- requests-oauthlib(version range:==1.1.0)
| | +- oauthlib(version range:>=2.1.0,<3.0.0)
```



```
337-Cut2-after
flask-oauthlib  0.9.5
| +- oauthlib(version range:>=1.1.0,<3.0.0)
| +- requests-oauthlib(version range:==1.1.0)
| | +- oauthlib(version range:>=2.1.0,<3.0.0)
```



### (issue) 337-Cut3 

```
337-Cut3-before
flask-oauthlib 0.9.5
| +- oauthlib(version range:>=1.1.2,<3.0.0)
| +- requests-oauthlib(version range:>=1.2.0,<=1.3.1)
| | +- oauthlib(version range:>=3.0.0)
```



```
337-Cut3-after
flask-oauthlib  0.9.5
| +- oauthlib(version range:>=1.1.0,<3.0.0)
| +- requests-oauthlib(version range:>=1.2.0,<=1.3.1)
| | +- oauthlib(version range:>=3.0.0)
```



## 339 



### 339-Cut1 

```
339-Cut1-before
docker-cron-cli - 0.3.0
| +- docker(version range:>=2.0.0, <=2.3.0)
| | +- requests (version range:>= 2.5.2, != 2.11.0, != 2.12.2)
| +- requests (version range:>=2.6.1,<2.8)
```



```
339-Cut1-after
docker-cron-cli - 0.3.0
| +- docker(version range:>=2.0.0, <=2.3.0)
| | +- requests (version range:>= 2.5.2, != 2.11.0)
| +-no call to requests, the dependency can be removed
```



### 339-Cut2  


```
339-Cut2-before
docker-cron-cli - 0.3.0
| +- docker(version range:>=2.4.0,<=2.6.1)
| | +- requests (version range:>= 2.5.2, != 2.11.0, != 2.12.2, != 2.18.0)
| +- requests (version range:>=2.6.1,<2.8)
```




```
339-Cut2-after
docker-cron-cli - 0.3.0
| +- docker(version range:>=2.4.0,<=2.6.1)
| | +- requests (version range:>= 2.5.2, != 2.11.0)
| +-no call to requests, the dependency can be removed
```



### (issue) 339-Cut3 


```
339-Cut3-before
docker-cron-cli - 0.3.0
| +- docker(version range:>=2.7.0,<=5.0.3)
| | +- requests (version range:>= 2.14.2, != 2.18.0)
| +- requests (version range:>=2.6.1,<2.8)
```




```
339-Cut3-after
docker-cron-cli - 0.3.0
| +- docker(version range:>=2.7.0,<=5.0.3)
| | +- requests (version range:>= 2.14.0, != 2.18.0)
| +-no call to requests, the dependency can be removed
```



### 339-Cut4  

```
339-Cut4-before
docker-cron-cli - 0.3.0
| +- docker(version range:>=6.0.0b1,<=6.0.1)
| | +- requests (version range:>= 2.26.0)
| +- requests (version range:>=2.6.1,<2.8)
```



```
339-Cut4-after
docker-cron-cli - 0.3.0
| +- docker(version range:>=6.0.0b1,<=6.0.1)
| | +- requests (version range:>= 2.26.0)
| +-no call to requests, the dependency can be removed
```





## 341



```
341-Cut0
molo-surveys - 8.3.3
| +- django-celery(version range:>=2.0.0,<=3.1.17)
| | +- no dependency on django
| +- wagtail-personalisation-molo(version range:<1.1,>=1.0.3)
| | +- wagtail(version range:>=2.2,<2.3)
| | | +- django(version range:<2.1,>=1.11)
```





### (issue) 341-Cut1 

```
341-Cut1-before
molo-surveys - 8.3.3
| +- django-celery(version range:>=3.2.1,<=3.3.1)
| | +- django(version range:>=1.8)
| +- wagtail-personalisation-molo(version range:<1.1,>=1.0.3)
| | +- wagtail(version range:>=2.2,<2.3)
| | | +- django(version range:<2.1,>=1.11)
```



```
341-Cut1-after
molo-surveys - 8.3.3
| +- no call to django-celery, the dependency can be removed
| +- wagtail-personalisation-molo(version range:<1.1,>=1.0.3)
| | +- wagtail(version range:>=2.2,<2.3)
| | | +- django(version range:<2.1,>=1.11)
```



## 346

### (issue) 346-Cut1 

```
346-Cut1-before
djangoplus - 0.0.98
| +- requests(version range:==2.21.0)
| | +- urllib3(version range:>=1.21.1,<1.25)
| +- selenium(version range:==3.141.0)
| | +- urllib3(version range:*)
```



```
346-Cut1-after
djangoplus - 0.0.98
| +- requests(version range:>=2.20.0,<=2.21.0)
| | +- urllib3(version range:>=1.21,<1.25)
| +- selenium(version range:==3.141.0) 
| | +- urllib3(version range:*)
```



## 347

### 347-Cut1 

```
347-Cut1-before
django-web3-auth  - 0.1.0
| +- ethereum(version range:==2.3.1)
| | +- rlp(version range:>=0.4.7)
| +- rlp(version range:==0.6.0)
```



```
347-Cut1-after
django-web3-auth  - 0.1.0
| +- ethereum(version range:==2.3.1) 
| | +- rlp(version range:>=0.4.7) 
| +-no call to rlp, the dependency can be removed
```



### (issue) 347-Cut2 

```
347-Cut2-before
django-web3-auth  - 0.1.0
| +- ethereum(version range:==2.3.2)
| | +- rlp(version range:>=1.0.1,<2.0.0)
| +- rlp(version range:==0.6.0)
```



```
347-Cut2-after
django-web3-auth  - 0.1.0
| +- ethereum(version range:==2.3.2)
| | +- rlp(version range:>=1.0.1,<2.0.0)
| +-no call to rlp, the dependency can be removed
```



## 349

```
349-Cut0
cert-mailer - 0.0.4
| +- six(version range:==1.11.0)
| +- tox(version range:>=4.2.0a2,<=4.2.6)
| | +- no dependency on six
```



### 349-Cut1 

```
349-Cut1-before
cert-mailer - 0.0.4
| +- six(version range:==1.11.0)
| +- tox(version range:==3.0.0)
| | +- six(version range:*)
```



```
349-Cut1-after
cert-mailer - 0.0.4
| +-no call to six, the dependency can be removed
| +-no call to tox, the dependency can be removed
```



### 349-Cut2 

```
349-Cut2-before
cert-mailer - 0.0.4
| +- six(version range:==1.11.0)
| +- tox(version range:>=3.1.0,<=3.14.3)
| | +- six(version range:<2,>=1.0.0)
```



```
349-Cut2-after
cert-mailer - 0.0.4
| +-no call to six, the dependency can be removed
| +-no call to tox, the dependency can be removed
```



### (issue) 349-Cut3 

```
349-Cut3-before
cert-mailer - 0.0.4
| +- six(version range:==1.11.0)
| +- tox(version range:>=3.14.4,<=3.15.0)
| | +- six(version range:<2,>=1.14.0)
```



```
349-Cut3-after
cert-mailer - 0.0.4
| +-no call to six, the dependency can be removed
| +-no call to tox, the dependency can be removed
```



### 349-Cut4 

```
349-Cut4-before
cert-mailer - 0.0.4
| +- six(version range:==1.11.0)
| +- tox(version range:>=3.15.1,<=3.28.0)
| | +- six(version range:>=1.14.0)
```



```
349-Cut4-after
cert-mailer - 0.0.4
| +-no call to six, the dependency can be removed
| +-no call to tox, the dependency can be removed
```



## 351



### (issue) 351-Cut1 

```
351-Cut1-before
antinex-client - 1.3.5
| +- pycodestyle(version range:<=2.3.1)
```



```
351-Cut1-after
antinex-client - 1.3.5
| +- no call to pycodestyle, the dependency can be removed
```



## 353

### (issue) 353-Cut1 

```
353-Cut1-before
agora-py - 0.5.47
| +- rdflib(version range:==4.2.1)
```



```
353-Cut1-after
agora-py - 0.5.47
| +- rdflib(version range:==4.2.1)
```





## 354



### 354-Cut1 

```
354-Cut1-before
agora-wot - 0.2.20
| +- rdflib(version range:==4.2.1)
| +- rdflib-jsonld(version range: ==0.2.0)
| | +- rdflib(version range:>=4.1)
```



```
354-Cut1-after
agora-wot - 0.2.20
| +- rdflib(version range:==4.2.1)
| +- rdflib-jsonld(version range: ==0.2.0)
| | +- rdflib(version range:>=4.1)
```





### 354-Cut2 

```
354-Cut2-before
agora-wot - 0.2.20
| +- rdflib(version range:==4.2.1)
| +- rdflib-jsonld(version range: >=0.3, <=0.4.0)
| | +- rdflib(version range:>=4.2)
```



```
354-Cut2-after
agora-wot - 0.2.20
| +- rdflib(version range:==4.2.1)
| +- rdflib-jsonld(version range: >=0.3, <=0.4.0)
| | +- rdflib(version range:>=4.2)
```



### (issue) 354-Cut3 

```
354-Cut3-before
agora-wot - 0.2.20
| +- rdflib(version range:==4.2.1)
| +- rdflib-jsonld(version range:==0.5.0)
| | +- rdflib(version range:>=4.2.2)
```



```
354-Cut3-after
agora-wot - 0.2.20
| +- rdflib(version range:==4.2.1) 
| +- rdflib-jsonld(version range:==0.5.0)
| | +- rdflib(version range:>=4.2.2) 
```



### 354-Cut4 

```
354-Cut4-before
agora-wot - 0.2.20
| +- rdflib(version range:==4.2.1)
| +- rdflib-jsonld(version range:==0.6.0)
| | +- rdflib(version range:*)
```



```
354-Cut4-after
agora-wot - 0.2.20
| +- rdflib(version range:==4.2.1)
| +- rdflib-jsonld(version range:==0.6.0)
| | +- rdflib(version range:*)
```



### 354-Cut5 

```
354-Cut5-before
agora-wot - 0.2.20
| +- rdflib(version range:==4.2.1)
| +- rdflib-jsonld(version range:==0.6.1)
| | +- rdflib(version range:>=5.0.0)
```



```
354-Cut5-after
agora-wot - 0.2.20
| +- rdflib(version range:==4.2.1) 
| +- rdflib-jsonld(version range:==0.6.1)
| | +- rdflib(version range:>=5.0.0)
```



### 354-Cut6 

```
354-Cut6-before
agora-wot - 0.2.20
| +- rdflib(version range:==4.2.1)
| +- rdflib-jsonld(version range:==0.6.2)
| | +- rdflib(version range:>=5.0.0)
```



```
354-Cut6-after
agora-wot - 0.2.20
| +- rdflib(version range:==4.2.1) 
| +- rdflib-jsonld(version range:==0.6.2)
| | +- no call to rdflib, the dependency can be removed
```



## 357

### (issue) 357-Cut1 

```
357-Cut1-before
aiocontextvars - 0.2.2
| +- contextvars(version range:==2.4)
```



```
357-Cut1-after
aiocontextvars - 0.2.2
| +- contextvars(version range:==2.4)
```



## 359

### (issue) 359-Cut1 

```
359-Cut1-before
django-client-logger - 2.0
| +- django(version range:>2.1)
| +- django-userservice(version range: <=3.1.2,>=3.1)
| | +- django(version range:<3.0,>2.1)
```



```
359-Cut1-after
django-client-logger - 2.0
| +- django(version range:>2.1)
| +- django-userservice(version range: <=3.1.2,>=3.1)
| | +- django(version range:<3.0,>2.1)
```



### 359-Cut2 

```
359-Cut2-before
django-client-logger - 2.0
| +- django(version range:>2.1)
| +- django-userservice(version range:==3.1.3)
| | +- django(version range:<3.2,>2.1)
```



```
359-Cut2-after
django-client-logger - 2.0
| +- django(version range:>2.1)
| +- django-userservice(version range:==3.1.3)
| | +- django(version range:<3.2,>2.1)
```



### 359-Cut3 

```
359-Cut3-before
django-client-logger - 2.0
| +- django(version range:>2.1)
| +- django-userservice(version range:==3.1.4)
| | +- django(version range:<3.3,>2.1)
```



```
359-Cut3-after
django-client-logger - 2.0
| +- django(version range:>2.1)
| +- django-userservice(version range:==3.1.4)
| | +- django(version range:<3.3,>2.1)
```



## 362

### (issue) 362-Cut1 

```
362-Cut1-before
piicatcher - 0.10.0
| +- boto3(version range:==1.12.1)
| | +- botocore(version range:>=1.15.1,<1.16.0)
| +- pyathena(version range:>=1.0.0,<=2.9.4)
| | +- botocore(version range:>=1.5.52)
```



```
362-Cut1-after
piicatcher - 0.10.0
| +- boto3(version range:==1.12.1)
| | +- botocore(version range:>=1.15.1,<1.16.0)
| +- pyathena(version range:>=1.0.0,<=2.9.4)
| | +- botocore(version range:>=1.5.52)
```





### 362-Cut2 

```
362-Cut2-before
piicatcher - 0.10.0
| +- boto3(version range:==1.12.1)
| | +- botocore(version range:>=1.15.1,<1.16.0)
| +- pyathena(version range:>=2.9.5,<=2.10.0)
| | +- botocore(version range:>=1.16.20)
```



```
362-Cut2-after
piicatcher - 0.10.0
| +- boto3(version range:==1.12.1)
| | +- botocore(version range:>=1.15.1,<1.16.0)
| +- pyathena(version range:>=2.9.5,<=2.10.0)
| | +- botocore(version range:>=1.16.20)
```



### 362-Cut3 

```
362-Cut3-before
piicatcher - 0.10.0
| +- boto3(version range:==1.12.1)
| | +- botocore(version range:>=1.15.1,<1.16.0)
| +- pyathena(version range:>=2.11.0,<=2.17.0)
| | +- botocore(version range:>=1.24.7)
```



```
362-Cut3-after
piicatcher - 0.10.0
| +- boto3(version range:==1.12.1)
| | +- botocore(version range:>=1.15.1,<1.16.0)
| +- pyathena(version range:>=2.11.0,<=2.17.0)
| | +- botocore(version range:>=1.24.7)
```



### 362-Cut4 

```
362-Cut4-before
piicatcher - 0.10.0
| +- boto3(version range:==1.12.1)
| | +- botocore(version range:>=1.15.1,<1.16.0)
| +- pyathena(version range:>=2.18.0,<=2.19.0)
| | +- botocore(version range:>=1.29.4)
```



```
362-Cut4-after
piicatcher - 0.10.0
| +- boto3(version range:==1.12.1)
| | +- botocore(version range:>=1.15.1,<1.16.0)
| +- pyathena(version range:>=2.18.0,<=2.19.0)
| | +- botocore(version range:>=1.29.4)
```





## 363



### 363-Cut1 

```
363-Cut1-before
superdesk-core - 1.33.1
| +- eve(version range:<=0.6.4,>=0.6)
| | +- itsdangerous(version range:<1.0,>=0.22)
| +- flask(version range:>=0.10.1,<=0.12)
| | +- itsdangerous(version range:>=0.21)
```



```
363-Cut1-after
superdesk-core - 1.33.1
| +- eve(version range:eve<=0.6.4,>=0.6)
| | +- no call to itsdangerous, the dependency can be removed
| +- flask(version range:>=0.10.1,<=0.12)
| | +- itsdangerous(version range:>=0.20)
```



### (issue) 363-Cut2 

```
363-Cut2-before
superdesk-core - 1.33.1
| +- eve(version range:<=0.7.8,>=0.7)
| | +- itsdangerous(version range:<1.0,>=0.24)
| +- flask(version range:>=0.10.1,<=0.12)
| | +- itsdangerous(version range:>=0.21)
```



```
363-Cut2-after
superdesk-core - 1.33.1
| +- eve(version range:<=0.7.8,>=0.7)
| | +- no call to itsdangerous, the dependency can be removed
| +- flask(version range:>=0.10.1,<=0.12)
| | +- itsdangerous(version range:>=0.20)
```



## 364



### 364-Cut1 

```
364-Cut1-before
trios - 2.1
| +- numpy(version range:==1.13.3)
| +- scikit-image(version range:==0.13.1)
| | +- tifffile(version range:==0.15.1)
| | | +- numpy(version range:>=1.8.2)
```



```
364-Cut1-after
trios - 2.1
| +- numpy(version range:>=1.13.0,<=1.13.3)
| +- no call to scikit-image, the dependency can be removed
```



### 364-Cut2 

```
364-Cut2-before
trios - 2.1
| +- numpy(version range:==1.13.3)
| +- scikit-image(version range:==0.13.1)
| | +- tifffile(version range:>=2018.10.18,<=2019.7.26)
| | | +- numpy(version range:>=1.11.3)
```



```
364-Cut2-after
trios - 2.1
| +- numpy(version range:>=1.13.0,<=1.13.3)
| +- no call to scikit-image, the dependency can be removed
```





### 364-Cut3 

```
364-Cut3-before
trios - 2.1
| +- numpy(version range:==1.13.3)
| +- scikit-image(version range:==0.13.1)
| | +- tifffile(version range:==2019.7.26.2)
| | | +- numpy(version range:>=1.14.6)
```



```
364-Cut3-after
trios - 2.1
| +- numpy(version range:>=1.13.0,<=1.13.3)
| +- no call to scikit-image, the dependency can be removed
```





### (issue) 364-Cut4 

```
364-Cut4-before
trios - 2.1
| +- numpy(version range:==1.13.3)
| +- scikit-image(version range:==0.13.1)
| | +- tifffile(version range:>=2020.2.16,<=2021.11.2)
| | | +- numpy(version range:>=1.15.1)
```



```
364-Cut4-after
trios - 2.1
| +- numpy(version range:>=1.13.0,<=1.13.3)
| +- no call to scikit-image, the dependency can be removed
```





### 364-Cut5 

```
364-Cut5-before
trios - 2.1
| +- numpy(version range:==1.13.3)
| +- scikit-image(version range:==0.13.1)
| | +- tifffile(version range:>=2022.2.2,<=2022.10.10)
| | | +- numpy(version range:>=1.19.2)
```



```
364-Cut5-after
trios - 2.1
| +- numpy(version range:>=1.13.0,<=1.13.3)
| +- no call to scikit-image, the dependency can be removed
```





## 365

```
365-cut0
wpt-superset - 1.0.1
| +- flower(version range:>=0.1.0,<=0.9.3)
| | +- no dependency on humanize
| +- humanize(install version:2.3.0 version range:*)
```



### (issue) 365-Cut1 

```
365-Cut1-before
wpt-superset - 1.0.1
| +- flower(version range:==0.9.4)
| | +- humanize(version range:==0.5.1)
| +- humanize(version range:*)
```



```
365-Cut1-after
wpt-superset - 1.0.1
| +- no call to flower, the dependency can be removed
| +- humanize(version range:*)
```



### 365-Cut2 

```
365-Cut2-before
wpt-superset - 1.0.1
| +- flower(version range:>=0.9.5,<=1.2.0)
| | +- humanize(version range:*)
| +- humanize(version range:*)
```



```
365-Cut2-after
wpt-superset - 1.0.1
| +- no call to flower, the dependency can be removed
| +- humanize(version range:*)
```





## 366

### 366-Cut1 

```
366-Cut1-before
zelt - 1.2.14
| +- kubernetes(version range:==10.0.1)
| | +- pyyaml(version range:>=3.12)
| +- pyyaml(version range:>=5.1,<6.0)
```



```
366-Cut1-after
zelt - 1.2.14
| +- kubernetes(version range:==10.0.1)
| | +- pyyaml(version range:>=3.10)
| +- pyyaml(version range:>=5.1,<6.0)
```



### (issue) 366-Cut2 

```
366-Cut2-before
zelt - 1.2.14
| +- kubernetes(version range:==10.1.0)
| | +- pyyaml(version range:<4,>=3.12)
| +- pyyaml(version range:>=5.1,<6.0)
```



```
366-Cut2-after
zelt - 1.2.14
| +- kubernetes(version range:==10.1.0)
| | +- pyyaml(version range:<4,>=3.10)
| +- pyyaml(version range:>=5.1,<6.0)
```



## 367

### 367-Cut1 

```
367-Cut1-before
zvt - 0.7.8
| +- jqdatasdk(version range:(>=1.4.3,<=1.7.0) U (>=1.8.6,<=1.8.11))
| | +- pandas(version range:>=0.16.2)
| +- pandas(version range:>=0.24.2)
```



```
367-Cut1-after
zvt - 0.7.8
| +- jqdatasdk(version range:(>=1.4.3,<=1.7.0) U (>=1.8.6,<=1.8.11))
| | +- pandas(version range:>=0.15.0)
| +- pandas(version range:>=0.24.2)
```



### 367-Cut2 

```
367-Cut2-before
zvt - 0.7.8
| +- jqdatasdk(version range:>=1.7.1,<=1.7.8)
| | +- pandas(version range:<=0.24.2,>=0.16.2)
| +- pandas(version range:>=0.24.2)
```



```
367-Cut2-after
zvt - 0.7.8
| +- jqdatasdk(version range:>=1.7.1,<=1.7.8)
| | +- pandas(version range:<=0.24.2,>=0.15.0))
| +- pandas(version range:>=0.24.2)
```



### (issue) 367-Cut3 

```
367-Cut3-before
zvt - 0.7.8
| +- jqdatasdk(version range:>=1.7.9,<=1.8.5)
| | +- pandas(version range:<=0.25.3,>=0.16.2)
| +- pandas(version range:>=0.24.2)
```



```
367-Cut3-after
zvt - 0.7.8
| +- jqdatasdk(version range:>=1.7.9,<=1.8.5)
| | +- pandas(version range:<=0.25.3,>=0.15.0)
| +- pandas(version range:>=0.24.2)
```


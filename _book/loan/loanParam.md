# 关于MOV借贷参数的附加说明

## 最小借出额

MOV借币用户借币的最小数量，当前设置最小借出额见下表所示，该数值可能根据产品需求和市场波动进行调整。

|币种|BTC|ETH|LTC|DOT|
|:----|:----|:----|:----|:----|
|最小借出额|0.03|1|8|60|


## 最小抵押率

MOV借币用户至少需要抵押的抵押品比例，当前设置的最小抵押率见下表所示，该数值可能根据产品需求和市场波动进行调整。

|币种|BTC|ETH|LTC|DOT|
|:----|:----|:----|:----|:----|
|最小抵押率|140%|140%|140%|140%|


举例：用户抵押ETH借出1个BTC，BTC的最小抵押率不能低于140%，假设当前BTC/ETH=24，那么借出1BTC，至少需要抵押 24* 140% = 33.6个ETH

## 最大抵押率

MOV借币用户最多需要抵押的抵押品比例，当前设置的最大抵押率见下表所示，该数值可能根据产品需求和市场波动进行调整。

|币种|BTC|ETH|LTC|DOT|
|:----|:----|:----|:----|:----|
|最小抵押率|330%|330%|330%|330%|

举例：用户抵押ETH借出1个BTC，BTC的最大抵押率不能高于330%，假设当前BTC/ETH=24，那么借出1BTC，最多可以抵押 24* 330% = 79.2个ETH


## 清算线

当用户的抵押率小于清算线时，则会进行清算，清算线如下表，该数值可能根据产品需求和市场波动进行调整。

|币种|BTC|ETH|LTC|DOT|
|:----|:----|:----|:----|:----|
|清算线|130%|130%|130%|130%|


举例：假设借出时BTC/ETH=24，用户抵押33.6个ETH借出1个BTC，当市场剧烈波动BTC/ETH=26时，用户的抵押率=33.6/26=129% < 130%，用户的ETH将被拍卖清算

## 危险等级

MOV设置了不同的危险等级来提醒用户注意资产的抵押率，防止被清算和资产损失。

**危险：（当前抵押率-清算线）≤10%**

**警告：10%<（当前抵押率-清算线）<30%**

**正常：30%≤（当前抵押率-清算线）**

危险用红色表示，警告用黄色表示，正常用绿色表示

## 最小偿还额

MOV用户在偿还借币时的最小数量，偿还时无法偿还小于该数值的抵押品，当前设置最小偿还额见下表所示，该数值可能根据产品需求和市场波动进行调整。

|币种|BTC|ETH|LTC|DOT|
|:----|:----|:----|:----|:----|
|最小偿还额|0.0015|0.05|0.4|3|


## 最小存入额

存币用户最小的存入数量，无法存入比最小存入额更小的数量，当前设置最小存入额见下表所示，该数值可能根据产品需求和市场波动进行调整。

|币种|BTC|ETH|LTC|DOT|
|:----|:----|:----|:----|:----|
|最小存入额|0.003|0.1|0.8|6|


## 最小取出额

存币用户最小的取出数量，无法取出比最小取出额更小的数量，当前设置最小取出额见下表所示，该数值可能根据产品需求和市场波动进行调整。

|币种|BTC|ETH|LTC|DOT|
|:----|:----|:----|:----|:----|
|最小取出额|0.003|0.1|0.8|6|


**注意：如果当你分批取出，最后一批的取出数量小于最小取出额时将无法取出，需要先存入一定的数量达到最小取出额后才能取出**

## 清算折扣

清算折扣从第一轮的95%开始，每轮递减5%，直到减少为50%则不再进行减少，后续将一直以50%的清算折扣进行拍卖。




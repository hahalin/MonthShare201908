# Serverless AWS Lambda 
# 使用NodeJS實作API+React 

## Serverless的特點

1. Faas: Function as a Service,不需要Server,VM
2. 呼叫時才啟動與計費
3. 搭配AWS API Gateway可實作出無狀態Web API

![](https://github.com/hahalin/MonthShare201908/blob/master/1_2PLUjcDf3zqPCwzaVsVT2A.png )
圖片出處: https://medium.com/google-cloud/serverless-on-google-cloud-platform-an-introduction-with-serverless-store-demo-41992dec085
![](https://github.com/hahalin/MonthShare201908/blob/master/1_pKKhpjQ-CVeJR8BNRWc1dg.png )
圖片出處: https://medium.com/google-cloud/serverless-on-google-cloud-platform-an-introduction-with-serverless-store-demo-41992dec085

![](https://github.com/hahalin/MonthShare201908/blob/master/bigPic.png )
這張我畫的

## 預先準備

1. AWS Account
2. Node.js+npm
3. tool
  - Serverless Framework
  - Dashbird account

## serverless framework

### 安裝

```javascript
  npm install -g serverless
```
### 設定AWS帳號

```javascript
  serverless config credentials --provider aws --key YOUR_ACCESS_KEY --secret YOUR_SECRET_KEY
```
### 使用AWS樣板建立專案

```javascript
  sls create -t aws-nodejs -p YourProjectName
```
### Client測試模式設定

```javascript
  npm install --save-dev serverless-offline
  npm i --save mongoose dotenv  
  sls offline start
```
### 發佈

```javascript
  sls deploy
```


## 實機Demo

1. Nodejs Project
https://github.com/hahalin/Serverless-Helloworld

2. React Project
https://github.com/hahalin/NoteItems

## 參考資料
1. https://hackernoon.com/a-crash-course-on-serverless-with-node-js-632b37d58b44
2. https://www.programmableweb.com/news/how-to-build-serverless-rest-api-nodejs-and-mongodb/how-to/2018/07/15
3. https://medium.com/hackernoon/how-to-deploy-a-node-js-application-to-aws-lambda-using-serverless-ae7e7ebe0996

## ToDo

1. Edit and Delete
2. Dashbird實際使用
3. 使用express取代handler內各function設定Path
4. 使用JWT設計Token based authenication
5. 設計APP(iOS,Android)呼叫Lambda建構的API

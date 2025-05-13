English version underneath

# 推特情緒分析監控系統
本專案運用 Microsoft Azure 平台，建構一套能即時偵測與分析推特上特定標籤情緒的自動化監控系統。專案整合 Azure Logic Apps、Cognitive Services 以及 Twilio，讓企業能即時掌握與自身品牌相關的負面聲量。

## 專案功能
- 自動偵測特定推特標籤貼文（#YUANenterprise）

- 情緒分析：透過 Azure Text Analytics 判定貼文情緒

- 負面推文警示：若情緒分數低於 0.5，透過 Twilio 簡訊即時通知使用者，內含：

1. 情緒分數

2. 貼文使用者 ID

## 系統處理流程
1. Trigger 設定：當有新推文包含 #YUANenterprise 時觸發流程

2. 情緒分析：使用 Azure Cognitive Services 中的 Text Analytics API 進行情緒評分

3. 判斷與通知：

  - 若情緒分數低於 0.5

  - 使用 Twilio 傳送簡訊至指定用戶，通知其有潛在負評

## 技術架構
- Azure Logic Apps：負責流程自動化

- Azure Cognitive Services - Text Analytics：處理情緒分析任務

- Twilio API：發送即時通知簡訊

- Twitter API：讀取並監控指定推文

## 成果展示
自動偵測特定推特標籤貼文（#YUANenterprise）
![image](https://github.com/giraffeiscute/azure-project-tweeter-sentiment-tracking/blob/main/result/twitter.png)

負面推文警示：若情緒分數低於 0.5，透過 Twilio 簡訊即時通知使用者，內含情緒分數和貼文使用者 ID
<img src="https://github.com/giraffeiscute/azure-project-tweeter-sentiment-tracking/blob/main/result/%E7%B0%A1%E8%A8%8A.jpg" alt="image" width="350">


## 參考資料
陳小熊 (Oct 2018). 使用Azure Logic Apps打造公司相關推特情緒分析監控系統

****

# Twitter Sentiment Monitoring System
This project leverages Microsoft Azure to build an automated system for real-time detection and sentiment analysis of specific hashtags on Twitter. It integrates Azure Logic Apps, Cognitive Services, and Twilio to help businesses monitor and respond to negative sentiment related to their brand.

## Project Features
- Automatic Detection of tweets containing the specific hashtag #YUANenterprise

- Sentiment Analysis using Azure Text Analytics to evaluate tweet sentiment

- Negative Tweet Alert: If the sentiment score is below 0.5, the system sends an instant SMS alert via Twilio, including:

1. Sentiment score

2. Tweet user ID

## Workflow
1. Trigger Setup: The workflow is triggered whenever a new tweet contains #YUANenterprise.

2. Sentiment Analysis: Azure Cognitive Services – Text Analytics API is used to evaluate the sentiment of the tweet.

3. Decision and Notification:

- If the sentiment score is below 0.5

- Twilio sends an SMS alert to the designated user, warning of potential negative feedback

## System Architecture
- Azure Logic Apps: Automates the workflow

- Azure Cognitive Services - Text Analytics: Performs sentiment analysis

- Twilio API: Sends real-time SMS alerts

- Twitter API: Reads and monitors specific tweets

## Result Demonstration
Automatic Detection of Tweets with Hashtag #YUANenterprise:

![image](https://github.com/giraffeiscute/azure-project-tweeter-sentiment-tracking/blob/main/result/twitter.png)


Negative Tweet Alert via Twilio SMS (score < 0.5):  

<img src="https://github.com/giraffeiscute/azure-project-tweeter-sentiment-tracking/blob/main/result/%E7%B0%A1%E8%A8%8A.jpg" alt="image" width="350">

## Reference
Chen, Xiao-Xiong (Oct 2018). Building a Twitter Sentiment Monitoring System Using Azure Logic Apps



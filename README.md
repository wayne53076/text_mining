# Final Project: Ted Bot

這個專案使用文件探勘的技術，旨在幫助使用者找到他們感興趣的 Ted 演講。

# 使用技術

## 爬蟲

Ted Bot 使用 Selenium 爬取 TED 網站上的動態生成內容。以下是爬蟲的主要步驟：

 - 循環遍歷 TED 網站上的多個頁面，找到每個頁面上的話題。
 - 對於每個話題，打開該話題的 URL，點擊 "Read transcript" 按鈕並解析字幕。
 - 將每個話題的標題、字幕、URL 和發布日期保存在字典 topic_transcripts 中。

## 文本探勘
Ted Bot 使用以下技術來分析和理解演講內容：

 - word2vec: 建構特徵矩陣，用於理解演講中的詞彙和主題。
 - Clustering: 對演講進行分群，以找到每年、每月的常見關鍵字。

## 自然語言處理
Ted Bot 使用預訓練模型 BERT 來進行以下任務：
 - 摘要生成：生成演講的摘要。
 - 問答系統：回答有關演講內容的問題。
 - 情感分析：分析演講中的情感和情緒。
## API 整合
Ted Bot 整合了 OpenAI 的 API，利用embedding來提升演講內容的理解和表達。


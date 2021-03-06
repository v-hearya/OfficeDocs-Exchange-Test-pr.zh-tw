﻿---
title: '變更的音訊轉碼器: Exchange Online Help'
TOCTitle: 變更的音訊轉碼器
ms:assetid: 139b2ccd-28c5-46c0-9050-777f4f59aade
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/Aa996342(v=EXCHG.150)
ms:contentKeyID: 50472602
ms.date: 05/23/2018
mtps_version: v=EXCHG.150
ms.translationtype: MT
---

# 變更的音訊轉碼器

 

_**適用版本：** Exchange Online, Exchange Server 2013, Exchange Server 2016_

_**上次修改主題的時間：** 2013-02-22_

整合的通訊可以使用其中一個四種轉碼器建立語音郵件訊息的 ︰ MP3、 Windows Media Audio (WMA)、 群組系統電話 (GSM) 06.10 及 G.711 脈衝代碼調變 (PCM) 線性。根據預設，當您建立整合通訊 (UM) 撥號 UM 撥號對應表會使用到記錄的語音訊息 MP3 音訊轉碼器。MP3 音訊格式是跨多個作業系統、 電子郵件用戶端和 MP3 播放器所使用的熱門音訊格式。建立 UM 撥號對應表之後，您可以設定 UM 撥號對應表使用其中一種其他包括 WMA、 GSM 06.10 或 G.711 PCM 線性音訊轉碼器的音訊格式。若要接聽語音訊息、 行動電話或電腦必須安裝相容的音訊軟體應用程式。

如需與 UM 撥號對應表相關的其他工作，請參閱[UM 撥號對應表規劃程序](um-dial-plan-procedures-exchange-2013-help.md)。

## 開始之前有哪些須知？

  - 預估完成時間： 少於 1 分鐘。

  - 您必須已獲指派權限，才能執行此程序或這些程序。若要查看您需要的權限，請參閱 [整合的通訊權限](unified-messaging-permissions-exchange-2013-help.md)主題中的「UM 撥號對應表」項目。

  - 在執行這些程序之前，請確認已建立 UM 撥號對應表。 如需詳細步驟，請參閱[建立 UM 撥號對應表](create-a-um-dial-plan-exchange-2013-help.md)。

  - 如需適用於此主題中程序的快速鍵相關資訊，請參閱 [Exchange 系統管理中心的鍵盤快速鍵](keyboard-shortcuts-in-the-exchange-admin-center-exchange-online-protection-help.md)。


> [!TIP]  
> 有問題嗎？在 Exchange 論壇中尋求協助。 論壇的網址為：<a href="https://go.microsoft.com/fwlink/p/?linkid=60612">Exchange Server</a>、 <a href="https://go.microsoft.com/fwlink/p/?linkid=267542">Exchange Online</a> 或 <a href="https://go.microsoft.com/fwlink/p/?linkid=285351">Exchange Online Protection</a>。.




## 您要執行的工作

## 使用 EAC 來變更整合通訊撥號對應表上的音訊轉碼器

1.  在 EAC 中，瀏覽至 \[整合通訊\] \> \[UM 撥號對應表\]。

2.  在清單檢視中，選取您要修改的 UM 撥號對應表，然後按一下 \[編輯\]![編輯圖示](images/JJ218640.6f53ccb2-1f13-4c02-bea0-30690e6ea71d(EXCHG.150).gif "編輯圖示")。

3.  在 \[UM 撥號對應表\] 頁面上，按一下 \[設定\]。

4.  在 \[設定\] 中的 \[音訊轉碼器\] 下，使用下拉式清單選取一個下列格式：
    
      - MP3
    
      - WMA
    
      - GSM
    
      - G711

5.  按一下 \[儲存\]。

## 使用命令介面來變更整合通訊撥號對應表上的音訊轉碼器

此範例會將名爲 `MyUMDialPlan` 之 UM 撥號對應表上的音訊轉碼器設為 G.711。

    Set-UMDialPlan -Identity MyUMDialPlan -AudioCodec G711

此範例會將名爲 `MyUMDialPlan` 之 UM 撥號對應表上的音訊轉碼器設為 WMA。

    Set-UMDialPlan -Identity MyUMDialPlan -AudioCodec Wma


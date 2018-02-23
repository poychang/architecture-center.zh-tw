---
title: "自然語言處理"
description: 
author: zoinerTejada
ms:date: 02/12/2018
ms.openlocfilehash: c03e2d017f9b4eb955a0e3494b5bc6c2603d1058
ms.sourcegitcommit: 90cf2de795e50571d597cfcb9b302e48933e7f18
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2018
---
# <a name="natural-language-processing"></a><span data-ttu-id="2d2a3-102">自然語言處理</span><span class="sxs-lookup"><span data-stu-id="2d2a3-102">Natural language processing</span></span>

<span data-ttu-id="2d2a3-103">自然語言處理 (NLP) 可用於多種工作，例如情感分析、主題偵測、語言偵測、關鍵片語擷取和文件分類。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-103">Natural language processing (NLP) is used for tasks such as sentiment analysis, topic detection, language detection, key phrase extraction, and document categorization.</span></span>

![](./images/nlp-pipeline.png)

## <a name="when-to-use-this-solution"></a><span data-ttu-id="2d2a3-104">使用此解決方案的時機</span><span class="sxs-lookup"><span data-stu-id="2d2a3-104">When to use this solution</span></span>

<span data-ttu-id="2d2a3-105">NLP 可用來進行文件分類，例如，將文件標示為機密或垃圾郵件。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-105">NLP can be use to classify documents, such as labeling documents as sensitive or spam.</span></span> <span data-ttu-id="2d2a3-106">NLP 的輸出可用於後續的查詢處理或搜尋。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-106">The output of NLP can be used for subsequent processing or search.</span></span> <span data-ttu-id="2d2a3-107">NLP 的另一項用途，是藉由識別文件中的實體來彙總文字。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-107">Another use for NLP is to summarize text by identifying the entities present in the document.</span></span> <span data-ttu-id="2d2a3-108">這些實體也可用來為文件標記關鍵字，而讓您能夠根據內容進行搜尋和擷取。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-108">These entities can also be used to tag documents with keywords, which enables search and retrieval based on content.</span></span> <span data-ttu-id="2d2a3-109">實體可合併為主題，並以摘要說明每個文件中的重要主題。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-109">Entities might be combined into topics, with summaries that describe the important topics present in each document.</span></span> <span data-ttu-id="2d2a3-110">偵測到的主題都可用來分類文件以供導覽，或根據選定的主題列舉相關文件。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-110">The detected topics may be used to categorize the documents for navigation, or to enumerate related documents given a selected topic.</span></span> <span data-ttu-id="2d2a3-111">NLP 的另一項用途是為文字進行情感評分，以評估文件的調性是正面還是負面的。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-111">Another use for NLP is to score text for sentiment, to assess the positive or negative tone of a document.</span></span> <span data-ttu-id="2d2a3-112">這些方法都用到許多來自於自然語言處理的技術，例如：</span><span class="sxs-lookup"><span data-stu-id="2d2a3-112">These approaches use many techniques from natural language processing, such as:</span></span> 

- <span data-ttu-id="2d2a3-113">**權杖化工具**。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-113">**Tokenizer**.</span></span> <span data-ttu-id="2d2a3-114">將文字分割成單字或片語。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-114">Splitting the text into words or phrases.</span></span>
- <span data-ttu-id="2d2a3-115">**詞幹分析和詞形歸併還原**。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-115">**Stemming and lemmatization**.</span></span> <span data-ttu-id="2d2a3-116">將單字正規化，使不同的形態會對應至具有相同意義的常態單字。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-116">Normalizing words so that that different forms map to the canonical word with the same meaning.</span></span> <span data-ttu-id="2d2a3-117">例如，"running" 和 "ran" 會對應至 "run"。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-117">For example, "running" and "ran" map to "run."</span></span> 
- <span data-ttu-id="2d2a3-118">**實體擷取**。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-118">**Entity extraction**.</span></span> <span data-ttu-id="2d2a3-119">識別文字中的主題。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-119">Identifying subjects in the text.</span></span>
- <span data-ttu-id="2d2a3-120">**詞性偵測**。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-120">**Part of speech detection**.</span></span> <span data-ttu-id="2d2a3-121">將文字識別為動詞、名詞、分詞、動詞片語等等。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-121">Identifying text as a verb, noun, participle, verb phrase, and so on.</span></span>
- <span data-ttu-id="2d2a3-122">**文句界限偵測**。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-122">**Sentence boundary detection**.</span></span> <span data-ttu-id="2d2a3-123">偵測文字段落內的完整句子。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-123">Detecting complete sentences within paragraphs of text.</span></span>

<span data-ttu-id="2d2a3-124">使用 NLP 從自由格式文字中擷取資訊和深入資訊時，通常會先從物件儲存體 (例如 Azure 儲存體或 Azure Data Lake Store) 中儲存的原始文件開始著手。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-124">When using NLP to extract information and insight from free-form text, the starting point is typically the raw documents stored in object storage such as Azure Storage or Azure Data Lake Store.</span></span> 

## <a name="challenges"></a><span data-ttu-id="2d2a3-125">挑戰</span><span class="sxs-lookup"><span data-stu-id="2d2a3-125">Challenges</span></span>

- <span data-ttu-id="2d2a3-126">處理自由格式文字文件的集合，通常需要耗費大量的計算資源和時間。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-126">Processing a collection of free-form text documents is typically computationally resource intensive, as well as being time intensive.</span></span>
- <span data-ttu-id="2d2a3-127">若沒有標準化的文件格式，使用自由格式文字處理來擷取文件中的特定事實時，可能非常難以達到一貫精確的結果。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-127">Without a standardized document format, it can be very difficult to achieve consistently accurate results using free-form text processing to extract specific facts from a document.</span></span> <span data-ttu-id="2d2a3-128">以發票的文字表示法為例 &mdash; 要建置可對任意數目的供應商提供的發票正確擷取發票號碼和發票日期的程序，可能非常不容易。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-128">For example, think of a text representation of an invoice&mdash;it can be difficult to build a process that correctly extracts the invoice number and invoice date for invoices across any number of vendors.</span></span>

## <a name="architecture"></a><span data-ttu-id="2d2a3-129">架構</span><span class="sxs-lookup"><span data-stu-id="2d2a3-129">Architecture</span></span>

<span data-ttu-id="2d2a3-130">在 NLP 解決方案中，會對包含文字段落的文件執行自由格式文字處理。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-130">In an NLP solution, free-form text processing is performed against documents containing paragraphs of text.</span></span> <span data-ttu-id="2d2a3-131">整體架構可以是[批次處理](./batch-processing.md)或[即時串流處理](./real-time-processing.md)架構。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-131">The overall architecture can be a [batch processing](./batch-processing.md) or [real-time stream processing](./real-time-processing.md) architecture.</span></span>

<span data-ttu-id="2d2a3-132">實際的處理會隨著所需的結果而不同，但就管線而言，NLP 可能會以批次或即時的方式套用。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-132">The actual processing varies based on the desired outcome, but in terms of the pipeline, NLP may be applied in a batch or real-time fashion.</span></span> <span data-ttu-id="2d2a3-133">例如，針對文字區塊可以使用情感分析，以產生情感分數。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-133">For example, sentiment analysis can be used against blocks of text to produce a sentiment score.</span></span> <span data-ttu-id="2d2a3-134">此作業可藉由對儲存體中的資料執行批次程序來完成，或即時使用透過傳訊服務傳遞的較小資料區塊來完成。</span><span class="sxs-lookup"><span data-stu-id="2d2a3-134">This can could be done by running a batch process against data in storage, or in real time using smaller chunks of data flowing through a messaging service.</span></span>

## <a name="technology-choices"></a><span data-ttu-id="2d2a3-135">技術選擇</span><span class="sxs-lookup"><span data-stu-id="2d2a3-135">Technology choices</span></span>

- [<span data-ttu-id="2d2a3-136">自然語言處理</span><span class="sxs-lookup"><span data-stu-id="2d2a3-136">Natural language processing</span></span>](../technology-choices/natural-language-processing.md)
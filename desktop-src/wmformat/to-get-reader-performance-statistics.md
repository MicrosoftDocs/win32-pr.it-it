---
title: Per ottenere le statistiche sulle prestazioni del lettore
description: Per ottenere le statistiche sulle prestazioni del lettore
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- ASF (Advanced Systems Format), statistiche sulle prestazioni del lettore
- ASF (formato avanzato dei sistemi), statistiche sulle prestazioni del lettore
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- ASF (Advanced Systems Format), statistiche sulle prestazioni
- ASF (formato avanzato dei sistemi), statistiche sulle prestazioni
- lettori asincroni, statistiche sulle prestazioni
- prestazioni, statistiche del lettore
- prestazioni, lettori asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5484b211f2c2d1e9ad4cf9aac3773c7946757c2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858002"
---
# <a name="to-get-reader-performance-statistics"></a><span data-ttu-id="f2fcc-112">Per ottenere le statistiche sulle prestazioni del lettore</span><span class="sxs-lookup"><span data-stu-id="f2fcc-112">To Get Reader Performance Statistics</span></span>

<span data-ttu-id="f2fcc-113">Quando si leggono i file localmente con il lettore asincrono, non è necessario verificare le prestazioni delle operazioni di lettura.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-113">When reading files locally with the asynchronous reader, it is not necessary to check the performance of reading operations.</span></span> <span data-ttu-id="f2fcc-114">Se l'applicazione sta leggendo da un'origine di flusso, tuttavia, le statistiche sulle prestazioni possono essere molto importanti.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-114">If your application is reading from a streaming source however, performance statistics can be very important.</span></span> <span data-ttu-id="f2fcc-115">L'applicazione può rispondere alle modifiche nelle prestazioni di riproduzione per garantire la migliore esperienza utente finale.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-115">Your application can respond to changes in playback performance to ensure the best possible end-user experience.</span></span>

<span data-ttu-id="f2fcc-116">Le informazioni sulle prestazioni che è possibile recuperare dal Reader includono le statistiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2fcc-116">The performance information you can retrieve from the reader includes the following statistics:</span></span>

-   <span data-ttu-id="f2fcc-117">Larghezza di banda corrente della connessione.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-117">The current bandwidth of the connection.</span></span>
-   <span data-ttu-id="f2fcc-118">Numero di pacchetti ricevuti dal server.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-118">The number of packets received from the server.</span></span>
-   <span data-ttu-id="f2fcc-119">Numero di pacchetti persi recuperati.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-119">The number of lost packets that were recovered.</span></span>
-   <span data-ttu-id="f2fcc-120">Numero di pacchetti persi che non sono stati recuperati.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-120">The number of lost packets that were not recovered.</span></span>
-   <span data-ttu-id="f2fcc-121">Percentuale del numero totale di pacchetti inviati ricevuti.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-121">The percentage of the total number of packets sent that have been received.</span></span>

<span data-ttu-id="f2fcc-122">Per ottenere le statistiche sulle prestazioni del lettore, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-122">To get reader performance statistics, perform the following steps.</span></span>

1.  <span data-ttu-id="f2fcc-123">Prima di iniziare la riproduzione, creare una struttura di [**\_ \_ statistiche di WM Reader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) .</span><span class="sxs-lookup"><span data-stu-id="f2fcc-123">Before starting playback, create a [**WM\_READER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) structure.</span></span> <span data-ttu-id="f2fcc-124">È necessario impostare il membro **cbSize** su sizeof (statistiche di WM \_ Reader \_ ).</span><span class="sxs-lookup"><span data-stu-id="f2fcc-124">You must set the **cbSize** member to sizeof(WM\_READER\_STATISTICS).</span></span>
2.  <span data-ttu-id="f2fcc-125">Ottenere un puntatore all'interfaccia [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) dell'oggetto Reader chiamando **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-125">Obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="f2fcc-126">Durante la riproduzione, eseguire le chiamate a [**IWMReaderAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) di frequente per monitorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-126">During playback, make calls to [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) frequently to monitor performance.</span></span> <span data-ttu-id="f2fcc-127">Passare la struttura delle **\_ \_ statistiche di WM Reader** a ogni chiamata ed esaminare i membri appropriati.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-127">Pass your **WM\_READER\_STATISTICS** structure with each call and examine the appropriate members.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2fcc-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2fcc-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2fcc-129">**Lettura di file con il lettore asincrono**</span><span class="sxs-lookup"><span data-stu-id="f2fcc-129">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 





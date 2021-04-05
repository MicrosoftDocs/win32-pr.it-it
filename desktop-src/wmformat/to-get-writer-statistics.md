---
title: Per ottenere le statistiche del writer
description: Per ottenere le statistiche del writer
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- ASF (Advanced Systems Format), statistiche del writer
- ASF (formato avanzato dei sistemi), statistiche del writer
- Statistiche writer, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103956266"
---
# <a name="to-get-writer-statistics"></a><span data-ttu-id="9092b-106">Per ottenere le statistiche del writer</span><span class="sxs-lookup"><span data-stu-id="9092b-106">To Get Writer Statistics</span></span>

<span data-ttu-id="9092b-107">Il writer può fornire informazioni statistiche sulle operazioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="9092b-107">The writer can provide statistical information about writing operations.</span></span> <span data-ttu-id="9092b-108">Esistono due metodi per raccogliere le statistiche del writer: [**IWMWriterAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) e [**IWMWriterAdvanced3:: GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span><span class="sxs-lookup"><span data-stu-id="9092b-108">There are two methods for gathering writer statistics: [**IWMWriterAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) and [**IWMWriterAdvanced3::GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span></span> <span data-ttu-id="9092b-109">Le informazioni recuperate da **GetStatisticsEx** sono più specifiche delle informazioni recuperate da **GetStatistics**.</span><span class="sxs-lookup"><span data-stu-id="9092b-109">The information retrieved by **GetStatisticsEx** is more specific than the information retrieved by **GetStatistics**.</span></span>

<span data-ttu-id="9092b-110">Entrambi i metodi popolano le strutture con informazioni statistiche.</span><span class="sxs-lookup"><span data-stu-id="9092b-110">Both methods populate structures with statistical information.</span></span> <span data-ttu-id="9092b-111">**GetStatistics** usa la struttura delle [**\_ \_ statistiche del writer WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) , mentre **GetStatisticsEx** usa la struttura [**ex di WM \_ writer \_ Statistics \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) .</span><span class="sxs-lookup"><span data-stu-id="9092b-111">**GetStatistics** uses the [**WM\_WRITER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) structure, and **GetStatisticsEx** uses the [**WM\_WRITER\_STATISTICS\_EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) structure.</span></span> <span data-ttu-id="9092b-112">**GetStatisticsEx** non duplica i dati ottenuti da **GetStatistics**.</span><span class="sxs-lookup"><span data-stu-id="9092b-112">**GetStatisticsEx** does not duplicate the data obtained by **GetStatistics**.</span></span> <span data-ttu-id="9092b-113">Per informazioni più complete, è necessario chiamare entrambi i metodi.</span><span class="sxs-lookup"><span data-stu-id="9092b-113">For the most complete information, you should call both methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9092b-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9092b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9092b-115">**Interfaccia IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="9092b-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="9092b-116">**Interfaccia IWMWriterAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="9092b-116">**IWMWriterAdvanced3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[<span data-ttu-id="9092b-117">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="9092b-117">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 





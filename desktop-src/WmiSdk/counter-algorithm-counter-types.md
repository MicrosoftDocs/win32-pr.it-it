---
description: I tipi di contatore dell'algoritmo contatore possono calcolare le frequenze o i byte medi per un campione o per un periodo di tempo per un'operazione specifica.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Tipi di contatori dell'algoritmo contatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bd55a2a9cc9cc9193a86ffe740ebfa856c0ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346746"
---
# <a name="counter-algorithm-counter-types"></a><span data-ttu-id="20696-103">Tipi di contatori dell'algoritmo contatore</span><span class="sxs-lookup"><span data-stu-id="20696-103">Counter Algorithm Counter Types</span></span>

<span data-ttu-id="20696-104">I tipi di contatore dell'algoritmo contatore possono calcolare le frequenze o i byte medi per un campione o per un periodo di tempo per un'operazione specifica.</span><span class="sxs-lookup"><span data-stu-id="20696-104">Counter algorithm counter types may calculate rates or averages bytes for a sample or over a time period for a particular operation.</span></span>

<span data-ttu-id="20696-105">La proprietà **AvgDiskBytesPerTransfer** nella classe [**Win32 \_ PerfRawData \_ perfdisk \_ PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) usa l' \_ CounterType bulk media delle prestazioni \_ .</span><span class="sxs-lookup"><span data-stu-id="20696-105">The **AvgDiskBytesPerTransfer** property in the [**Win32\_PerfRawData\_PerfDisk\_PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) class uses the PERF\_AVERAGE\_BULK countertype.</span></span> <span data-ttu-id="20696-106">In questo caso, il trasferimento è l'operazione e il numero di byte di accumulo inviati è costituito dai dati del contatore.</span><span class="sxs-lookup"><span data-stu-id="20696-106">In this case, the transfer is the operation, and the accumulating number of bytes that are sent is the counter data.</span></span> <span data-ttu-id="20696-107">Per due esempi, dividendo la differenza tra i byte accumulati e la differenza nell'accumulo dei trasferimenti, viene generato il numero medio di byte per trasferimento durante il periodo tra gli esempi.</span><span class="sxs-lookup"><span data-stu-id="20696-107">For any two samples, dividing the difference of accumulated bytes by the difference in accumulating transfers will produce the average number of bytes per transfer during the period between the samples.</span></span>

<span data-ttu-id="20696-108">Sono disponibili gli algoritmi dei contatori seguenti:</span><span class="sxs-lookup"><span data-stu-id="20696-108">The following counter algorithms are provided:</span></span>



| <span data-ttu-id="20696-109">CounterType</span><span class="sxs-lookup"><span data-stu-id="20696-109">CounterType</span></span>                                                                                              | <span data-ttu-id="20696-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20696-110">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20696-111">[Prestazioni \_ 1073874176 \_ ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale in blocco medio</span><span class="sxs-lookup"><span data-stu-id="20696-111">[PERF\_AVERAGE\_BULK](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073874176</span></span><br/>       | <span data-ttu-id="20696-112">Numero medio di elementi elaborati durante un'operazione.</span><span class="sxs-lookup"><span data-stu-id="20696-112">Number of items processed, on average, during an operation.</span></span> <span data-ttu-id="20696-113">Questo tipo di contatore visualizza un rapporto tra gli elementi elaborati (ad esempio i byte inviati) e il numero di operazioni completate e richiede una proprietà di base con prestazioni \_ medie di \_ base come tipo di contatore.</span><span class="sxs-lookup"><span data-stu-id="20696-113">This counter type displays a ratio of the items processed (such as bytes sent) to the number of operations completed, and requires a base property with PERF\_AVERAGE\_BASE as the counter type.</span></span> |
| <span data-ttu-id="20696-114">[Prestazioni \_ Contatore \_ contatore decimale](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))272696320</span><span class="sxs-lookup"><span data-stu-id="20696-114">[PERF\_COUNTER\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696320</span></span><br/>     | <span data-ttu-id="20696-115">Numero medio di operazioni completate durante ogni secondo dell'intervallo di campionamento.</span><span class="sxs-lookup"><span data-stu-id="20696-115">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="20696-116">.</span><span class="sxs-lookup"><span data-stu-id="20696-116">.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="20696-117">[Prestazioni \_ \_Contatore campione](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 4260864</span><span class="sxs-lookup"><span data-stu-id="20696-117">[PERF\_SAMPLE\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864</span></span><br/>        | <span data-ttu-id="20696-118">Numero medio di operazioni completate in un secondo.</span><span class="sxs-lookup"><span data-stu-id="20696-118">Average number of operations completed in one second.</span></span> <span data-ttu-id="20696-119">Questo tipo di contatore richiede una proprietà di base con la base di esempio delle prestazioni del tipo di contatore \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="20696-119">This counter type requires a base property with the counter type PERF\_SAMPLE\_BASE.</span></span>                                                                                                                   |
| <span data-ttu-id="20696-120">[Prestazioni \_ CONTATORE \_ \_ conteggio bulk numero](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 272696576</span><span class="sxs-lookup"><span data-stu-id="20696-120">[PERF\_COUNTER\_BULK\_COUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696576</span></span><br/> | <span data-ttu-id="20696-121">Numero medio di operazioni completate durante ogni secondo dell'intervallo di campionamento.</span><span class="sxs-lookup"><span data-stu-id="20696-121">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="20696-122">Questo tipo di contatore è identico al \_ \_ tipo di contatore di contatori delle prestazioni, ma usa campi di dimensioni maggiori per contenere valori più grandi.</span><span class="sxs-lookup"><span data-stu-id="20696-122">This counter type is the same as the PERF\_COUNTER\_COUNTER type, but it uses larger fields to accommodate larger values.</span></span>                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="20696-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="20696-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20696-124">Tipi di contatori delle prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="20696-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 


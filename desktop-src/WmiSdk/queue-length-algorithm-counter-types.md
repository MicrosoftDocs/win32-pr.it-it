---
description: I tipi di contatori degli algoritmi a lunghezza coda incrementano il numero di elementi in una coda a ogni intervallo di campionamento, come specificato dalla proprietà Frequency appropriata&\# 8212; Frequenza \_ PerfTime e così via.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Tipi di contatori degli algoritmi a lunghezza coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06665c2fb8fca014c7d722f0ea22cf7e86833ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226838"
---
# <a name="queue-length-algorithm-counter-types"></a><span data-ttu-id="4dd5c-103">Tipi di contatori degli algoritmi a lunghezza coda</span><span class="sxs-lookup"><span data-stu-id="4dd5c-103">Queue-length Algorithm Counter Types</span></span>

<span data-ttu-id="4dd5c-104">I tipi di contatori degli algoritmi a lunghezza coda incrementano il numero di elementi in una coda a ogni intervallo di campionamento, come specificato dalla frequenza di proprietà della frequenza appropriata \_ PerfTime e così via.</span><span class="sxs-lookup"><span data-stu-id="4dd5c-104">Queue-length algorithm counter types increment the number of items in a queue at each sample interval as specified by the appropriate frequency property Frequency\_PerfTime, and so on.</span></span> <span data-ttu-id="4dd5c-105">Il risultato cotto divide il numero di campioni per produrre la lunghezza media della coda.</span><span class="sxs-lookup"><span data-stu-id="4dd5c-105">The cooked result divides by the number of samples to produce the average queue length.</span></span>

<span data-ttu-id="4dd5c-106">Un esempio è la proprietà **AvgDiskQueueLength** in [**Win32 \_ PerfRawData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) che usa il contatore delle prestazioni 100 ns tipo di contatore di \_ \_ \_ tipo QUEUELEN \_ .</span><span class="sxs-lookup"><span data-stu-id="4dd5c-106">An example is the **AvgDiskQueueLength** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) that uses the PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE counter type.</span></span>



| <span data-ttu-id="4dd5c-107">Costante CounterType</span><span class="sxs-lookup"><span data-stu-id="4dd5c-107">CounterType Constant</span></span>                                                                                                 | <span data-ttu-id="4dd5c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dd5c-108">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd5c-109">[Prestazioni \_ COUNTER \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 4523008</span><span class="sxs-lookup"><span data-stu-id="4dd5c-109">[PERF\_COUNTER\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008</span></span><br/>            | <span data-ttu-id="4dd5c-110">Lunghezza media di una coda a una risorsa nel tempo.</span><span class="sxs-lookup"><span data-stu-id="4dd5c-110">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="4dd5c-111">Mostra la differenza tra le lunghezze di coda osservate durante gli ultimi due intervalli di campionamento divisa per la durata dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="4dd5c-111">It shows the difference between the queue lengths observed during the last two sample intervals divided by the duration of the interval.</span></span>                       |
| <span data-ttu-id="4dd5c-112">[Prestazioni \_ CONTATORE \_ di \_ \_ tipo QUEUELEN di grandi dimensioni](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 4523264</span><span class="sxs-lookup"><span data-stu-id="4dd5c-112">[PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264</span></span><br/>     | <span data-ttu-id="4dd5c-113">Lunghezza media di una coda a una risorsa nel tempo.</span><span class="sxs-lookup"><span data-stu-id="4dd5c-113">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="4dd5c-114">I contatori di questo tipo mostrano la differenza tra le lunghezze di coda osservate durante gli ultimi due intervalli di campionamento, divisa per la durata dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="4dd5c-114">Counters of this type display the difference between the queue lengths observed during the last two sample intervals, divided by the duration of the interval.</span></span> |
| <span data-ttu-id="4dd5c-115">[Prestazioni \_ COUNTER \_ 100 NS \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 5571840</span><span class="sxs-lookup"><span data-stu-id="4dd5c-115">[PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840</span></span><br/>     | <span data-ttu-id="4dd5c-116">Lunghezza media di una coda a una risorsa nel tempo in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="4dd5c-116">Average length of a queue to a resource over time in 100 nanosecond units.</span></span>                                                                                                                                        |
| <span data-ttu-id="4dd5c-117">[Prestazioni \_ COUNTER \_ obj \_ time \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 6620416</span><span class="sxs-lookup"><span data-stu-id="4dd5c-117">[PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416</span></span><br/> | <span data-ttu-id="4dd5c-118">Tempo in cui un oggetto si trova in una coda.</span><span class="sxs-lookup"><span data-stu-id="4dd5c-118">Time an object is in a queue.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="4dd5c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4dd5c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dd5c-120">Tipi di contatori delle prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="4dd5c-120">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 


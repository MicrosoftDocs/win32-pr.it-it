---
description: Ai tipi di contatori non computazionali non è associata una formula. Il valore non elaborato è direttamente significativo.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Tipi di contatori non computazionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ba2757f08dcb2256236117daf2ef3343004425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232401"
---
# <a name="noncomputational-counter-types"></a><span data-ttu-id="7e5f9-104">Tipi di contatori non computazionali</span><span class="sxs-lookup"><span data-stu-id="7e5f9-104">Noncomputational Counter Types</span></span>

<span data-ttu-id="7e5f9-105">Ai tipi di contatori non computazionali non è associata una formula.</span><span class="sxs-lookup"><span data-stu-id="7e5f9-105">Noncomputational counter types do not have an associated formula.</span></span> <span data-ttu-id="7e5f9-106">Il valore non elaborato è direttamente significativo.</span><span class="sxs-lookup"><span data-stu-id="7e5f9-106">The raw value is directly meaningful.</span></span>

<span data-ttu-id="7e5f9-107">La proprietà **FilesToBeIndexed** nella classe [**Win32 \_ PerfRawData \_ ContentIndex \_ IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) è un esempio del contatore delle prestazioni del contatore delle prestazioni di tipo **\_ \_ RAWCOUNT** .</span><span class="sxs-lookup"><span data-stu-id="7e5f9-107">The **FilesToBeIndexed** property in the [**Win32\_PerfRawData\_ContentIndex\_IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class is an example of the **PERF\_COUNTER\_RAWCOUNT** counter type.</span></span> <span data-ttu-id="7e5f9-108">Contiene un conteggio dei file che non sono stati indicizzati.</span><span class="sxs-lookup"><span data-stu-id="7e5f9-108">It contains a count of files that have not been indexed.</span></span>

<span data-ttu-id="7e5f9-109">I tipi di contatori sono designati dalla costante definita in Winperf. h, disponibile in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="7e5f9-109">Counter types are designated by the constant defined in Winperf.h located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7e5f9-110">Nella tabella seguente sono elencati i tipi di contatori non computazionali forniti.</span><span class="sxs-lookup"><span data-stu-id="7e5f9-110">The following table lists the noncomputational counter types that are provided.</span></span>



| <span data-ttu-id="7e5f9-111">CounterType</span><span class="sxs-lookup"><span data-stu-id="7e5f9-111">CounterType</span></span>                                                                                                 | <span data-ttu-id="7e5f9-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e5f9-112">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e5f9-113">[Prestazioni \_ \_Testo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale del contatore 2816</span><span class="sxs-lookup"><span data-stu-id="7e5f9-113">[PERF\_COUNTER\_TEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816</span></span><br/>                | <span data-ttu-id="7e5f9-114">Questo tipo di contatore mostra una stringa di testo a lunghezza variabile in Unicode.</span><span class="sxs-lookup"><span data-stu-id="7e5f9-114">This counter type shows a variable-length text string in Unicode.</span></span> <span data-ttu-id="7e5f9-115">Non vengono visualizzati i valori calcolati.</span><span class="sxs-lookup"><span data-stu-id="7e5f9-115">It does not display calculated values.</span></span>               |
| <span data-ttu-id="7e5f9-116">[Prestazioni \_ CONTATORE \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 65536</span><span class="sxs-lookup"><span data-stu-id="7e5f9-116">[PERF\_COUNTER\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536</span></span><br/>           | <span data-ttu-id="7e5f9-117">Valore del contatore non elaborato che non richiede calcoli e rappresenta un campione che è l'ultimo valore osservato.</span><span class="sxs-lookup"><span data-stu-id="7e5f9-117">Raw counter value that does not require calculations, and represents one sample which is the last observed value only.</span></span> |
| <span data-ttu-id="7e5f9-118">[Prestazioni \_ COUNTER \_ Large \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792</span><span class="sxs-lookup"><span data-stu-id="7e5f9-118">[PERF\_COUNTER\_LARGE\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792</span></span><br/>    | <span data-ttu-id="7e5f9-119">Uguale al **contatore delle prestazioni \_ \_ RAWCOUNT**, ma una rappresentazione a 64 bit per valori più grandi.</span><span class="sxs-lookup"><span data-stu-id="7e5f9-119">Same as **PERF\_COUNTER\_RAWCOUNT**, but a 64-bit representation for larger values.</span></span>                                    |
| <span data-ttu-id="7e5f9-120">[Prestazioni \_ CONTATORE \_ RAWCOUNT \_ esadecimale](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span><span class="sxs-lookup"><span data-stu-id="7e5f9-120">[PERF\_COUNTER\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span></span><br/>                  | <span data-ttu-id="7e5f9-121">Valore osservato più recentemente in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="7e5f9-121">Most recently observed value in hexadecimal format.</span></span> <span data-ttu-id="7e5f9-122">Non visualizza una media.</span><span class="sxs-lookup"><span data-stu-id="7e5f9-122">It does not display an average.</span></span>                                    |
| <span data-ttu-id="7e5f9-123">[Prestazioni \_ COUNTER \_ Large \_ RAWCOUNT \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))256</span><span class="sxs-lookup"><span data-stu-id="7e5f9-123">[PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256</span></span><br/> | <span data-ttu-id="7e5f9-124">Uguale al **contatore delle prestazioni \_ \_ RAWCOUNT \_ Hex**, ma una rappresentazione a 64 bit in esadecimale da usare con valori di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="7e5f9-124">Same as **PERF\_COUNTER\_RAWCOUNT\_HEX**, but a 64-bit representation in hexadecimal for use with large values.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7e5f9-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e5f9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e5f9-126">Tipi di contatori delle prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="7e5f9-126">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 


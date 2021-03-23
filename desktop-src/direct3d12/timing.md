---
title: Temporizzazione (grafica Direct3D 12)
description: In questa sezione viene illustrata l'esecuzione di query sui timestamp e la calibratura dei contatori di timestamp CPU e GPU.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: a1f58e231315e95bbf9178994f8c52303fc0d4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/21/2020
ms.locfileid: "104548897"
---
# <a name="timing-direct3d-12-graphics"></a><span data-ttu-id="f3c05-103">Temporizzazione (grafica Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="f3c05-103">Timing (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="f3c05-104">In questa sezione viene illustrata l'esecuzione di query sui timestamp e la calibratura dei contatori di timestamp CPU e GPU.</span><span class="sxs-lookup"><span data-stu-id="f3c05-104">This section covers querying timestamps, and calibrating the GPU and CPU timestamp counters.</span></span>

## <a name="timestamp-frequency"></a><span data-ttu-id="f3c05-105">Frequenza timestamp</span><span class="sxs-lookup"><span data-stu-id="f3c05-105">Timestamp frequency</span></span>

<span data-ttu-id="f3c05-106">L'applicazione può eseguire una query sulla frequenza del timestamp GPU in base alla coda per ogni comando (vedere il metodo [**ID3D12CommandQueue:: GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) ).</span><span class="sxs-lookup"><span data-stu-id="f3c05-106">Your application can query the GPU timestamp frequency on a per-command queue basis (refer to the [**ID3D12CommandQueue::GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) method).</span></span>

<span data-ttu-id="f3c05-107">La frequenza restituita è misurata in Hz (cicli/sec).</span><span class="sxs-lookup"><span data-stu-id="f3c05-107">The returned frequency is measured in Hz (ticks/sec).</span></span> <span data-ttu-id="f3c05-108">Se la coda di comandi specificata non supporta i timestamp (vedere la tabella nella sezione [query](queries.md) ), l'API ha esito negativo e restituisce **E_FAIL**.</span><span class="sxs-lookup"><span data-stu-id="f3c05-108">If the specified command queue doesn't support timestamps (see the table in the [Queries](queries.md) section), then this API fails (and returns **E_FAIL**).</span></span> <span data-ttu-id="f3c05-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) e [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) supportano sempre i timestamp.</span><span class="sxs-lookup"><span data-stu-id="f3c05-109">[**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) always support timestamps.</span></span> <span data-ttu-id="f3c05-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) supporta facoltativamente i timestamp se il membro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) è **true**.</span><span class="sxs-lookup"><span data-stu-id="f3c05-110">[**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) optionally supports timestamps if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

## <a name="timestamp-calibration"></a><span data-ttu-id="f3c05-111">Calibrazione timestamp</span><span class="sxs-lookup"><span data-stu-id="f3c05-111">Timestamp calibration</span></span>

<span data-ttu-id="f3c05-112">D3D12 consente alle applicazioni di correlare i risultati ottenuti dalle query timestamp con i risultati ottenuti dalla chiamata a `QueryPerformanceCounter` .</span><span class="sxs-lookup"><span data-stu-id="f3c05-112">D3D12 enables applications to correlate results obtained from timestamp queries with results obtained from calling `QueryPerformanceCounter`.</span></span> <span data-ttu-id="f3c05-113">Questo è abilitato dalla chiamata [**ID3D12CommandQueue:: GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).</span><span class="sxs-lookup"><span data-stu-id="f3c05-113">This is enabled by the call [**ID3D12CommandQueue::GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).</span></span>

<span data-ttu-id="f3c05-114">[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) campiona il contatore dei timestamp della GPU per una coda di comandi specificata ed esegue il campionamento del contatore della CPU `QueryPerformanceCounter` quasi allo stesso tempo.</span><span class="sxs-lookup"><span data-stu-id="f3c05-114">[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) samples the GPU timestamp counter for a given command queue and samples the CPU counter via `QueryPerformanceCounter` at nearly the same time.</span></span> <span data-ttu-id="f3c05-115">Anche in questo caso, l'API ha esito negativo \_ , se la coda di comandi specificata non supporta i timestamp, ovvero la restituzione di un errore. vedere la tabella nell'argomento [query](queries.md) .</span><span class="sxs-lookup"><span data-stu-id="f3c05-115">Again this API fails (returning E\_FAIL) if the specified command queue does not support timestamps (see the table in the [Queries](queries.md) topic).</span></span>

<span data-ttu-id="f3c05-116">Si noti che i contatori di timestamp della GPU e della CPU non sono necessariamente correlati direttamente alla velocità di clock di questi processori, ma funzionano invece con i tick del timestamp.</span><span class="sxs-lookup"><span data-stu-id="f3c05-116">Note that GPU and CPU timestamp counters are not necessarily directly related to the clock speed of these processors, but instead work from timestamp ticks.</span></span>

## <a name="timestamp-queries"></a><span data-ttu-id="f3c05-117">Query timestamp</span><span class="sxs-lookup"><span data-stu-id="f3c05-117">Timestamp queries</span></span>

<span data-ttu-id="f3c05-118">È possibile ottenere i timestamp come parte di un elenco di comandi, anziché una chiamata lato CPU in una coda di comandi, tramite le query timestamp.</span><span class="sxs-lookup"><span data-stu-id="f3c05-118">You can obtain timestamps as part of a command list (rather than a CPU-side call on a command queue) via timestamp queries.</span></span> <span data-ttu-id="f3c05-119">(Per altre informazioni sulle query in generale, vedere [query](queries.md) ).</span><span class="sxs-lookup"><span data-stu-id="f3c05-119">(See [Queries](queries.md) for more information about queries in general).</span></span> 

<span data-ttu-id="f3c05-120">Tutte le query timestamp utilizzano il tipo [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) per la query effettiva.</span><span class="sxs-lookup"><span data-stu-id="f3c05-120">All timestamp queries use the type [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) for the actual query.</span></span> <span data-ttu-id="f3c05-121">Tuttavia, a causa delle limitazioni hardware, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) e [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) utilizzano un [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) diverso da quello utilizzato da [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) .</span><span class="sxs-lookup"><span data-stu-id="f3c05-121">However, due to hardware limitations, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) and [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) use a different [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) from the one that [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) uses.</span></span>

<span data-ttu-id="f3c05-122">Le code Direct e COMPUTE utilizzano [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span><span class="sxs-lookup"><span data-stu-id="f3c05-122">Direct and compute queues use [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="f3c05-123">Le code di copia utilizzano [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span><span class="sxs-lookup"><span data-stu-id="f3c05-123">Copy queues use [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).</span></span>

<span data-ttu-id="f3c05-124">Le query della coda di copia sono supportate solo se il membro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) è **true**.</span><span class="sxs-lookup"><span data-stu-id="f3c05-124">Copy queue queries are supported only if the [**D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) member is **TRUE**.</span></span>

<span data-ttu-id="f3c05-125">Le query timestamp, dopo essere state risolte tramite [**ID3D12GraphicsCommandList:: ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), sono un **UInt64** che rappresenta i cicli, così come viene restituito da [**ID3D12CommandQueue:: GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)e, di conseguenza, deve essere diviso per la frequenza della coda per ottenere la lunghezza in secondi.</span><span class="sxs-lookup"><span data-stu-id="f3c05-125">Timestamp queries, once resolved via [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), are a **UINT64** that represents ticks, as is returned by [**ID3D12CommandQueue::GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration), and as such it must be divided by the queue frequency to get the length in seconds.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3c05-126">Per maggiore precisione, usare l'aritmetica a virgola mobile durante il calcolo di intervalli di secondi o millisecondi di timestamp.</span><span class="sxs-lookup"><span data-stu-id="f3c05-126">For accuracy, use floating-point arithmetic when calculating second or millisecond intervals of timestamps.</span></span> <span data-ttu-id="f3c05-127">Usare, ad esempio, `queriedTicks / (double)Frequency` invece di `queriedTicks / Frequency`.</span><span class="sxs-lookup"><span data-stu-id="f3c05-127">For example, use `queriedTicks / (double)Frequency` instead of `queriedTicks / Frequency`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3c05-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3c05-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3c05-129">Contatori e query</span><span class="sxs-lookup"><span data-stu-id="f3c05-129">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="f3c05-130">**ID3D12Device::SetStablePowerState**</span><span class="sxs-lookup"><span data-stu-id="f3c05-130">**ID3D12Device::SetStablePowerState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[<span data-ttu-id="f3c05-131">**ID3D12Object:: nome**</span><span class="sxs-lookup"><span data-stu-id="f3c05-131">**ID3D12Object::SetName**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[<span data-ttu-id="f3c05-132">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="f3c05-132">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[<span data-ttu-id="f3c05-133">Misurazione delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="f3c05-133">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>

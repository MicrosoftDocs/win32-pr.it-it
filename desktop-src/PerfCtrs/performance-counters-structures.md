---
description: Utilizzare le strutture seguenti quando si utilizzano i dati sulle prestazioni.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Strutture dei contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0629aa1763f08dfce9e2cc646bd1b5744d6591cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967501"
---
# <a name="performance-counters-structures"></a><span data-ttu-id="89150-103">Strutture dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="89150-103">Performance Counters Structures</span></span>

<span data-ttu-id="89150-104">Utilizzare le strutture seguenti quando si utilizzano i dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="89150-104">You use the following structures when working with performance data.</span></span>

<span data-ttu-id="89150-105">Per informazioni sulle funzioni disponibili per l'utilizzo dei contatori delle prestazioni, vedere [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="89150-105">For information about the functions that are available for working with performance counters, see [Performance Counters Functions](performance-counters-functions.md).</span></span>

## <a name="performance-data-helper-pdh-structures"></a><span data-ttu-id="89150-106">Strutture PDH (Performance Data Helper)</span><span class="sxs-lookup"><span data-stu-id="89150-106">Performance Data Helper (PDH) structures</span></span>

<span data-ttu-id="89150-107">I consumer che utilizzano le funzioni [PDH (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) utilizzano le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="89150-107">Consumers that use the [Performance Data Helper (PDH)](using-the-pdh-functions-to-consume-counter-data.md) functions use the following structures:</span></span>

- [<span data-ttu-id="89150-108">**PDH \_ esplorare \_ la \_ configurazione DLG**</span><span class="sxs-lookup"><span data-stu-id="89150-108">**PDH\_BROWSE\_DLG\_CONFIG**</span></span>](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [<span data-ttu-id="89150-109">**PDH \_ Browse \_ DLG \_ config \_ H**</span><span class="sxs-lookup"><span data-stu-id="89150-109">**PDH\_BROWSE\_DLG\_CONFIG\_H**</span></span>](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [<span data-ttu-id="89150-110">**\_info contatore \_ PDH**</span><span class="sxs-lookup"><span data-stu-id="89150-110">**PDH\_COUNTER\_INFO**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [<span data-ttu-id="89150-111">**\_elementi del \_ percorso del contatore PDH \_**</span><span class="sxs-lookup"><span data-stu-id="89150-111">**PDH\_COUNTER\_PATH\_ELEMENTS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [<span data-ttu-id="89150-112">**\_elementi del \_ percorso dell'elemento di dati PDH \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89150-112">**PDH\_DATA\_ITEM\_PATH\_ELEMENTS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [<span data-ttu-id="89150-113">**PDH \_ FMT \_ COUNTERVALUE**</span><span class="sxs-lookup"><span data-stu-id="89150-113">**PDH\_FMT\_COUNTERVALUE**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [<span data-ttu-id="89150-114">**\_ \_ elemento COUNTERVALUE di PDH FMT \_**</span><span class="sxs-lookup"><span data-stu-id="89150-114">**PDH\_FMT\_COUNTERVALUE\_ITEM**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [<span data-ttu-id="89150-115">**PDH \_ \_ contatore RAW**</span><span class="sxs-lookup"><span data-stu-id="89150-115">**PDH\_RAW\_COUNTER**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [<span data-ttu-id="89150-116">**PDH \_ \_ elemento contatore non elaborato \_**</span><span class="sxs-lookup"><span data-stu-id="89150-116">**PDH\_RAW\_COUNTER\_ITEM**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [<span data-ttu-id="89150-117">**\_record del \_ log non elaborato PDH \_**</span><span class="sxs-lookup"><span data-stu-id="89150-117">**PDH\_RAW\_LOG\_RECORD**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [<span data-ttu-id="89150-118">**\_statistiche PDH**</span><span class="sxs-lookup"><span data-stu-id="89150-118">**PDH\_STATISTICS**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [<span data-ttu-id="89150-119">**\_informazioni PDH tempo \_**</span><span class="sxs-lookup"><span data-stu-id="89150-119">**PDH\_TIME\_INFO**</span></span>](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a><span data-ttu-id="89150-120">Strutture consumer PerfLib V2</span><span class="sxs-lookup"><span data-stu-id="89150-120">PerfLib V2 Consumer structures</span></span>

<span data-ttu-id="89150-121">I consumer che usano le funzioni [consumer Perflib V2](using-the-perflib-functions-to-consume-counter-data.md) utilizzano le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="89150-121">Consumers that use the [PerfLib V2 Consumer](using-the-perflib-functions-to-consume-counter-data.md) functions use the following structures:</span></span>

- [<span data-ttu-id="89150-122">**\_dati contatore \_ prestazioni**</span><span class="sxs-lookup"><span data-stu-id="89150-122">**PERF\_COUNTER\_DATA**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [<span data-ttu-id="89150-123">**\_intestazione contatore \_ prestazioni**</span><span class="sxs-lookup"><span data-stu-id="89150-123">**PERF\_COUNTER\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [<span data-ttu-id="89150-124">**\_identificatore contatore \_ prestazioni**</span><span class="sxs-lookup"><span data-stu-id="89150-124">**PERF\_COUNTER\_IDENTIFIER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [<span data-ttu-id="89150-125">**\_ \_ informazioni reg contatore \_ prestazioni**</span><span class="sxs-lookup"><span data-stu-id="89150-125">**PERF\_COUNTER\_REG\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [<span data-ttu-id="89150-126">**\_ \_ informazioni reg del contatore delle prestazioni \_**</span><span class="sxs-lookup"><span data-stu-id="89150-126">**PERF\_COUNTERSET\_REG\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [<span data-ttu-id="89150-127">**\_intestazione dati \_ perf**</span><span class="sxs-lookup"><span data-stu-id="89150-127">**PERF\_DATA\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [<span data-ttu-id="89150-128">**\_intestazione dell'istanza Perf \_**</span><span class="sxs-lookup"><span data-stu-id="89150-128">**PERF\_INSTANCE\_HEADER**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [<span data-ttu-id="89150-129">**PRESTAZIONI \_ più \_ contatori**</span><span class="sxs-lookup"><span data-stu-id="89150-129">**PERF\_MULTI\_COUNTERS**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [<span data-ttu-id="89150-130">**più \_ istanze di perf \_**</span><span class="sxs-lookup"><span data-stu-id="89150-130">**PERF\_MULTI\_INSTANCES**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [<span data-ttu-id="89150-131">**\_ \_ intestazione buffer stringa \_ perf**</span><span class="sxs-lookup"><span data-stu-id="89150-131">**PERF\_STRING\_BUFFER\_HEADER**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [<span data-ttu-id="89150-132">**\_ \_ intestazione contatore della stringa Perf \_**</span><span class="sxs-lookup"><span data-stu-id="89150-132">**PERF\_STRING\_COUNTER\_HEADER**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a><span data-ttu-id="89150-133">Strutture del provider PerfLib V2</span><span class="sxs-lookup"><span data-stu-id="89150-133">PerfLib V2 Provider structures</span></span>

<span data-ttu-id="89150-134">[V2 i provider di dati sulle prestazioni](providing-counter-data-using-version-2-0.md) utilizzano le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="89150-134">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following structures:</span></span>

- [<span data-ttu-id="89150-135">**\_identità contatore \_ prestazioni**</span><span class="sxs-lookup"><span data-stu-id="89150-135">**PERF\_COUNTER\_IDENTITY**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="89150-136">**\_informazioni contatore \_ prestazioni**</span><span class="sxs-lookup"><span data-stu-id="89150-136">**PERF\_COUNTER\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="89150-137">**informazioni sul contatore delle prestazioni \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89150-137">**PERF\_COUNTERSET\_INFO**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="89150-138">**istanza del contatore delle prestazioni \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89150-138">**PERF\_COUNTERSET\_INSTANCE**</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [<span data-ttu-id="89150-139">**\_contesto del provider Perf \_**</span><span class="sxs-lookup"><span data-stu-id="89150-139">**PERF\_PROVIDER\_CONTEXT**</span></span>](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a><span data-ttu-id="89150-140">Strutture DLL di prestazioni</span><span class="sxs-lookup"><span data-stu-id="89150-140">Performance DLL structures</span></span>

<span data-ttu-id="89150-141">I [provider di dll dell'estensione](providing-counter-data-using-a-performance-dll.md) per le prestazioni e [gli utenti che utilizzano le funzioni del registro di sistema per](using-the-registry-functions-to-consume-counter-data.md) utilizzare i dati del contatore utilizzano le seguenti strutture</span><span class="sxs-lookup"><span data-stu-id="89150-141">[Performance extension DLL providers](providing-counter-data-using-a-performance-dll.md) and [consumers that use the registry functions to consume counter data](using-the-registry-functions-to-consume-counter-data.md) use the following structures:</span></span>

- [<span data-ttu-id="89150-142">**\_blocco contatore \_ prestazioni**</span><span class="sxs-lookup"><span data-stu-id="89150-142">**PERF\_COUNTER\_BLOCK**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [<span data-ttu-id="89150-143">**\_definizione del contatore delle prestazioni \_**</span><span class="sxs-lookup"><span data-stu-id="89150-143">**PERF\_COUNTER\_DEFINITION**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [<span data-ttu-id="89150-144">**\_blocco di dati Perf \_**</span><span class="sxs-lookup"><span data-stu-id="89150-144">**PERF\_DATA\_BLOCK**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [<span data-ttu-id="89150-145">**\_definizione dell'istanza di perf \_**</span><span class="sxs-lookup"><span data-stu-id="89150-145">**PERF\_INSTANCE\_DEFINITION**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [<span data-ttu-id="89150-146">**\_tipo di oggetto Perf \_**</span><span class="sxs-lookup"><span data-stu-id="89150-146">**PERF\_OBJECT\_TYPE**</span></span>](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)

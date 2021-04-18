---
description: Utilizzare le funzioni seguenti per utilizzare e fornire dati sulle prestazioni.
ms.assetid: a2c97b8b-b1b1-4dd8-8f23-edffaa74d028
title: Funzioni dei contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8ef01ac07ae8507f1005839ab838e2528e76d6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312124"
---
# <a name="performance-counters-functions"></a><span data-ttu-id="d538e-103">Funzioni dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="d538e-103">Performance Counters Functions</span></span>

<span data-ttu-id="d538e-104">Utilizzare le funzioni seguenti per utilizzare e fornire dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="d538e-104">Use the following functions to consume and provide performance data.</span></span>

## <a name="consumer-functions"></a><span data-ttu-id="d538e-105">Funzioni consumer</span><span class="sxs-lookup"><span data-stu-id="d538e-105">Consumer functions</span></span>

### <a name="performance-data-helper-pdh-functions"></a><span data-ttu-id="d538e-106">Funzioni PDH (Performance Data Helper)</span><span class="sxs-lookup"><span data-stu-id="d538e-106">Performance Data Helper (PDH) functions</span></span>

<span data-ttu-id="d538e-107">Utilizzare le funzioni PDH (Performance Data Helper) per utilizzare i dati sulle prestazioni dai provider di dati delle prestazioni V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="d538e-107">Use the Performance Data Helper (PDH) functions to consume performance data from both V1 and V2 performance data providers.</span></span>

> [!Note]
> <span data-ttu-id="d538e-108">Le app OneCore di Windows non possono usare le funzioni PDH.</span><span class="sxs-lookup"><span data-stu-id="d538e-108">Windows OneCore apps cannot use the PDH functions.</span></span> <span data-ttu-id="d538e-109">Se si stanno scrivendo app OneCore di Windows, usare le [funzioni consumer di Perflib V2](using-the-perflib-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="d538e-109">If you are writing Windows OneCore apps, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

- [<span data-ttu-id="d538e-110">*CounterPathCallBack*</span><span class="sxs-lookup"><span data-stu-id="d538e-110">*CounterPathCallBack*</span></span>](/windows/desktop/api/Pdh/nc-pdh-counterpathcallback)
- [<span data-ttu-id="d538e-111">**Chiamata PdhAddCounter**</span><span class="sxs-lookup"><span data-stu-id="d538e-111">**PdhAddCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera)
- [<span data-ttu-id="d538e-112">**PdhAddEnglishCounter**</span><span class="sxs-lookup"><span data-stu-id="d538e-112">**PdhAddEnglishCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)
- [<span data-ttu-id="d538e-113">**PdhBindInputDataSource**</span><span class="sxs-lookup"><span data-stu-id="d538e-113">**PdhBindInputDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)
- [<span data-ttu-id="d538e-114">**PdhBrowseCounters**</span><span class="sxs-lookup"><span data-stu-id="d538e-114">**PdhBrowseCounters**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa)
- [<span data-ttu-id="d538e-115">**PdhBrowseCountersH**</span><span class="sxs-lookup"><span data-stu-id="d538e-115">**PdhBrowseCountersH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersha)
- [<span data-ttu-id="d538e-116">**PdhCalculateCounterFromRawValue**</span><span class="sxs-lookup"><span data-stu-id="d538e-116">**PdhCalculateCounterFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue)
- [<span data-ttu-id="d538e-117">**PdhCloseLog**</span><span class="sxs-lookup"><span data-stu-id="d538e-117">**PdhCloseLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog)
- [<span data-ttu-id="d538e-118">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="d538e-118">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="d538e-119">**PdhCollectQueryData**</span><span class="sxs-lookup"><span data-stu-id="d538e-119">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="d538e-120">**PdhCollectQueryDataEx**</span><span class="sxs-lookup"><span data-stu-id="d538e-120">**PdhCollectQueryDataEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex)
- [<span data-ttu-id="d538e-121">**PdhCollectQueryDataWithTime**</span><span class="sxs-lookup"><span data-stu-id="d538e-121">**PdhCollectQueryDataWithTime**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydatawithtime)
- [<span data-ttu-id="d538e-122">**PdhComputeCounterStatistics**</span><span class="sxs-lookup"><span data-stu-id="d538e-122">**PdhComputeCounterStatistics**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics)
- [<span data-ttu-id="d538e-123">**PdhConnectMachine**</span><span class="sxs-lookup"><span data-stu-id="d538e-123">**PdhConnectMachine**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhconnectmachinea)
- [<span data-ttu-id="d538e-124">**PdhEnumLogSetNames**</span><span class="sxs-lookup"><span data-stu-id="d538e-124">**PdhEnumLogSetNames**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumlogsetnamesa)
- [<span data-ttu-id="d538e-125">**PdhEnumMachines**</span><span class="sxs-lookup"><span data-stu-id="d538e-125">**PdhEnumMachines**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesa)
- [<span data-ttu-id="d538e-126">**PdhEnumMachinesH**</span><span class="sxs-lookup"><span data-stu-id="d538e-126">**PdhEnumMachinesH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesha)
- [<span data-ttu-id="d538e-127">**PdhEnumObjectItems**</span><span class="sxs-lookup"><span data-stu-id="d538e-127">**PdhEnumObjectItems**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)
- [<span data-ttu-id="d538e-128">**PdhEnumObjectItemsH**</span><span class="sxs-lookup"><span data-stu-id="d538e-128">**PdhEnumObjectItemsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsha)
- [<span data-ttu-id="d538e-129">**PdhEnumObjects**</span><span class="sxs-lookup"><span data-stu-id="d538e-129">**PdhEnumObjects**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa)
- [<span data-ttu-id="d538e-130">**PdhEnumObjectsH**</span><span class="sxs-lookup"><span data-stu-id="d538e-130">**PdhEnumObjectsH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsha)
- [<span data-ttu-id="d538e-131">**PdhExpandCounterPath**</span><span class="sxs-lookup"><span data-stu-id="d538e-131">**PdhExpandCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandcounterpatha)
- [<span data-ttu-id="d538e-132">**PdhExpandWildCardPath**</span><span class="sxs-lookup"><span data-stu-id="d538e-132">**PdhExpandWildCardPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)
- [<span data-ttu-id="d538e-133">**PdhExpandWildCardPathH**</span><span class="sxs-lookup"><span data-stu-id="d538e-133">**PdhExpandWildCardPathH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpathha)
- [<span data-ttu-id="d538e-134">**PdhFormatFromRawValue**</span><span class="sxs-lookup"><span data-stu-id="d538e-134">**PdhFormatFromRawValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue)
- [<span data-ttu-id="d538e-135">**PdhGetCounterInfo**</span><span class="sxs-lookup"><span data-stu-id="d538e-135">**PdhGetCounterInfo**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcounterinfoa)
- [<span data-ttu-id="d538e-136">**PdhGetCounterTimeBase**</span><span class="sxs-lookup"><span data-stu-id="d538e-136">**PdhGetCounterTimeBase**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase)
- [<span data-ttu-id="d538e-137">**PdhGetDataSourceTimeRange**</span><span class="sxs-lookup"><span data-stu-id="d538e-137">**PdhGetDataSourceTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)
- [<span data-ttu-id="d538e-138">**PdhGetDataSourceTimeRangeH**</span><span class="sxs-lookup"><span data-stu-id="d538e-138">**PdhGetDataSourceTimeRangeH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangeh)
- [<span data-ttu-id="d538e-139">**PdhGetDefaultPerfCounter**</span><span class="sxs-lookup"><span data-stu-id="d538e-139">**PdhGetDefaultPerfCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcountera)
- [<span data-ttu-id="d538e-140">**PdhGetDefaultPerfCounterH**</span><span class="sxs-lookup"><span data-stu-id="d538e-140">**PdhGetDefaultPerfCounterH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcounterha)
- [<span data-ttu-id="d538e-141">**PdhGetDefaultPerfObject**</span><span class="sxs-lookup"><span data-stu-id="d538e-141">**PdhGetDefaultPerfObject**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjecta)
- [<span data-ttu-id="d538e-142">**PdhGetDefaultPerfObjectH**</span><span class="sxs-lookup"><span data-stu-id="d538e-142">**PdhGetDefaultPerfObjectH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjectha)
- [<span data-ttu-id="d538e-143">**PdhGetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="d538e-143">**PdhGetDllVersion**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetdllversion)
- [<span data-ttu-id="d538e-144">**PdhGetFormattedCounterArray**</span><span class="sxs-lookup"><span data-stu-id="d538e-144">**PdhGetFormattedCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya)
- [<span data-ttu-id="d538e-145">**PdhGetFormattedCounterValue**</span><span class="sxs-lookup"><span data-stu-id="d538e-145">**PdhGetFormattedCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)
- [<span data-ttu-id="d538e-146">**PdhGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="d538e-146">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
- [<span data-ttu-id="d538e-147">**PdhGetRawCounterArray**</span><span class="sxs-lookup"><span data-stu-id="d538e-147">**PdhGetRawCounterArray**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya)
- [<span data-ttu-id="d538e-148">**PdhGetRawCounterValue**</span><span class="sxs-lookup"><span data-stu-id="d538e-148">**PdhGetRawCounterValue**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)
- [<span data-ttu-id="d538e-149">**PdhIsRealTimeQuery**</span><span class="sxs-lookup"><span data-stu-id="d538e-149">**PdhIsRealTimeQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhisrealtimequery)
- [<span data-ttu-id="d538e-150">**PdhLookupPerfIndexByName**</span><span class="sxs-lookup"><span data-stu-id="d538e-150">**PdhLookupPerfIndexByName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfindexbynamea)
- [<span data-ttu-id="d538e-151">**PdhLookupPerfNameByIndex**</span><span class="sxs-lookup"><span data-stu-id="d538e-151">**PdhLookupPerfNameByIndex**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfnamebyindexa)
- [<span data-ttu-id="d538e-152">**PdhMakeCounterPath**</span><span class="sxs-lookup"><span data-stu-id="d538e-152">**PdhMakeCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha)
- [<span data-ttu-id="d538e-153">**PdhOpenLog**</span><span class="sxs-lookup"><span data-stu-id="d538e-153">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
- [<span data-ttu-id="d538e-154">**PdhOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="d538e-154">**PdhOpenQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya)
- [<span data-ttu-id="d538e-155">**PdhOpenQueryH**</span><span class="sxs-lookup"><span data-stu-id="d538e-155">**PdhOpenQueryH**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)
- [<span data-ttu-id="d538e-156">**PdhParseCounterPath**</span><span class="sxs-lookup"><span data-stu-id="d538e-156">**PdhParseCounterPath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha)
- [<span data-ttu-id="d538e-157">**PdhParseInstanceName**</span><span class="sxs-lookup"><span data-stu-id="d538e-157">**PdhParseInstanceName**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea)
- [<span data-ttu-id="d538e-158">**PdhReadRawLogRecord**</span><span class="sxs-lookup"><span data-stu-id="d538e-158">**PdhReadRawLogRecord**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhreadrawlogrecord)
- [<span data-ttu-id="d538e-159">**PdhRemoveCounter**</span><span class="sxs-lookup"><span data-stu-id="d538e-159">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="d538e-160">**PdhSelectDataSource**</span><span class="sxs-lookup"><span data-stu-id="d538e-160">**PdhSelectDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea)
- [<span data-ttu-id="d538e-161">**PdhSetCounterScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="d538e-161">**PdhSetCounterScaleFactor**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)
- [<span data-ttu-id="d538e-162">**PdhSetDefaultRealTimeDataSource**</span><span class="sxs-lookup"><span data-stu-id="d538e-162">**PdhSetDefaultRealTimeDataSource**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetdefaultrealtimedatasource)
- [<span data-ttu-id="d538e-163">**PdhSetQueryTimeRange**</span><span class="sxs-lookup"><span data-stu-id="d538e-163">**PdhSetQueryTimeRange**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange)
- [<span data-ttu-id="d538e-164">**PdhUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="d538e-164">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
- [<span data-ttu-id="d538e-165">**PdhUpdateLogFileCatalog**</span><span class="sxs-lookup"><span data-stu-id="d538e-165">**PdhUpdateLogFileCatalog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdatelogfilecatalog)
- [<span data-ttu-id="d538e-166">**PdhValidatePath**</span><span class="sxs-lookup"><span data-stu-id="d538e-166">**PdhValidatePath**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha)
- [<span data-ttu-id="d538e-167">**PdhValidatePathEx**</span><span class="sxs-lookup"><span data-stu-id="d538e-167">**PdhValidatePathEx**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepathexa)

### <a name="perflib-v2-consumer-functions"></a><span data-ttu-id="d538e-168">Funzioni consumer PerfLib V2</span><span class="sxs-lookup"><span data-stu-id="d538e-168">PerfLib V2 Consumer functions</span></span>

<span data-ttu-id="d538e-169">Usare le funzioni consumer PerfLib V2 per usare i dati sulle prestazioni dei provider di dati prestazioni V2 se non è possibile usare le funzioni PDH (Performance Data Helper).</span><span class="sxs-lookup"><span data-stu-id="d538e-169">Use the PerfLib V2 Consumer functions to consume performance data from V2 performance data providers if you cannot use the Performance Data Helper (PDH) functions.</span></span> <span data-ttu-id="d538e-170">Queste funzioni possono essere usate durante la scrittura di applicazioni OneCore per la raccolta di V2 CounterSet o quando è necessario raccogliere CounterSet V2 specifiche con dipendenze minime e overhead.</span><span class="sxs-lookup"><span data-stu-id="d538e-170">These functions might be used when writing OneCore applications to collect V2 countersets or when you need to collect specific V2 countersets with minimal dependencies and overhead.</span></span>

> [!TIP]
> <span data-ttu-id="d538e-171">Le funzioni consumer PerfLib V2 sono più difficili da usare rispetto alle funzioni PDH (Performance Data Helper) e supportano solo la raccolta dei dati dai provider v2.</span><span class="sxs-lookup"><span data-stu-id="d538e-171">The PerfLib V2 Consumer functions are harder to use than the Performance Data Helper (PDH) functions and only support collecting data from V2 providers.</span></span> <span data-ttu-id="d538e-172">Le funzioni PDH dovrebbero essere preferite per la maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d538e-172">The PDH functions should be preferred for most applications.</span></span>

- [<span data-ttu-id="d538e-173">**PerfAddCounters**</span><span class="sxs-lookup"><span data-stu-id="d538e-173">**PerfAddCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters)
- [<span data-ttu-id="d538e-174">**PerfCloseQueryHandle**</span><span class="sxs-lookup"><span data-stu-id="d538e-174">**PerfCloseQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle)
- [<span data-ttu-id="d538e-175">**PerfDeleteCounters**</span><span class="sxs-lookup"><span data-stu-id="d538e-175">**PerfDeleteCounters**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters)
- [<span data-ttu-id="d538e-176">**PerfEnumerateCounterSet**</span><span class="sxs-lookup"><span data-stu-id="d538e-176">**PerfEnumerateCounterSet**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset)
- [<span data-ttu-id="d538e-177">**PerfEnumerateCounterSetInstances**</span><span class="sxs-lookup"><span data-stu-id="d538e-177">**PerfEnumerateCounterSetInstances**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances)
- [<span data-ttu-id="d538e-178">**PerfOpenQueryHandle**</span><span class="sxs-lookup"><span data-stu-id="d538e-178">**PerfOpenQueryHandle**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle)
- [<span data-ttu-id="d538e-179">**PerfQueryCounterData**</span><span class="sxs-lookup"><span data-stu-id="d538e-179">**PerfQueryCounterData**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata)
- [<span data-ttu-id="d538e-180">**PerfQueryCounterInfo**</span><span class="sxs-lookup"><span data-stu-id="d538e-180">**PerfQueryCounterInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo)
- [<span data-ttu-id="d538e-181">**PerfQueryCounterSetRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="d538e-181">**PerfQueryCounterSetRegistrationInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo)

## <a name="provider-functions"></a><span data-ttu-id="d538e-182">Funzioni del provider</span><span class="sxs-lookup"><span data-stu-id="d538e-182">Provider functions</span></span>

### <a name="perflib-v2-provider-functions"></a><span data-ttu-id="d538e-183">Funzioni del provider PerfLib V2</span><span class="sxs-lookup"><span data-stu-id="d538e-183">PerfLib V2 Provider functions</span></span>

<span data-ttu-id="d538e-184">[V2 i provider di dati sulle prestazioni](providing-counter-data-using-version-2-0.md) utilizzano le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d538e-184">[V2 performance data providers](providing-counter-data-using-version-2-0.md) use the following functions:</span></span>

- [<span data-ttu-id="d538e-185">*AllocateMemory*</span><span class="sxs-lookup"><span data-stu-id="d538e-185">*AllocateMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)
- [<span data-ttu-id="d538e-186">*ControlCallback*</span><span class="sxs-lookup"><span data-stu-id="d538e-186">*ControlCallback*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="d538e-187">**CounterCleanup**</span><span class="sxs-lookup"><span data-stu-id="d538e-187">**CounterCleanup**</span></span>](countercleanup.md)
- [<span data-ttu-id="d538e-188">**CounterInitialize**</span><span class="sxs-lookup"><span data-stu-id="d538e-188">**CounterInitialize**</span></span>](counterinitialize.md)
- [<span data-ttu-id="d538e-189">*FreeMemory*</span><span class="sxs-lookup"><span data-stu-id="d538e-189">*FreeMemory*</span></span>](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)
- [<span data-ttu-id="d538e-190">**PerfCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="d538e-190">**PerfCreateInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="d538e-191">**PerfDecrementULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="d538e-191">**PerfDecrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
- [<span data-ttu-id="d538e-192">**PerfDecrementULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="d538e-192">**PerfDecrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
- [<span data-ttu-id="d538e-193">**PerfDeleteInstance**</span><span class="sxs-lookup"><span data-stu-id="d538e-193">**PerfDeleteInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="d538e-194">**PerfIncrementULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="d538e-194">**PerfIncrementULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
- [<span data-ttu-id="d538e-195">**PerfIncrementULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="d538e-195">**PerfIncrementULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)
- [<span data-ttu-id="d538e-196">**PerfQueryInstance**</span><span class="sxs-lookup"><span data-stu-id="d538e-196">**PerfQueryInstance**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="d538e-197">**PerfSetCounterSetInfo**</span><span class="sxs-lookup"><span data-stu-id="d538e-197">**PerfSetCounterSetInfo**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="d538e-198">**PerfSetULongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="d538e-198">**PerfSetULongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="d538e-199">**PerfSetULongLongCounterValue**</span><span class="sxs-lookup"><span data-stu-id="d538e-199">**PerfSetULongLongCounterValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="d538e-200">**PerfSetCounterRefValue**</span><span class="sxs-lookup"><span data-stu-id="d538e-200">**PerfSetCounterRefValue**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="d538e-201">**PerfStartProvider**</span><span class="sxs-lookup"><span data-stu-id="d538e-201">**PerfStartProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="d538e-202">**PerfStartProviderEx**</span><span class="sxs-lookup"><span data-stu-id="d538e-202">**PerfStartProviderEx**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartproviderex)
- [<span data-ttu-id="d538e-203">**PerfStopProvider**</span><span class="sxs-lookup"><span data-stu-id="d538e-203">**PerfStopProvider**</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

> [!Note]
> <span data-ttu-id="d538e-204">Per installare e disinstallare i provider v2, usare gli strumenti **lodctr** e **unlodctr** .</span><span class="sxs-lookup"><span data-stu-id="d538e-204">To install and uninstall V2 providers, use the **lodctr** and **unlodctr** tools.</span></span> <span data-ttu-id="d538e-205">Non è possibile usare le funzioni **LoadPerfCounterTextStrings** e **UnloadPerfCounterTextStrings** per installare e disinstallare i provider v2.</span><span class="sxs-lookup"><span data-stu-id="d538e-205">The **LoadPerfCounterTextStrings** and **UnloadPerfCounterTextStrings** functions cannot be used to install and uninstall V2 providers.</span></span>

### <a name="performance-dll-functions"></a><span data-ttu-id="d538e-206">Funzioni DLL prestazioni</span><span class="sxs-lookup"><span data-stu-id="d538e-206">Performance DLL functions</span></span>

<span data-ttu-id="d538e-207">I [provider di dati delle prestazioni V1](providing-counter-data-using-a-performance-dll.md) implementano una dll che fornisce le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d538e-207">[V1 performance data providers](providing-counter-data-using-a-performance-dll.md) implement a DLL that provides the following functions:</span></span>

- [<span data-ttu-id="d538e-208">*ClosePerformanceData*</span><span class="sxs-lookup"><span data-stu-id="d538e-208">*ClosePerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_close_proc)
- [<span data-ttu-id="d538e-209">*CollectPerformanceData*</span><span class="sxs-lookup"><span data-stu-id="d538e-209">*CollectPerformanceData*</span></span>](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)
- <span data-ttu-id="d538e-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d538e-210">[*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))</span></span>

> [!Note]
> <span data-ttu-id="d538e-211">A causa di problemi di affidabilità e prestazioni significativi, i provider di dati delle prestazioni V1 sono deprecati.</span><span class="sxs-lookup"><span data-stu-id="d538e-211">Due to significant performance and reliability issues, V1 performance data providers are deprecated.</span></span> <span data-ttu-id="d538e-212">Sebbene sia comunque possibile utilizzare una DLL di estensione per le prestazioni per fornire i dati dei contatori, è consigliabile [creare un provider v2](providing-counter-data-using-version-2-0.md) .</span><span class="sxs-lookup"><span data-stu-id="d538e-212">Although you still can use a performance extension DLL to provide counter data, you are encouraged to [create a V2 provider](providing-counter-data-using-version-2-0.md) instead.</span></span> <span data-ttu-id="d538e-213">Si consiglia inoltre di sostituire i provider v1 esistenti con i provider v2.</span><span class="sxs-lookup"><span data-stu-id="d538e-213">You also are encouraged to replace existing V1 providers with V2 providers.</span></span>

<span data-ttu-id="d538e-214">È possibile installare e disinstallare i provider v1 usando gli strumenti **lodctr** e **unlodctr** oppure chiamando le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d538e-214">V1 providers can be installed and uninstalled using the **lodctr** and **unlodctr** tools or by calling the following functions:</span></span>

- [<span data-ttu-id="d538e-215">**LoadPerfCounterTextStrings**</span><span class="sxs-lookup"><span data-stu-id="d538e-215">**LoadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-loadperfcountertextstringsa)
- [<span data-ttu-id="d538e-216">**UnloadPerfCounterTextStrings**</span><span class="sxs-lookup"><span data-stu-id="d538e-216">**UnloadPerfCounterTextStrings**</span></span>](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)

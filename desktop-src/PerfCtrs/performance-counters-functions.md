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
# <a name="performance-counters-functions"></a>Funzioni dei contatori delle prestazioni

Utilizzare le funzioni seguenti per utilizzare e fornire dati sulle prestazioni.

## <a name="consumer-functions"></a>Funzioni consumer

### <a name="performance-data-helper-pdh-functions"></a>Funzioni PDH (Performance Data Helper)

Utilizzare le funzioni PDH (Performance Data Helper) per utilizzare i dati sulle prestazioni dai provider di dati delle prestazioni V1 e V2.

> [!Note]
> Le app OneCore di Windows non possono usare le funzioni PDH. Se si stanno scrivendo app OneCore di Windows, usare le [funzioni consumer di Perflib V2](using-the-perflib-functions-to-consume-counter-data.md).

- [*CounterPathCallBack*](/windows/desktop/api/Pdh/nc-pdh-counterpathcallback)
- [**Chiamata PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera)
- [**PdhAddEnglishCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)
- [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)
- [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa)
- [**PdhBrowseCountersH**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersha)
- [**PdhCalculateCounterFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue)
- [**PdhCloseLog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog)
- [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [**PdhCollectQueryDataEx**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex)
- [**PdhCollectQueryDataWithTime**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydatawithtime)
- [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics)
- [**PdhConnectMachine**](/windows/desktop/api/Pdh/nf-pdh-pdhconnectmachinea)
- [**PdhEnumLogSetNames**](/windows/desktop/api/Pdh/nf-pdh-pdhenumlogsetnamesa)
- [**PdhEnumMachines**](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesa)
- [**PdhEnumMachinesH**](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesha)
- [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)
- [**PdhEnumObjectItemsH**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsha)
- [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa)
- [**PdhEnumObjectsH**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsha)
- [**PdhExpandCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandcounterpatha)
- [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)
- [**PdhExpandWildCardPathH**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpathha)
- [**PdhFormatFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue)
- [**PdhGetCounterInfo**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcounterinfoa)
- [**PdhGetCounterTimeBase**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase)
- [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)
- [**PdhGetDataSourceTimeRangeH**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangeh)
- [**PdhGetDefaultPerfCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcountera)
- [**PdhGetDefaultPerfCounterH**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcounterha)
- [**PdhGetDefaultPerfObject**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjecta)
- [**PdhGetDefaultPerfObjectH**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjectha)
- [**PdhGetDllVersion**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdllversion)
- [**PdhGetFormattedCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya)
- [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)
- [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
- [**PdhGetRawCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya)
- [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)
- [**PdhIsRealTimeQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhisrealtimequery)
- [**PdhLookupPerfIndexByName**](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfindexbynamea)
- [**PdhLookupPerfNameByIndex**](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfnamebyindexa)
- [**PdhMakeCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha)
- [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
- [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya)
- [**PdhOpenQueryH**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)
- [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha)
- [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea)
- [**PdhReadRawLogRecord**](/windows/desktop/api/Pdh/nf-pdh-pdhreadrawlogrecord)
- [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea)
- [**PdhSetCounterScaleFactor**](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)
- [**PdhSetDefaultRealTimeDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhsetdefaultrealtimedatasource)
- [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange)
- [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
- [**PdhUpdateLogFileCatalog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdatelogfilecatalog)
- [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha)
- [**PdhValidatePathEx**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepathexa)

### <a name="perflib-v2-consumer-functions"></a>Funzioni consumer PerfLib V2

Usare le funzioni consumer PerfLib V2 per usare i dati sulle prestazioni dei provider di dati prestazioni V2 se non è possibile usare le funzioni PDH (Performance Data Helper). Queste funzioni possono essere usate durante la scrittura di applicazioni OneCore per la raccolta di V2 CounterSet o quando è necessario raccogliere CounterSet V2 specifiche con dipendenze minime e overhead.

> [!TIP]
> Le funzioni consumer PerfLib V2 sono più difficili da usare rispetto alle funzioni PDH (Performance Data Helper) e supportano solo la raccolta dei dati dai provider v2. Le funzioni PDH dovrebbero essere preferite per la maggior parte delle applicazioni.

- [**PerfAddCounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters)
- [**PerfCloseQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle)
- [**PerfDeleteCounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters)
- [**PerfEnumerateCounterSet**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset)
- [**PerfEnumerateCounterSetInstances**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances)
- [**PerfOpenQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle)
- [**PerfQueryCounterData**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata)
- [**PerfQueryCounterInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo)
- [**PerfQueryCounterSetRegistrationInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo)

## <a name="provider-functions"></a>Funzioni del provider

### <a name="perflib-v2-provider-functions"></a>Funzioni del provider PerfLib V2

[V2 i provider di dati sulle prestazioni](providing-counter-data-using-version-2-0.md) utilizzano le funzioni seguenti:

- [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)
- [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [**CounterCleanup**](countercleanup.md)
- [**CounterInitialize**](counterinitialize.md)
- [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)
- [**PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
- [**PerfDecrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
- [**PerfDeleteInstance**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [**PerfIncrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
- [**PerfIncrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)
- [**PerfQueryInstance**](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [**PerfSetULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [**PerfSetULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [**PerfStartProviderEx**](/windows/desktop/api/Perflib/nf-perflib-perfstartproviderex)
- [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

> [!Note]
> Per installare e disinstallare i provider v2, usare gli strumenti **lodctr** e **unlodctr** . Non è possibile usare le funzioni **LoadPerfCounterTextStrings** e **UnloadPerfCounterTextStrings** per installare e disinstallare i provider v2.

### <a name="performance-dll-functions"></a>Funzioni DLL prestazioni

I [provider di dati delle prestazioni V1](providing-counter-data-using-a-performance-dll.md) implementano una dll che fornisce le funzioni seguenti:

- [*ClosePerformanceData*](/windows/win32/api/winperf/nc-winperf-pm_close_proc)
- [*CollectPerformanceData*](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)
- [*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))

> [!Note]
> A causa di problemi di affidabilità e prestazioni significativi, i provider di dati delle prestazioni V1 sono deprecati. Sebbene sia comunque possibile utilizzare una DLL di estensione per le prestazioni per fornire i dati dei contatori, è consigliabile [creare un provider v2](providing-counter-data-using-version-2-0.md) . Si consiglia inoltre di sostituire i provider v1 esistenti con i provider v2.

È possibile installare e disinstallare i provider v1 usando gli strumenti **lodctr** e **unlodctr** oppure chiamando le funzioni seguenti:

- [**LoadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-loadperfcountertextstringsa)
- [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)

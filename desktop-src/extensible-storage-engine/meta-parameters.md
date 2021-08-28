---
description: 'Altre informazioni su: Meta parameters (Parametri meta)'
title: Meta Parameters
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f821d3aea8055f6c1344ed9d5107417adbaf604
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985514"
---
# <a name="meta-parameters"></a>Meta Parameters


_**Si applica a:** Windows | Windows Server_

## <a name="meta-parameters"></a>Meta Parameters

In questo argomento sono contenuti i parametri utilizzati per controllare altri parametri.

JET_paramConfiguration  
129  
Questo parametro espone più set di valori predefiniti per l'intero set di parametri di sistema. Quando questo parametro è impostato su una configurazione specifica, tutti i valori dei parametri di sistema vengono reimpostati sui valori predefiniti per tale configurazione. Se la configurazione è impostata per un'istanza specifica, i parametri di sistema globali non verranno reimpostati sui valori predefiniti.

Inoltre, il parametro stesso può avere altri effetti sul comportamento del motore di database.

Al momento sono disponibili due configurazioni supportate:

  - Configurazione piccola (0): il motore di database è ottimizzato per l'uso della memoria.

  - Configurazione legacy (1): il motore di database ha le impostazioni predefinite tradizionali.

Configurazione di piccole dimensioni modifica i valori predefiniti dei parametri di sistema seguenti con i valori specificati:


| <p>Parametro di sistema</p> | <p>Nuovo valore predefinito</p> | 
|-------------------------|--------------------------|
| <p>JET_paramMaxSessions</p> | <p>30000</p> | 
| <p>JET_paramMaxOpenTables</p> | <p>2147483647</p> | 
| <p>JET_paramMaxCursors</p> | <p>2147483647</p> | 
| <p>JET_paramMaxVerPages</p> | <p>2147483647</p> | 
| <p>JET_paramMaxTemporaryTables</p> | <p>2147483647</p> | 
| <p>JET_paramLogFileSize</p> | <p>64</p> | 
| <p>JET_paramLogBuffers</p> | <p>1</p> | 
| <p>JET_paramDbExtensionSize</p> | <p>16</p> | 
| <p>JET_paramPageTempDBMin</p> | <p>14</p> | 
| <p>JET_paramCacheSizeMax</p> | <p>16</p> | 
| <p>JET_paramCheckpointDepthMax</p> | <p>65536</p> | 
| <p>JET_paramLRUKHistoryMax</p> | <p>10</p> | 
| <p>JET_paramOutstandingIOMax</p> | <p>16</p> | 
| <p>JET_paramStartFlushThreshold</p> | <p>1</p> | 
| <p>JET_paramStopFlushThreshold</p> | <p>2</p> | 
| <p>JET_paramNoInformationEvent</p> | <p>1</p> | 
| <p>JET_paramCacheSizeMin</p> | <p>16</p> | 
| <p>JET_paramPreferredVerPages</p> | <p>2147483647</p> | 
| <p>JET_paramLogFileCreateAsynch</p> | <p>0</p> | 
| <p>JET_paramGlobalMinVerPages</p> | <p>1</p> | 
| <p>JET_paramPageHintCacheSize</p> | <p>32</p> | 
| <p>JET_paramDisablePerfmon</p> | <p>1</p> | 
| <p>JET_paramEnableFileCache</p> | <p>1</p> | 
| <p>JET_paramEnableViewCache</p> | <p>1</p> | 
| <p>JET_paramVerPageSize</p> | <p>1024</p> | 
| <p>JET_paramEnableAdvanced</p> | <p>0</p> | 
| <p>JET_paramCheckpointIOMax</p> | <p>8</p> | 



Small Configuration ha anche diversi altri effetti sul motore di database, tra cui:

  - Tutte le risorse gestite dai parametri di sistema vengono allocate dall'heap in base alle esigenze

  - Le altre risorse interne usate dal motore di database vengono ridotte di dimensioni

  - Varie attività di manutenzione vengono ridimensionate per evitare l'attività del thread in background


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>1 (legacy)</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0 – 1</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>A partire Windows Server 2008 e Windows Vista</p> | 



JET_paramEnableAdvanced  
130  
Questo parametro viene utilizzato per controllare quando il motore di database accetta o rifiuta le modifiche apportate a un subset dei parametri di sistema. Questo parametro viene usato in combinazione con JET_paramConfiguration per impedire che alcuni parametri di sistema vengano impostati in base alle impostazioni predefinite della configurazione selezionata.

I parametri di sistema seguenti non verranno impostati quando questo parametro è impostato su False:

  - JET_paramMaxSessionsfon

  - JET_paramMaxOpenTables

  - JET_paramPreferredMaxOpenTables

  - JET_paramMaxCursors

  - JET_paramMaxVerPages

  - JET_paramMaxTemporaryTables

  - JET_paramLogBuffers

  - JET_paramWaitLogFlush

  - JET_paramLogCheckpointPeriod

  - JET_paramLogWaitingUserMax

  - JET_paramDbExtensionSize

  - JET_paramPageTempDBMin

  - JET_paramPageFragment

  - JET_paramBatchIOBufferMax

  - JET_paramCacheSizeMax

  - JET_paramLRUKCorrInterval

  - JET_paramLRUKHistoryMax

  - JET_paramLRUKPolicy

  - JET_paramLRUKTimeout

  - JET_paramLRUKTrxCorrInterval

  - JET_paramOutstandingIOMax

  - JET_paramStartFlushThreshold

  - JET_paramStopFlushThreshold

  - JET_paramCacheSize

  - JET_paramCacheSizeMin

  - JET_paramPreferredVerPages

  - JET_paramBackupChunkSize

  - JET_paramBackupOutstandingReads

  - JET_paramLogFileCreateAsynch

  - JET_paramRecordUpgradeDirtyLevel

  - JET_paramGlobalMinVerPages

  - JET_paramPageHintCacheSize

  - JET_paramVersionStoreTaskQueueMax

  - JET_paramDBAPageAvailMin

  - JET_paramMaxRandomIOSize

  - JET_paramCachedClosedTables

  - JET_paramEnableFileCache

  - JET_paramEnableViewCache

  - JET_paramVerPageSize

  - JET_paramCheckpointIOMax


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Vero</p> | 
| <p>Digitare:</p> | <p>Boolean</p> | 
| <p>Intervallo valido:</p> | <p>False, True</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>A partire da Windows Server 2008 e Windows Vista</p> | 



### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)

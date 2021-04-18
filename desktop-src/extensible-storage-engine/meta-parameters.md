---
description: 'Altre informazioni su: meta Parameters'
title: Meta parametri
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
ms.openlocfilehash: 82b5fac0cc59e9a0511344e72b3f316af9013965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306206"
---
# <a name="meta-parameters"></a>Meta parametri


_**Si applica a:** Windows | Windows Server_

## <a name="meta-parameters"></a>Meta parametri

Questo argomento contiene i parametri usati per controllare altri parametri.

JET_paramConfiguration  
129  
Questo parametro espone più set di valori predefiniti per l'intero set di parametri di sistema. Quando questo parametro è impostato su una configurazione specifica, tutti i valori dei parametri di sistema vengono reimpostati sui valori predefiniti per tale configurazione. Se la configurazione è impostata per un'istanza specifica, i parametri di sistema globali non verranno reimpostati sui valori predefiniti.

Inoltre, il parametro stesso può avere altri effetti sul comportamento del motore di database.

A questo punto, sono disponibili due configurazioni supportate:

  - Small Configuration (0): il motore di database è ottimizzato per l'uso della memoria.

  - Configurazione legacy (1): il motore di database presenta le impostazioni predefinite tradizionali.

Small Configuration modifica le impostazioni predefinite dei seguenti parametri di sistema con i valori specificati:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parametro di sistema</p></th>
<th><p>Nuovo valore predefinito</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_paramMaxSessions</p></td>
<td><p>30000</p></td>
</tr>
<tr class="even">
<td><p>JET_paramMaxOpenTables</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramMaxCursors</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="even">
<td><p>JET_paramMaxVerPages</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramMaxTemporaryTables</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="even">
<td><p>JET_paramLogFileSize</p></td>
<td><p>64</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramLogBuffers</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>JET_paramDbExtensionSize</p></td>
<td><p>16</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramPageTempDBMin</p></td>
<td><p>14</p></td>
</tr>
<tr class="even">
<td><p>JET_paramCacheSizeMax</p></td>
<td><p>16</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramCheckpointDepthMax</p></td>
<td><p>65536</p></td>
</tr>
<tr class="even">
<td><p>JET_paramLRUKHistoryMax</p></td>
<td><p>10</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramOutstandingIOMax</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>JET_paramStartFlushThreshold</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramStopFlushThreshold</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>JET_paramNoInformationEvent</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramCacheSizeMin</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>JET_paramPreferredVerPages</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramLogFileCreateAsynch</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>JET_paramGlobalMinVerPages</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramPageHintCacheSize</p></td>
<td><p>32</p></td>
</tr>
<tr class="even">
<td><p>JET_paramDisablePerfmon</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramEnableFileCache</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>JET_paramEnableViewCache</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramVerPageSize</p></td>
<td><p>1024</p></td>
</tr>
<tr class="even">
<td><p>JET_paramEnableAdvanced</p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramCheckpointIOMax</p></td>
<td><p>8</p></td>
</tr>
</tbody>
</table>


La configurazione di piccole dimensioni ha anche diversi altri effetti sul motore di database, tra cui:

  - Tutte le risorse gestite dai parametri di sistema vengono allocate dall'heap in base alle esigenze

  - Le altre risorse interne usate dal motore di database vengono ridimensionate

  - Diverse attività di manutenzione vengono ridimensionate per evitare attività dei thread in background

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>1 (legacy)</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0 – 1</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>A partire da Windows Server 2008 e Windows Vista</p></td>
</tr>
</tbody>
</table>


JET_paramEnableAdvanced  
130  
Questo parametro viene utilizzato per controllare quando il motore di database accetta o rifiuta le modifiche apportate a un subset dei parametri di sistema. Questo parametro viene utilizzato in combinazione con JET_paramConfiguration per impedire l'impostazione di alcuni parametri di sistema dalle impostazioni predefinite della configurazione selezionata.

I parametri di sistema seguenti verranno protetti dall'impostazione quando questo parametro è impostato su false:

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>Vero</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>A partire da Windows Server 2008 e Windows Vista</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)

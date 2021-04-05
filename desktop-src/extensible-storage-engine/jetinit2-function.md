---
description: 'Altre informazioni su: funzione JetInit2'
title: Funzione JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00cc3402567a7c1342e78d3c84a1d6cfca8ab4d8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103969540"
---
# <a name="jetinit2-function"></a>Funzione JetInit2


_**Si applica a:** Windows | Windows Server_

## <a name="jetinit2-function"></a>Funzione JetInit2

La funzione **JetInit2** inserisce il motore di database in uno stato in cui può supportare l'utilizzo di file di database da parte dell'applicazione. Il motore deve essere già configurato correttamente per l'inizializzazione tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md). Il ripristino dell'arresto anomalo del database viene eseguito automaticamente nell'ambito del processo di inizializzazione.

**Windows XP:**  **JetInit2** è stato introdotto in Windows XP.

questa funzione è obsoleta. In alternativa, usare [JetInit3](./jetinit3-function.md) .

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parametri

*pinstance*

Istanza di da utilizzare per questa chiamata.

Per Windows 2000, questo parametro viene ignorato e deve essere sempre NULL.

Per Windows XP e versioni successive, l'uso di questo parametro dipende dalla modalità operativa del motore. Se il motore funziona in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza, questo parametro può essere NULL o può essere impostato su un buffer di output valido che contiene NULL o JET_instanceNil che restituisce l'handle di istanza globale creato come effetto collaterale dell'inizializzazione. Questo handle di istanza può quindi essere passato a qualsiasi altra API che accetta un'istanza di. Se il motore funziona in modalità a istanze diverse, questo parametro deve essere impostato su un buffer di input valido che contiene l'handle dell'istanza restituito da [JetCreateInstance](./jetcreateinstance-function.md) che viene inizializzato.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitReplayReplicatedLogFiles</p></td>
<td><p>Riservato per utilizzi futuri.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateSFSVolumeIfNotExist</p></td>
<td><p>Riservato per utilizzi futuri.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreMissingDB</p></td>
<td><p>Questa opzione consente all'utente di eseguire il ripristino in un set di file di log, senza che tutti i database presenti siano collegati in un punto del set di log.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecoveryWithoutUndo</p></td>
<td><p>Eseguire il ripristino, ma arrestare la fase di rollback. Ciò consente la copia e l'applicazione dei log delle transazioni aggiuntivi.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTruncateLogsAfterRecovery</p></td>
<td><p>Al completamento del ripristino, troncare i file di log.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitReplayMissingMapEntryDB</p></td>
<td><p>Impostazione predefinita per la voce della mappa di database non presente nella stessa posizione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreLostLogs</p></td>
<td><p>Ignorare i log persi alla fine del flusso di log.</p>
<p><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> è stato introdotto in Windows 7.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .


#### <a name="remarks"></a>Commenti

Un'istanza deve essere inizializzata con una chiamata a **JetInit2** prima che possa essere usata da un valore diverso da [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Un'istanza viene distrutta da una chiamata alla funzione [JetTerm](./jetterm-function.md) , anche se tale istanza non è mai stata inizializzata usando [JetInit](./jetinit-function.md). Un'istanza è l'unità di recupero per il motore di database. Consente di controllare il ciclo di vita di tutti i file utilizzati per proteggere l'integrità dei dati in un set di file di database. Questi file includono il file del checkpoint e i file di log delle transazioni.

Se il ripristino viene eseguito in un set di log, per cui non sono presenti tutti i database (che restituiscono l'errore JET_errAttachedDatabaseMismatch in circostanze normali) e il client desidera che il ripristino continui nonostante i database mancanti, il JET_ bitReplayIgnoreMissingDB viene utilizzato per continuare il ripristino dei database disponibili.

Per ulteriori informazioni, vedere la sezione Osservazioni in [JetInit](./jetinit-function.md) .

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[File del motore di archiviazione estendibile](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri delle risorse](./resource-parameters.md)

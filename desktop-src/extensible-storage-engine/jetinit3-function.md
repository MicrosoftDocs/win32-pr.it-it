---
description: 'Altre informazioni su: funzione JetInit3'
title: Funzione JetInit3
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96171920b7538e71e822eaf0879e476fb2fd31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350421"
---
# <a name="jetinit3-function"></a>Funzione JetInit3


_**Si applica a:** Windows | Windows Server_

## <a name="jetinit3-function"></a>Funzione JetInit3

La funzione **JetInit3** inserisce il motore di database in uno stato in cui può supportare l'utilizzo di file di database da parte dell'applicazione. Il motore deve essere già configurato correttamente per l'inizializzazione, operazione eseguita usando la funzione [JetSetSystemParameter](./jetsetsystemparameter-function.md) . Si noti che il ripristino dell'arresto anomalo del database viene eseguito automaticamente nell'ambito del processo di inizializzazione.

**Windows Vista:**  **JetInit3** è stato introdotto in Windows Vista.

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*pinstance*

Istanza di utilizzata per una particolare chiamata. L'uso di questo parametro dipende dalla modalità operativa del motore. Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000), in cui è supportata una sola istanza, è possibile impostare questo parametro su **null** o su un buffer di output valido contenente **null** o JET_instanceNil, che restituisce l'handle di istanza globale creato come effetto collaterale dell'inizializzazione. Questo handle di istanza può quindi essere passato a qualsiasi altra API che accetta un'istanza di. Se il motore funziona in modalità a istanze diverse, è necessario impostare questo parametro su un buffer di input valido contenente l'handle dell'istanza restituito dalla funzione [JetCreateInstance](./jetcreateinstance-function.md) che viene inizializzata.

*prstInfo*

Parametri di recupero aggiuntivi utilizzati per rimappare i database durante il ripristino, per impostare la posizione in cui il ripristino viene arrestato o per determinare lo stato di ripristino corrente.

*grbit*

Gruppo di bit che specifica zero o più opzioni elencate e definite nella tabella seguente.

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
<td><p>Questo valore è riservato per l'uso futuro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateSFSVolumeIfNotExist</p></td>
<td><p>Questo valore è riservato per l'uso futuro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreMissingDB</p></td>
<td><p>Questo valore consente all'utente di eseguire il ripristino in un set di file di log, anche in assenza dei database collegati al set di file di log in un determinato momento.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecoveryWithoutUndo</p></td>
<td><p>Questo valore consente all'utente di eseguire il ripristino, ma solo fino alla fase di annullamento (e non inclusa). Utilizzando questo valore, i log delle transazioni aggiuntivi possono essere copiati e applicati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTruncateLogsAfterRecovery</p></td>
<td><p>Questo valore causa il troncamento dei file di log durante un ripristino soft.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitReplayMissingMapEntryDB</p></td>
<td><p>Questo valore causa la mancata impostazione predefinita di una voce di mapping del database nella stessa posizione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreLostLogs</p></td>
<td><p>Questo valore causa la perdita dei log dalla fine del flusso di log da ignorare durante il ripristino.</p>
<p><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> è stato introdotto in Windows 7.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sui possibili errori di Extensible Storage Engine (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .


#### <a name="remarks"></a>Commenti

Un'istanza deve essere inizializzata con una chiamata alla funzione **JetInit3** prima che possa essere utilizzata da qualsiasi altra funzione [JetSetSystemParameter](./jetsetsystemparameter-function.md) .

Un'istanza viene distrutta da una chiamata alla funzione [JetTerm](./jetterm-function.md) , anche se tale istanza non è mai stata inizializzata tramite la funzione [JetInit](./jetinit-function.md) . Un'istanza è l'unità di recupero per il motore di database. Consente di controllare il ciclo di vita di tutti i file utilizzati per proteggere l'integrità dei dati in un set di file di database. Questi file includono il file del checkpoint e i file di log delle transazioni. Si noti che [JetTerm](./jetterm-function.md) non deve essere chiamato se la funzione **JetInit3** ha esito negativo. Tuttavia, [JetTerm](./jetterm-function.md) deve comunque essere chiamato per tutte le istanze create da **JetCreateInstance2** se **JetInit3** non è mai stato chiamato o se **JetInit3** ha esito positivo.

Se il ripristino viene eseguito in un set di log per cui non sono presenti tutti i database correlati (che restituiscono l'errore JET_errAttachedDatabaseMismatch in circostanze normali) e il client desidera che il ripristino continui nonostante i database mancanti, viene utilizzato l'errore JET_bitReplayIgnoreMissingDB per continuare il ripristino dei database disponibili.

Poiché il ripristino dell'arresto anomalo del sistema non si verifica di solito nello stesso computer (e con la stessa configurazione) del momento in cui si è verificato l'arresto anomalo, un database non cambia in genere il percorso. In alcuni scenari, ad esempio lo stato di trasferimento di file in un computer diverso o il ripristino del backup di snapshot in posizioni diverse, questo non è più vero. La funzione **JetInit3** consente di specificare un mapping (usando le strutture [JET_RSTINFO](./jet-rstinfo-structure.md) e [JET_RSTMAP](./jet-rstmap-structure.md) ) tra il percorso del database precedente e la nuova posizione. Infatti, è necessaria solo la nuova posizione purché i file di database siano presenti in tale posizione. Non appena si conoscono i percorsi dei database ripristinati, la firma del database verrà utilizzata per identificare il database durante il processo di ripristino. Il percorso del database originale sarà necessario solo se è necessario ricreare un database, nel qual caso la firma è nota.

Inoltre, se è necessario arrestare un ripristino dopo un'operazione di annullamento, è possibile specificare una posizione di log specifica in corrispondenza della quale il ripristino viene interrotto. Si noti che ciò include la possibilità di arrestare alla fine di una particolare generazione del log se la posizione specificata fa parte della generazione ma oltre la fine del log effettivo.

Per ulteriori informazioni, vedere la sezione "osservazioni" nell'argomento [JetInit](./jetinit-function.md) .

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Client</p></td>
<td><p>Richiede Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>Server</p></td>
<td><p>Richiede Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p>Intestazione</p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p>Libreria</p></td>
<td><p>USA ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p>Unicode</p></td>
<td><p>Implementato come <strong>JetInit3W</strong> (Unicode) e <strong>JetInit3A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[File del motore di archiviazione estendibile](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_RSTINFO](./jet-rstinfo-structure.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri delle risorse](./resource-parameters.md)

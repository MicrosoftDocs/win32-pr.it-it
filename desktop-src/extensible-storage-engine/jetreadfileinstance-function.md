---
description: 'Altre informazioni su: funzione JetReadFileInstance'
title: Funzione JetReadFileInstance
TOCTitle: JetReadFileInstance Function
ms:assetid: b17b4b43-86e5-4507-8a85-bbd5eac0aa3c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294060(v=EXCHG.10)
ms:contentKeyID: 32765675
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9aad9828a92d67f2e7411aa534103696d913934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524960"
---
# <a name="jetreadfileinstance-function"></a>Funzione JetReadFileInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetreadfileinstance-function"></a>Funzione JetReadFileInstance

La funzione **JetReadFileInstance** Recupera il contenuto di un file aperto con la funzione [JetOpenFileInstance](./jetopenfileinstance-function.md) .

**Windows XP**:   **JetReadFileInstance** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a>Parametri

*istanza*

Istanza di da utilizzare per una particolare chiamata API.

Si noti che per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza. In questo caso, l'utilizzo di questa istanza globale è implicito.

Per Windows XP e versioni successive, è possibile chiamare la variante API che non accetta questo parametro solo quando il motore è in modalità legacy (modalità di compatibilità di Windows 2000) nei casi in cui è supportata una sola istanza. In caso contrario, l'operazione avrà esito negativo e restituirà l'errore JET_errRunningInMultiInstanceMode.

*hfFile*

Handle del file da leggere.

*PV*

Buffer di output che riceverà i dati del file.

*CB*

Dimensione massima, in byte, del buffer di output.

*PCB*

Quantità effettiva di dati recuperati dal file.

### <a name="return-value"></a>Valore restituito

Questa funzione semplifica la restituzione di qualsiasi tipo di dati [JET_ERR](./jet-err.md) definiti nell'API ESE (Extensible Storage Engine). Per altre informazioni sugli errori di JET, vedere [errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md) e [parametri di gestione degli](./error-handling-parameters.md)errori.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata alla funzione <a href="gg269240(v=exchg.10).md">JetStopService</a> . Questo errore viene restituito solo da Windows XP e versioni successive di Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata alla funzione <a href="gg269240(v=exchg.10).md">JetStopService</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore viene restituito solo da Windows XP e versioni successive di Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri specificati contiene un valore imprevisto o un valore che non ha senso se combinato con il valore di un altro parametro. Questa situazione può verificarsi per la funzione <strong>JetReadFileInstance</strong> quando si verifica una delle condizioni seguenti:</p>
<ul>
<li><p>L'handle dell'istanza specificato non è valido. Windows XP e versioni successive di Windows.</p></li>
<li><p>La dimensione del buffer di output non è un multiplo delle dimensioni della pagina del database (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP e versioni successive di Windows.</p></li>
<li><p>Le dimensioni del buffer di output sono inferiori a tre pagine di database (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) ed è la prima chiamata alla funzione <strong>JetReadFileInstance</strong> per l'handle specificato. Windows XP e versioni successive di Windows.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>Operazione non riuscita perché è stato rilevato un danneggiamento dei dati irreversibile durante la lettura di un file di log delle transazioni. Questo errore viene restituito solo da Windows XP e versioni successive di Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata a questa sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>Operazione non riuscita perché è stato rilevato un danneggiamento dei dati irreversibile durante la lettura di una pagina del database da un file di database o da un file di patch del database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata a questa sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) nel caso in cui sia supportata una sola istanza, ma esistono già più istanze.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata a questa sessione è stata arrestata.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, il blocco di dati successivo del file verrà letto nel buffer di output. Verrà restituito anche il numero effettivo di byte recuperati. L'offset del file in corrispondenza del quale verrà eseguita la lettura successiva verrà spostato in base a questa quantità.

In caso di errore, lo stato del buffer di output non è definito. L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza corrente. In Windows XP e versioni successive di Windows, il backup non verrà annullato se si è verificato un errore durante la lettura di un file di database. Tuttavia, il backup del file di database verrà comunque annullato e l'handle corrispondente verrà chiuso automaticamente.

#### <a name="remarks"></a>Commenti

Qualsiasi chiamata alla funzione **JetReadFileInstance** eseguita usando un handle che ha già restituito tutti i dati nel file sottostante (ad esempio se una chiamata precedente ha restituito un minor numero di byte rispetto alla dimensione del buffer di output) avrà sempre esito positivo ma restituirà zero byte di dati.

Per ottimizzare le prestazioni del backup, è necessario utilizzare un buffer di output di grandi dimensioni. Potrebbe essere necessario sperimentare per individuare il compromesso ottimale tra l'utilizzo delle risorse e la velocità effettiva per una particolare situazione. In ogni caso, il buffer di output non deve essere inferiore a 64 KB. Il puntatore passato a **JetReadFileInstance** deve essere allineato con un limite della pagina di memoria (4 KB o 8 KB). Questa operazione può essere eseguita chiamando la funzione **VirtualAlloc** .

Non sono supportate più chiamate simultanee a **JetReadFileInstance** effettuate usando lo stesso handle di file. Ciò significa che non è possibile accodare diversi buffer per la lettura simultanea sullo stesso file per ottenere una velocità effettiva elevata sequenziale. Usare invece un solo buffer di grandi dimensioni.

Se è stata configurata una particolare istanza in modo che lo scrubbing della pagina del database sia abilitato (vedere il [JET_paramCircularLog](./transaction-log-parameters.md) parametro nei [parametri di sistema](./extensible-storage-engine-system-parameters.md)), i dati eliminati verranno rimossi dal database come effetto collaterale di una chiamata a **JetReadFileInstance** sul file di database.

È molto importante comprendere in che modo il backup e il danneggiamento dei dati interagiscono. Se il motore di database rileva il danneggiamento dei dati durante un backup, il backup del database interessato o dell'intera istanza avrà esito negativo. Si tratta di una decisione di progettazione consapevole per la protezione dalla perdita di dati. Se il motore di database ha consentito la riuscita di un backup in cui è presente il danneggiamento dei dati, è possibile che un backup precedente non danneggiato possa essere eliminato. Si tratta di un peccato perché sarebbe possibile correggere il danneggiamento dei dati nell'istanza di Live ripristinando tale backup e riproducendo tutti i file di log delle transazioni su tale database. Questo scenario di perdita di dati zero presuppone che la registrazione circolare non sia abilitata (vedere [JET_paramCircularLog](./transaction-log-parameters.md) nei [parametri di sistema](./extensible-storage-engine-system-parameters.md)).

È inoltre importante comprendere che in genere i casi di danneggiamento dei dati vengono rilevati per la prima volta durante il backup di flusso. Questo perché il backup di flusso è l'unico processo che esegue periodicamente l'analisi di ogni singola pagina del file di database. È anche probabile che il backup di flusso sia il primo processo per rilevare i primi segni di errore hardware, come manifestato da errori di danneggiamento dei dati intermittenti, a causa della quantità di dati recuperati dal backup e della velocità di recupero dei dati.

Il danneggiamento dei dati viene rilevato dal motore di database tramite l'utilizzo di checksum dei blocchi. Questi checksum vengono impostati immediatamente prima della scrittura di una pagina del database e vengono verificati in una pagina di database letta. Questo schema consente al motore di database di determinare che i dati sono stati danneggiati a un certo punto, ma non consente al motore di database di determinare l'origine di tale danneggiamento. Storicamente, le istanze di tali dati danneggiate sono state originate da origini diverse dal motore di database stesso.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Client</p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>Server</p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>Intestazione</p></td>
<td><p>Viene dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p>Libreria</p></td>
<td><p>USA ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)

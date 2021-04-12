---
description: 'Altre informazioni su: funzione JetReadFile'
title: JetReadFile (funzione)
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57e11f3b5478f18bc7883974c2f598bf24dcb8fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232555"
---
# <a name="jetreadfile-function"></a>JetReadFile (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetreadfile-function"></a>JetReadFile (funzione)

La funzione **JetReadFile** Recupera il contenuto di un file aperto con [JetOpenFile](./jetopenfile-function.md).

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parametri

*hfFile*

Handle del file da leggere.

*PV*

Buffer di output che riceverà i dati del file.

*CB*

Dimensione massima in byte del buffer di output.

*pcbActual*

Riceve la quantità effettiva di dati di file recuperati.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo problema può verificarsi per <strong>JetReadFile</strong> quando:</p>
<ul>
<li><p>L'handle dell'istanza specificato non è valido. Windows XP e versioni successive.</p></li>
<li><p>La dimensione del buffer di output non è un multiplo delle dimensioni della pagina del database (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP e versioni successive.</p></li>
<li><p>Le dimensioni del buffer di output sono inferiori a tre pagine di database (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) ed è la prima chiamata a <strong>JetReadFile</strong> per l'handle specificato. Windows XP e versioni successive.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>Operazione non riuscita perché è stato rilevato un danneggiamento dei dati non ripristinabili durante la lettura di una pagina del database da un file di database o un file di patch del database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>Operazione non riuscita perché è stato rilevato un danneggiamento dei dati non ripristinabili durante la lettura di un file di log delle transazioni. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, il blocco di dati successivo del file verrà letto nel buffer di output. Verrà restituito anche il numero effettivo di byte recuperati. L'offset del file in corrispondenza del quale verrà eseguita la lettura successiva verrà spostato in base a questa quantità.

In caso di errore, lo stato del buffer di output non è definito. L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza. In Windows XP e versioni successive, il backup non verrà annullato se si è verificato un errore durante la lettura di un file di database. Tuttavia, il backup del file di database verrà comunque annullato e l'handle corrispondente verrà chiuso automaticamente.

#### <a name="remarks"></a>Commenti

Qualsiasi chiamata a **JetReadFile** utilizzando un handle che ha già restituito tutti i dati nel file sottostante, ad esempio una chiamata precedente restituita meno byte rispetto alla dimensione del buffer di output, avrà sempre esito positivo ma restituirà sempre zero byte di dati.

Per ottimizzare le prestazioni del backup, è necessario utilizzare un buffer di output di grandi dimensioni. Potrebbe essere necessaria una sperimentazione per individuare il compromesso giusto tra il consumo di risorse e la velocità effettiva per una determinata situazione. Il buffer di output non deve essere minore di 64KB in qualsiasi caso.

Non sono supportate più chiamate simultanee a **JetReadFile** con lo stesso handle di file. Ciò significa che non è possibile accodare diversi buffer per la lettura simultanea nello stesso file per ottenere una velocità effettiva elevata sequenziale. In alternativa, è necessario usare un singolo buffer di grandi dimensioni.

Se l'istanza è configurata in modo che lo scrubbing della pagina del database sia abilitato (vedere JET_paramZeroDatabaseDuringBackup nei parametri di sistema), i dati eliminati verranno rimossi dal database come effetto collaterale di una chiamata a **JetReadFile** rispetto al file di database.

È molto importante comprendere in che modo il backup e il danneggiamento dei dati interagiscono. Se il motore di database rileva il danneggiamento dei dati durante un backup, il backup del database interessato o dell'intera istanza avrà esito negativo. Si tratta di una decisione di progettazione consapevole per la protezione dalla perdita di dati. Se il motore di database ha consentito la riuscita di un backup in cui è presente il danneggiamento dei dati, è possibile che un backup precedente non danneggiato possa essere scartato di conseguenza. Si tratta di un peccato perché sarebbe possibile correggere il danneggiamento dei dati nell'istanza di Live ripristinando tale backup e riproducendo tutti i file di log delle transazioni su tale database. Questo scenario con zero perdite di dati presuppone che la registrazione circolare non sia abilitata (vedere [JET_paramCircularLog](./transaction-log-parameters.md) nei [parametri di sistema](./extensible-storage-engine-system-parameters.md)).

È inoltre importante comprendere che, quando è presente il danneggiamento dei dati, il backup di flusso sarà il posto più probabile che verrà prima rilevato. Questo avviene perché il backup di flusso è l'unico processo che esegue periodicamente l'analisi di ogni singola pagina del file di database. È anche probabile che il backup di flusso sia il primo processo per rilevare i primi segni di errore hardware, come manifestato da errori di danneggiamento dei dati intermittenti. Ciò è dovuto alla quantità di dati recuperati da backup e alla velocità con cui viene recuperato.

Il danneggiamento dei dati viene rilevato dal motore di database tramite l'utilizzo di checksum dei blocchi. Questi checksum vengono impostati immediatamente prima della scrittura di una pagina del database e vengono verificati in una pagina di database letta. Questo schema consente al motore di database di determinare che i dati sono stati danneggiati a un certo punto, ma non consente al motore di database di determinare l'origine di tale danneggiamento. In passato, la ragione principale di tale danneggiamento è stata rilevata da origini diverse dal motore di database stesso.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)

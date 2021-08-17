---
description: Altre informazioni sulla funzione JetReadFileInstance
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
ms.openlocfilehash: ec5c83bb78528a61bbe7af9bafa59567100ee9da669915b96230bfb97b8bf390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117891117"
---
# <a name="jetreadfileinstance-function"></a>Funzione JetReadFileInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetreadfileinstance-function"></a>Funzione JetReadFileInstance

La **funzione JetReadFileInstance** recupera il contenuto di un file aperto con la [funzione JetOpenFileInstance.](./jetopenfileinstance-function.md)

**Windows XP:** **JetReadFileInstance** è stato introdotto in Windows XP.

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

*Istanza*

Istanza di da usare per una determinata chiamata API.

Si noti che per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza. L'uso di questa istanza globale è implicito in questo caso.

Per Windows XP e versioni successive, è possibile chiamare la variante API che non accetta questo parametro solo quando il motore è in modalità legacy (modalità di compatibilità Windows 2000) nei casi in cui è supportata una sola istanza. In caso contrario, l'operazione avrà esito negativo e restituirà JET_errRunningInMultiInstanceMode errore.

*hfFile*

Handle del file da leggere.

*Pv*

Buffer di output che riceverà i dati del file.

*Cb*

Dimensione massima, in byte, del buffer di output.

*Pcb*

Quantità effettiva di dati del file recuperati.

### <a name="return-value"></a>Valore restituito

Questa funzione facilita la [](./jet-err.md) restituzione di JET_ERR tipi di dati definiti nell'API Extensible Archiviazione Engine (ESE). Per altre informazioni sugli errori JET, vedere [Errori del motore](./extensible-storage-engine-errors.md) Archiviazione estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).

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
<td><p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata alla <a href="gg269240(v=exchg.10).md">funzione JetStopService.</a> Questo errore verrà restituito solo da Windows XP e versioni successive Windows successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata alla <a href="gg269240(v=exchg.10).md">funzione JetStopService.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive Windows successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri specificati conteneva un valore imprevisto o un valore che non aveva senso se combinato con il valore di un altro parametro. Ciò può verificarsi per <strong>la funzione JetReadFileInstance</strong> quando si verifica una delle condizioni seguenti:</p>
<ul>
<li><p>L'handle di istanza specificato non è valido. Windows XP e versioni Windows successive.</p></li>
<li><p>Le dimensioni del buffer di output non sono un multiplo delle dimensioni della pagina del database (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP e versioni Windows successive.</p></li>
<li><p>Le dimensioni del buffer di output sono inferiori a tre pagine di database (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) e si tratta della prima chiamata alla funzione <strong>JetReadFileInstance</strong> per l'handle specificato. Windows XP e versioni Windows successive.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>L'operazione non è riuscita perché è stato rilevato un danneggiamento dei dati irreversibile durante la lettura di un file di log delle transazioni. Questo errore verrà restituito solo da Windows XP e versioni successive Windows successive.</p></td>
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
<td><p>Jet_errreadverifyfailure</p></td>
<td><p>L'operazione non è riuscita perché è stato rilevato un danneggiamento dei dati irreversibile durante la lettura di una pagina di database da un file di database o da un file di patch del database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata a questa sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità Windows 2000) in un caso in cui è supportata una sola istanza ma esistono già più istanze.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata a questa sessione.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, il blocco successivo di dati dal file verrà letto nel buffer di output. Verrà restituito anche il numero effettivo di byte recuperati. L'offset del file in corrispondenza del quale verrà eseguita la lettura successiva verrà avanzato di questa quantità.

In caso di errore, lo stato del buffer di output non è definito. L'errore comporta l'annullamento dell'intero processo di backup per l'istanza corrente. In Windows XP e versioni successive Windows, il backup non verrà annullato se si è verificato un errore durante la lettura di un file di database. Tuttavia, il backup del file di database verrà comunque annullato e l'handle corrispondente verrà chiuso automaticamente.

#### <a name="remarks"></a>Commenti

Qualsiasi chiamata alla funzione **JetReadFileInstance** eseguita usando un handle che ha già restituito tutti i dati nel file sottostante ,ad esempio se una chiamata precedente ha restituito un numero di byte inferiore a quello del buffer di output, avrà sempre esito positivo, ma restituirà zero byte di dati.

È consigliabile usare un buffer di output di grandi dimensioni per ottimizzare le prestazioni di backup. Potrebbe essere necessario sperimentare per trovare il compromesso ottimale tra l'utilizzo delle risorse e la velocità effettiva per una determinata situazione. In ogni caso, il buffer di output non deve essere inferiore a 64 KB. Il puntatore passato a **JetReadFileInstance** deve essere allineato a un limite di pagina di memoria (4 KB o 8 KB). A tale scopo, chiamare la **funzione VirtualAlloc.**

Non sono supportate più chiamate simultanee a **JetReadFileInstance** effettuate usando lo stesso handle di file. Ciò significa che non è possibile accodare diversi buffer per la lettura simultanea nello stesso file per ottenere una velocità effettiva sequenziale elevata. È consigliabile usare invece un singolo buffer di grandi dimensioni.

Se è stata configurata una particolare istanza in modo che sia abilitato lo scrubbing della pagina del database [(vedere](./transaction-log-parameters.md) il parametro JET_paramCircularLog [in](./extensible-storage-engine-system-parameters.md)Parametri di sistema), i dati eliminati verranno rimossi dal database come effetto collaterale di una chiamata a **JetReadFileInstance** sul file di database.

È molto importante comprendere l'interazione tra backup e danneggiamento dei dati. Se il motore di database rileva il danneggiamento dei dati durante un backup, il backup del database interessato o dell'intera istanza avrà esito negativo. Si tratta di una decisione di progettazione consapevole destinata a proteggersi dalla perdita di dati. Se il motore di database ha consentito l'esito positivo di un backup in cui era presente un danneggiamento dei dati, è possibile che un backup precedente non danneggiato possa essere eliminato di conseguenza. Questo sarebbe un problema perché sarebbe possibile correggere il danneggiamento dei dati nell'istanza in tempo reale ripristinando tale backup e riproducendo tutti i file di log delle transazioni in tale database. Questo scenario di perdita di dati zero presuppone che la registrazione circolare non sia abilitata (vedere JET_paramCircularLog [in](./transaction-log-parameters.md) Parametri [di sistema](./extensible-storage-engine-system-parameters.md)).

È anche importante comprendere che i casi di danneggiamento dei dati vengono in genere rilevati per primi durante il backup di streaming. Questo perché il backup di streaming è l'unico processo che esegue regolarmente l'analisi di ogni singola pagina del file di database. È anche probabile che il backup di streaming sia il primo processo per rilevare i primi segnali di errore hardware come manifestati da errori intermittenti di danneggiamento dei dati, sia per la quantità di dati recuperati dal backup che per la velocità con cui vengono recuperati i dati.

Il danneggiamento dei dati viene rilevato dal motore di database tramite l'uso di checksum di blocco. Questi checksum vengono impostati subito prima della scrittura di una pagina del database e vengono verificati in una pagina di database letta. Questo schema consente al motore di database di determinare che i dati sono stati danneggiati a un certo punto, ma non consente al motore di database di determinare l'origine di tale danneggiamento. In genere, le istanze di tale danneggiamento dei dati hanno avuto origine da origini diverse dal motore di database stesso.

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
<td><p>Viene dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p>Libreria</p></td>
<td><p>Usa ESENT.lib.</p></td>
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

---
description: Altre informazioni sulla funzione JetReadFile
title: Funzione JetReadFile
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
ms.openlocfilehash: b7f089e87fad910232bae85e14f1d6d2ab6e00b0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470278"
---
# <a name="jetreadfile-function"></a>Funzione JetReadFile


_**Si applica a:** Windows | Windows Server_

## <a name="jetreadfile-function"></a>Funzione JetReadFile

La **funzione JetReadFile** recupera il contenuto di un file aperto con [JetOpenFile.](./jetopenfile-function.md)

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

*Pv*

Buffer di output che riceverà i dati del file.

*Cb*

Dimensione massima in byte del buffer di output.

*pcbActual*

Riceve la quantità effettiva di dati del file recuperati.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a> Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Questo problema può verificarsi <strong>per JetReadFile</strong> quando:</p><ul><li><p>L'handle di istanza specificato non è valido. Windows XP e versioni successive.</p></li><li><p>Le dimensioni del buffer di output non sono un multiplo delle dimensioni della pagina del database (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP e versioni successive.</p></li><li><p>Le dimensioni del buffer di output sono inferiori a tre pagine di database ( JET_paramDatabasePageSize )<a href="gg269337(v=exchg.10).md">e</a>si tratta della prima chiamata a <strong>JetReadFile</strong> per l'handle specificato. Windows XP e versioni successive.</p></li></ul> | 
| <p>JET_errNoBackup</p> | <p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>Jet_errreadverifyfailure</p> | <p>L'operazione non è riuscita perché è stato rilevato un danneggiamento dei dati non ripristinabili durante la lettura di una pagina di database da un file di database o da un file di patch del database.</p> | 
| <p>JET_errLogReadVerifyFailure</p> | <p>L'operazione non è riuscita perché è stato rilevato un danneggiamento dei dati non ripristinabili durante la lettura di un file di log delle transazioni. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza quando in realtà esistono già più istanze.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, il blocco successivo di dati dal file verrà letto nel buffer di output. Verrà restituito anche il numero effettivo di byte recuperati. L'offset del file in corrispondenza del quale verrà eseguita la lettura successiva verrà avanzato di questa quantità.

In caso di errore, lo stato del buffer di output non è definito. L'errore comporta l'annullamento dell'intero processo di backup per l'istanza. In Windows XP e versioni successive, il backup non verrà annullato se si è verificato un errore durante la lettura di un file di database. Tuttavia, il backup del file di database verrà comunque annullato e l'handle corrispondente verrà chiuso automaticamente.

#### <a name="remarks"></a>Commenti

Qualsiasi chiamata a **JetReadFile** che usa un handle che ha già restituito tutti i dati nel file sottostante (ad esempio una chiamata precedente ha restituito meno byte rispetto alle dimensioni del buffer di output) avrà sempre esito positivo, ma restituirà zero byte di dati.

Per ottimizzare le prestazioni di backup, è necessario usare un buffer di output di grandi dimensioni. Potrebbe essere necessaria una sperimentazione per trovare il giusto compromesso tra l'utilizzo delle risorse e la velocità effettiva per una determinata situazione. In ogni caso, il buffer di output non deve essere inferiore a 64 KB.

Non sono supportate più **chiamate simultanee a JetReadFile** usando lo stesso handle di file. Ciò significa che non è possibile accodare diversi buffer per la lettura simultanea nello stesso file per ottenere una velocità effettiva sequenziale elevata. In alternativa, è necessario usare un singolo buffer di grandi dimensioni.

Se l'istanza è configurata in modo che sia abilitato lo scrubbing della pagina del database (vedere JET_paramZeroDatabaseDuringBackup in Parametri di sistema), i dati eliminati verranno rimossi dal database come effetto collaterale di una chiamata a **JetReadFile** sul file di database.

È molto importante comprendere l'interazione tra backup e danneggiamento dei dati. Se il motore di database rileva il danneggiamento dei dati durante un backup, il backup del database interessato o dell'intera istanza avrà esito negativo. Si tratta di una decisione di progettazione consapevole destinata a proteggersi dalla perdita di dati. Se il motore di database ha consentito l'esito positivo di un backup in cui era presente un danneggiamento dei dati, è possibile che un backup precedente non danneggiato possa essere eliminato di conseguenza. Questo sarebbe un problema perché sarebbe possibile correggere il danneggiamento dei dati nell'istanza in tempo reale ripristinando il backup e riproducendo tutti i file di log delle transazioni nel database. Questo scenario di perdita di dati zero presuppone che la registrazione circolare non sia abilitata (vedere [JET_paramCircularLog](./transaction-log-parameters.md) in Parametri [di sistema](./extensible-storage-engine-system-parameters.md)).

È anche importante comprendere che quando è presente il danneggiamento dei dati, il backup di streaming sarà la posizione più probabile in cui verrà rilevato per primo. Questo è il caso perché il backup di streaming è l'unico processo che esegue regolarmente l'analisi di ogni singola pagina del file di database. È anche probabile che il backup di streaming sia il primo processo per rilevare i primi segnali di errore hardware come manifestati da errori intermittenti di danneggiamento dei dati. Ciò è dovuto alla quantità di dati recuperati dal backup e alla velocità con cui vengono recuperati.

Il danneggiamento dei dati viene rilevato dal motore di database tramite l'uso di checksum di blocco. Questi checksum vengono impostati subito prima della scrittura di una pagina del database e vengono verificati in una pagina di database letta. Questo schema consente al motore di database di determinare che i dati sono stati danneggiati a un certo punto, ma non consente al motore di database di determinare l'origine di tale danneggiamento. Storicamente, la causa predominante di tale danneggiamento è stata trovata in origini diverse dal motore di database stesso.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)

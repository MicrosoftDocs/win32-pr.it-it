---
description: 'Altre informazioni su: funzione JetRestore2'
title: Funzione JetRestore2
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb297aac0bc26e50bba519206eff346abb7943c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318085"
---
# <a name="jetrestore2-function"></a>Funzione JetRestore2


_**Si applica a:** Windows | Windows Server_

## <a name="jetrestore2-function"></a>Funzione JetRestore2

Il **JetRestore2** Ripristina e recupera un backup di flusso di un'istanza, inclusi tutti i database collegati. Questa funzione è principalmente per la compatibilità con le versioni precedenti di Windows 2000 e dei motori di database precedenti, in cui è consentita una sola istanza di un database. In questo caso, l'istanza attiva è l'istanza di ripristinata.

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parametri

*SZ*

Cartella in cui si trova il backup. Il backup dovrebbe essere stato generato usando le API [JetBackup](./jetbackup-function.md) .

*szDest*

Nome della cartella in cui verranno copiati e ripristinati i file di database del set di backup. Se questo valore è impostato su NULL (come nel caso della [JetRestore](./jetrestore-function.md)legacy), i file di database verranno copiati e ripristinati nel percorso originale.

*PFN*

Puntatore facoltativo alla funzione che verrà chiamato come informazioni di notifica sullo stato di avanzamento dell'operazione di ripristino.

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
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>L'operazione non è riuscita perché il motore è già inizializzato per questa istanza.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLogSequence</p></td>
<td><p>Il set di file di log dal set di backup e dal percorso del log corrente non corrispondono.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo errore viene restituito da <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> quando il motore è in modalità a istanze diverse e pinstance si riferisce a un'istanza non valida di Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>L'operazione non è riuscita perché alcuni percorsi specificati non sono validi (percorso di backup, percorso di destinazione, log o percorso di sistema per l'istanza).</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch</p></td>
<td><p>L'operazione non è riuscita perché il motore è configurato per l'utilizzo di una dimensione di pagina del database (utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> per <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) che non corrisponde alle dimensioni della pagina del database utilizzate per creare i file di log delle transazioni o i database associati ai file di log delle transazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L'operazione non è riuscita perché i parametri implicavano la modalità a istanza singola (modalità di compatibilità di Windows 2000) e il motore è già in modalità a istanze diverse.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, i file di database del set di backup verranno ripristinati nel percorso e verrà eseguito il ripristino in modo che i database si trovino in uno stato di coerenza transazionale pulito. Il ripristino rieseguirà i file di log dal set di backup e i file di log del percorso del log se tali file esistono. Con questo ripristino verranno apportate modifiche al file del checkpoint, ai file di log delle transazioni e a tutti i database a cui fanno riferimento tali file di log delle transazioni.

In caso di errore, l'istanza rimane in uno stato non inizializzato. È probabile che lo stato dei file di log delle transazioni e di eventuali database a cui fanno riferimento tali file di log delle transazioni sia stato modificato nel tentativo di inizializzare il ripristino e ripristinare i database.

#### <a name="remarks"></a>Commenti

Il processo di ripristino ricostruirà i database collegati all'istanza durante il backup e salverà le modifiche nei file di database. Il risultato sarà costituito da database coerenti con le transazioni. Se possibile, verrà salvata anche nel database le modifiche apportate dal momento in cui è stato eseguito il backup fino a quando non viene rilevata la modifica più recente nei log delle transazioni. Questo potrebbe essere possibile se i log delle transazioni generati dopo l'esecuzione del backup sono ancora presenti nella directory dei log delle transazioni. Si noti che se per l'istanza è stata abilitata la registrazione circolare, i log delle transazioni generati vengono riutilizzati in modo tale che il ripristino possa salvare le modifiche apportate fino al momento del backup. In ogni caso, il processo può richiedere molto tempo se il numero di file di log delle transazioni da riprodurre sui database è di grandi dimensioni.

È necessario chiamare le funzioni [JetRestore](./jetrestore-function.md) su un'istanza prima di chiamare [JetInit](./jetinit-function.md) per l'istanza.

Poiché durante il ripristino viene utilizzato un numero significativo di pagine di database e di log delle transazioni, è presente un'intera serie di errori che potrebbero essere restituiti da queste funzioni. Questi errori possono essere causati da errori di allocazione delle risorse temporanei come Jet_errOutOfMemory a errori che rappresentano danneggiamenti fisici come JET_errReadVerifyFailure, JET_errLogFileCorrupt o JET_errBadPageLink. Questi errori sono quasi sempre causati da problemi hardware e pertanto non possono essere evitati. La gestione non automatica dei file si manifesterà più spesso come JET_errMissingLogFile o JET_errAttachedDatabaseMismatch o JET_errDatabaseSharingViolation o JET_errInvalidLogSequence. Questi errori possono essere evitati dall'applicazione. L'applicazione deve prestare attenzione a proteggere il repository di questi file dalla manipolazione da parte di forze esterne, ad esempio l'utente o altre applicazioni. Se l'applicazione desidera eliminare completamente un'istanza, è necessario eliminare tutti i file associati all'istanza. Sono inclusi il file del checkpoint, i file di log delle transazioni e tutti i file di database collegati all'istanza.

Per i diversi passaggi del ripristino vengono generate voci del registro eventi, tra cui lo stato di riproduzione del log delle transazioni e il risultato finale del ripristino.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetRestore2W</strong> (Unicode) e <strong>JetRestore2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)

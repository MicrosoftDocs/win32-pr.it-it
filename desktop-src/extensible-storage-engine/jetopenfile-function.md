---
description: 'Altre informazioni su: funzione JetOpenFile'
title: Funzione JetOpenFile
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2996ffc46e2f6b37cdfec12cd4ee2fc62efa188a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305732"
---
# <a name="jetopenfile-function"></a>Funzione JetOpenFile


_**Si applica a:** Windows | Windows Server_

## <a name="jetopenfile-function"></a>Funzione JetOpenFile

La funzione **JetOpenFile** apre un database collegato, un file di patch del database o un file di log delle transazioni di un'istanza attiva allo scopo di eseguire un backup fuzzy di streaming. I dati di questi file possono essere successivamente letti tramite l'handle restituito mediante [JetReadFile](./jetreadfile-function.md). L'handle restituito deve essere chiuso utilizzando [JetCloseFile](./jetclosefile-function.md). È necessario che un backup esterno dell'istanza sia stato avviato in precedenza utilizzando [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a>Parametri

*szFileName*

Percorso relativo o assoluto di un database collegato, di un file di patch del database o di un file di log delle transazioni gestito dall'istanza di che verrà letta per il backup.

*phfFile*

Buffer di output che riceve un handle per il file da leggere.

*pulFileSizeLow*

Il buffer di output che riceve i bit 32 meno significativi della dimensione del file.

*pulFileSizeHigh*

Il buffer di output che riceve i 32 bit più significativi della dimensione del file.

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
<td><p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileAccessDenied</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile aprire il file richiesto a causa di una violazione di condivisione o di privilegi insufficienti.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato. Questo errore verrà restituito solo da Windows 2000.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo problema può verificarsi per <strong>JetOpenFile</strong> quando:</p>
<ul>
<li><p>L'handle dell'istanza specificato non è valido (Windows XP e versioni successive).</p></li>
<li><p>Il parametro filename specificato è NULL o una stringa di lunghezza zero (Windows XP e versioni successive).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFileToBackup</p></td>
<td><p>Non è stato possibile aprire il file richiesto per il backup perché non è stato trovato. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento. <strong>JetOpenFile</strong> restituirà JET_errOutOfMemory se viene effettuato un tentativo di aprire un altro file prima che il file precedente aperto utilizzando <strong>JetOpenFile</strong> sia stato chiuso da <a href="gg294127(v=exchg.10).md">JetCloseFile</a>. Attualmente è supportato un solo handle di file in attesa.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata. JET_errRestoreInProgress non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, verrà restituito un handle per il file richiesto. Se l'handle è per un file di database, il file di database verrà preparato per il backup di flusso, che può comportare la creazione di un file di patch del database nello stesso percorso del file di database. Il file di patch del database ha esattamente lo stesso percorso e il nome file del file di database, ma dispone di un. Estensione PAT. Verranno restituite anche le dimensioni del file.

In caso di errore, lo stato dei buffer di output sarà indefinito. Un file di patch del database può essere temporaneamente creato sul disco ed è possibile che qualsiasi file esistente nel percorso del file di patch venga eliminato. L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza. In Windows XP e versioni successive, il backup non verrà annullato se è stato effettuato un tentativo di eseguire il backup di un database non collegato all'istanza al momento della chiamata.

**Avviso**  di  Per motivi di sicurezza, è importante tenere presente che **JetOpenFile** non verifica che il percorso del file richiesto sia associato al set di file di cui eseguire il backup per l'istanza di. Di conseguenza, è possibile usare questa funzione per accedere a qualsiasi file che può essere aperto dal contesto di sicurezza corrente del thread. È fondamentale che l'applicazione limiti i percorsi passati a questa funzione a un set noto di percorsi di file validi oppure che sia possibile che si verifichi una divulgazione di attacchi informativi.

#### <a name="remarks"></a>Commenti

È necessario che siano presenti i buffer di output delle dimensioni del file e dell'handle. Se non sono presenti, il motore si arresterà in modo anomalo perché i parametri del buffer di output non vengono convalidati.

A questo punto, è possibile aprire un solo file per il backup in qualsiasi momento.

**JetOpenFile** non dichiara il privilegio di backup prima di aprire il file richiesto.

La dimensione del file da leggere come indicato da questa funzione potrebbe non corrispondere a quella del file su disco. In Windows XP e versioni successive, le informazioni aggiuntive possono essere aggiunte a un file di database utilizzato dal motore di database durante un'operazione di ripristino. Di conseguenza, l'applicazione deve basarsi solo sulle dimensioni del file restituite da **JetOpenFile** o sul numero effettivo di byte di dati restituiti da [JetReadFile](./jetreadfile-function.md).

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
<td><p>Implementato come <strong>JetOpenFileW</strong> (Unicode) e <strong>JetOpenFileA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)

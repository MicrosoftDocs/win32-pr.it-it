---
description: Altre informazioni sulla funzione JetOpenFile
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
ms.openlocfilehash: ffe4527390e21e86ed46820125eb2a422367d8ec
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480377"
---
# <a name="jetopenfile-function"></a>Funzione JetOpenFile


_**Si applica a:** Windows | Windows Server_

## <a name="jetopenfile-function"></a>Funzione JetOpenFile

La **funzione JetOpenFile** apre un database collegato, un file di patch del database o un file di log delle transazioni di un'istanza attiva allo scopo di eseguire un backup fuzzy di streaming. I dati di questi file possono essere successivamente letti tramite l'handle restituito usando [JetReadFile](./jetreadfile-function.md). L'handle restituito deve essere chiuso [tramite JetCloseFile](./jetclosefile-function.md). Un backup esterno dell'istanza deve essere stato avviato in precedenza usando [JetBeginExternalBackup.](./jetbeginexternalbackup-function.md)

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

Percorso relativo o assoluto di un database collegato, di un file di patch del database o di un file di log delle transazioni gestito dall'istanza che verrà letta per il backup.

*phfFile*

Buffer di output che riceve un handle per il file da leggere.

*pulFileSizeLow*

Buffer di output che riceve i 32 bit meno significativi delle dimensioni del file.

*pulFileSizeHigh*

Buffer di output che riceve i 32 bit più significativi delle dimensioni del file.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup.</a> Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errFileAccessDenied</p> | <p>L'operazione non è riuscita perché non è stato possibile aprire il file richiesto a causa di una violazione di condivisione o di privilegi insufficienti.</p> | 
| <p>JET_errFileNotFound</p> | <p>L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato. Questo errore verrà restituito solo da Windows 2000.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Ciò può verificarsi per <strong>JetOpenFile</strong> quando:</p><ul><li><p>L'handle di istanza specificato non è valido (Windows XP e versioni successive).</p></li><li><p>Il parametro filename specificato è NULL o una stringa di lunghezza zero (Windows XP e versioni successive).</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</p> | 
| <p>JET_errMissingFileToBackup</p> | <p>Impossibile aprire il file richiesto per il backup perché non è stato trovato. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errNoBackup</p> | <p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla. <strong>JetOpenFile</strong> restituirà JET_errOutOfMemory se viene effettuato un tentativo di aprire un altro file prima che il file precedente aperto con <strong>JetOpenFile</strong> sia stato chiuso <a href="gg294127(v=exchg.10).md">da JetCloseFile</a>. È attualmente supportato un solo handle di file in sospeso.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza quando in realtà esistono già più istanze.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione. JET_errRestoreInProgress non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 



In caso di esito positivo, verrà restituito un handle per il file richiesto. Se l'handle è per un file di database, tale file di database verrà preparato per il backup di streaming, che potrebbe comportare la creazione di un file di patch del database nello stesso percorso del file di database. Il file di patch del database ha lo stesso percorso e lo stesso nome file del file di database, ma ha un oggetto . Estensione PAT. Verranno restituite anche le dimensioni del file.

In caso di errore, lo stato dei buffer di output non sarà definito. Un file di patch del database può essere creato temporaneamente su disco e qualsiasi file esistente nel percorso del file di patch può essere eliminato. L'errore comporta l'annullamento dell'intero processo di backup per l'istanza. In Windows XP e versioni successive, il backup non verrà annullato se è stato effettuato un tentativo di backup di un database non collegato all'istanza al momento della chiamata.

**Avviso**  Per motivi di sicurezza, è importante notare che **JetOpenFile** non verifica che il percorso del file richiesto sia associato al set di file di cui eseguire il backup per l'istanza. Di conseguenza, è possibile usare questa funzione per accedere a qualsiasi file che può essere aperto dal contesto di sicurezza corrente del thread. È fondamentale che l'applicazione restringa i percorsi passati a questa funzione a un set noto di percorsi di file validi o potrebbe essere reso possibile un attacco di divulgazione di informazioni.

#### <a name="remarks"></a>Commenti

I buffer di output di handle e dimensioni del file devono essere presenti. Se non sono presenti, il motore si arresterà in modo anomalo perché i parametri del buffer di output non vengono convalidati.

Al momento, è possibile aprire un solo file per il backup contemporaneamente.

**JetOpenFile non** asserire il privilegio di backup prima di aprire il file richiesto.

Le dimensioni del file da leggere come segnalato da questa funzione potrebbero non corrispondere alle dimensioni del file su disco. In Windows XP e versioni successive, è possibile aggiungere informazioni aggiuntive a un file di database usato dal motore di database durante un'operazione di ripristino. Di conseguenza, l'applicazione deve basarsi solo sulle dimensioni del file restituite da **JetOpenFile** o sul numero effettivo di byte di dati restituiti [da JetReadFile](./jetreadfile-function.md).

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetOpenFileW</strong> (Unicode) e <strong>JetOpenFileA</strong> (ANSI).</p> | 



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

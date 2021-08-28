---
description: Altre informazioni sulla funzione JetOpenFileInstance
title: Funzione JetOpenFileInstance
TOCTitle: JetOpenFileInstance Function
ms:assetid: 44af9549-77ef-48f4-8580-507f7199f281
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269238(v=EXCHG.10)
ms:contentKeyID: 32765540
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileInstanceA
- JetOpenFileInstanceW
- JetOpenFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba66545c65abcaa3d3969ec7c3d61d73c57be732
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983374"
---
# <a name="jetopenfileinstance-function"></a>Funzione JetOpenFileInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetopenfileinstance-function"></a>Funzione JetOpenFileInstance

La **funzione JetOpenFileInstance** apre un database collegato, un file di patch del database o un file di log delle transazioni di un'istanza attiva allo scopo di eseguire un backup fuzzy di flusso. I dati di questi file possono essere successivamente letti tramite l'handle restituito [usando JetReadFileInstance.](./jetreadfileinstance-function.md) L'handle restituito deve essere chiuso [tramite JetCloseFileInstance.](./jetclosefileinstance-function.md) Un backup esterno dell'istanza deve essere stato avviato in precedenza [tramite JetBeginExternalBackupInstance.](./jetbeginexternalbackupinstance-function.md)

**Windows XP:****JetOpenFileInstance** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetOpenFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Istanza di da utilizzare per questa chiamata.

Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza. L'uso di questa istanza globale è implicito in questo caso.

Per Windows XP e versioni successive, la variante api che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza. In caso contrario, l'operazione avrà esito negativo JET_errRunningInMultiInstanceMode.

*szFileName*

Percorso relativo o assoluto di un database collegato, di un file di patch del database o di un file di log delle transazioni gestito dall'istanza di letta per il backup.

*phfFile*

Puntatore al buffer di output che riceve un handle per il file da leggere.

*pulFileSizeLow*

Puntatore al buffer di output che riceve i 32 bit meno significativi delle dimensioni del file.

*pulFileSizeHigh*

Puntatore al buffer di output che riceve i 32 bit più significativi delle dimensioni del file.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg269309(v=exchg.10).md">JetStopBackupInstance.</a> Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutta l'attività nell'istanza associata alla sessione è stata finisce in seguito a una chiamata a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance.</a></p> | 
| <p>JET_errFileAccessDenied</p> | <p>L'operazione non è riuscita perché non è stato possibile aprire il file richiesto a causa di una violazione di condivisione o di privilegi insufficienti.</p> | 
| <p>JET_errFileNotFound</p> | <p>L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato. Questo errore verrà restituito solo da Windows 2000.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza.</p> | 
| <p>JET_errInvalidPath</p> | <p>L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questa operazione può verificarsi <strong>per JetOpenFileInstance</strong> quando:</p><ul><li><p>L'handle di istanza specificato non è valido (Windows XP e versioni successive).</p></li><li><p>Il parametro filename specificato è NULL o una stringa di lunghezza zero (Windows XP e versioni successive).</p></li></ul> | 
| <p>JET_errMissingFileToBackup</p> | <p>Impossibile aprire il file richiesto per il backup perché non è stato trovato. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errNoBackup</p> | <p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla. <strong>JetOpenFileInstance</strong> restituirà JET_errOutOfMemory se viene effettuato un tentativo di aprire un altro file prima che il file precedente aperto con <strong>JetOpenFileInstance</strong> sia stato chiuso da <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>. Attualmente è supportato un solo handle di file in sospeso.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza quando in realtà esistono già più istanze.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, viene restituito un handle per il file richiesto. Se l'handle è per un file di database, tale file di database verrà preparato per un backup di flusso che potrebbe comportare la creazione di un file di patch del database nello stesso percorso del file di database. Il file di patch del database ha esattamente lo stesso percorso e lo stesso nome file del file di database, ma con . Estensione PAT. Verranno restituite anche le dimensioni del file.

In caso di errore, lo stato dei buffer di output non sarà definito. Un file di patch del database può essere creato temporaneamente su disco ed è possibile eliminare qualsiasi file esistente nel percorso del file di patch. L'errore comporta l'annullamento dell'intero processo di backup per l'istanza. In Windows XP e versioni successive, il backup non verrà annullato se è stato effettuato un tentativo di backup di un database non collegato all'istanza al momento della chiamata.

**Avviso**  Per motivi di sicurezza, è importante notare che **JetOpenFileInstance** non verifica che il percorso del file richiesto sia associato al set di file di cui viene eseguito il backup per l'istanza. Di conseguenza, è possibile usare questa funzione per accedere a qualsiasi file che può essere aperto dal contesto di sicurezza corrente del thread. È fondamentale che l'applicazione restringa i percorsi passati a questa funzione a un set noto di percorsi di file validi o potrebbe essere resa possibile la divulgazione di informazioni.

#### <a name="remarks"></a>Commenti

I buffer di output dell'handle e delle dimensioni del file devono essere presenti. Se non sono presenti, il motore si arresterà in modo anomalo perché i parametri del buffer di output non vengono convalidati.

Al momento, è possibile aprire un solo file per il backup alla volta.

**JetOpenFileInstance non** asserzione del privilegio di backup prima di aprire il file richiesto.

Le dimensioni del file da leggere come segnalato da questa funzione potrebbero non corrispondere alle dimensioni del file su disco. In Windows XP e versioni successive, è possibile aggiungere informazioni aggiuntive a un file di database usato dal motore di database durante un'operazione di ripristino. Di conseguenza, l'applicazione deve basarsi solo sulle dimensioni del file restituite da **JetOpenFileInstance** o sul numero effettivo di byte di dati restituiti da [JetReadFileInstance.](./jetreadfileinstance-function.md)

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetOpenFileInstanceW</strong> (Unicode) e <strong>JetOpenFileInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFileInstance](./jetclosefileinstance-function.md)  
[JetGetAttachInfoInstance](./jetgetattachinfoinstance-function.md)  
[JetGetLogInfoInstance](./jetgetloginfoinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopBackupInstance](./jetstopbackupinstance-function.md)  
[JetTruncateLogInstance](./jettruncateloginstance-function.md)

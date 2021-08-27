---
description: 'Altre informazioni su: Funzione JetRestore'
title: Funzione JetRestore
TOCTitle: JetRestore Function
ms:assetid: cdfb8823-6260-46f2-adfc-77e2512a68fd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294093(v=EXCHG.10)
ms:contentKeyID: 32765708
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore
- JetRestoreW
- JetRestoreA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b6699a6241f41b8bd2ef2aa07025e86454c0e6c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985674"
---
# <a name="jetrestore-function"></a>Funzione JetRestore


_**Si applica a:** Windows | Windows Server_

## <a name="jetrestore-function"></a>Funzione JetRestore

La **funzione JetRestore** ripristina e ripristina un backup di flusso di un'istanza, inclusi tutti i database collegati. Questa funzione è principalmente per la compatibilità con le versioni precedenti Windows 2000 e con i motori di database precedenti, in cui è consentita una sola istanza di un database. In questo caso, l'istanza attiva è l'istanza ripristinata. Con **JetRestore** non è possibile specificare il percorso per i database ripristinati.

```cpp
JET_ERR JET_API JetRestore(
  __in          JET_PCSTR sz,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a>Parametri

*Sz*

Cartella in cui si trova il backup. Il backup dovrebbe essere stato generato usando la [funzione JetBackup.](./jetbackup-function.md)

*Pfn*

Puntatore facoltativo alla funzione che verrà chiamato come informazioni di notifica sullo stato di avanzamento dell'operazione di ripristino.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>L'operazione non è riuscita perché il motore è già inizializzato per questa istanza.</p> | 
| <p>JET_errInvalidLogSequence</p> | <p>Il set di file di log dal set di backup e dal percorso del log corrente non corrisponde.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</p> | 
| <p>JET_errInvalidPath</p> | <p>L'operazione non è riuscita perché alcuni percorsi specificati non sono validi (percorso di backup, percorso di destinazione, log o percorso di sistema per l'istanza).</p> | 
| <p>JET_errPageSizeMismatch</p> | <p>L'operazione non è riuscita perché il motore è configurato per l'utilizzo delle dimensioni di pagina del database (tramite <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> per <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) che non corrispondono alle dimensioni della pagina del database utilizzate per creare i file di log delle transazioni o i database associati ai file di log delle transazioni.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>L'operazione non è riuscita perché i parametri hanno implicito la modalità a istanza singola (modalità di compatibilità Windows 2000) e il motore è già in modalità a istanza multipla.</p> | 



In caso di esito positivo, i file di database del set di backup verranno ripristinati nel percorso e il ripristino verrà eseguito in modo che i database siano in uno stato di coerenza transazionale pulita. Il ripristino rieseguirà i file di log dal set di backup e i file di log dal percorso del log, se tali file esistono. Questo recupero comporta modifiche al file del checkpoint, ai file di log delle transazioni e a tutti i database a cui fanno riferimento tali file di log delle transazioni.

In caso di errore, l'istanza rimane in uno stato non inizializzato. È probabile che lo stato dei file di log delle transazioni e di tutti i database a cui fanno riferimento tali file di log delle transazioni sia stato modificato nel tentativo di inizializzare il ripristino e recuperare i database.

#### <a name="remarks"></a>Commenti

Il processo di ripristino ricostruirà i database collegati all'istanza durante il backup e salverà di nuovo le modifiche nei file di database. Il risultato sarà un database coerente con le transazioni. Se possibile, verranno salvate anche nel database le modifiche apportate dopo l'esecuzione del backup fino alla modifica più recente trovata nei log delle transazioni. Ciò è possibile se i log delle transazioni generati dopo l'esecuzione del backup sono ancora presenti nella directory del log delle transazioni. Si noti che se per l'istanza è stata abilitata la registrazione circolare, i log delle transazioni generati vengono riutilizzati in modo che il ripristino sia in grado di salvare le modifiche apportate fino al momento del backup. In ogni caso, questo processo può richiedere molto tempo se il numero di file di log delle transazioni da riprodurre nei database è elevato.

**Le funzioni JetRestore** devono essere chiamate su un'istanza prima [di chiamare JetInit](./jetinit-function.md) per tale istanza.

Poiché durante il recupero verrà usato un numero significativo di pagine di database e log delle transazioni, queste funzioni potrebbero restituire un'intera serie di errori. Tali errori possono essere da errori temporanei di allocazione delle risorse come Jet_errOutOfMemory a errori che rappresentano danneggiamenti fisici come JET_errReadVerifyFailure, JET_errLogFileCorrupt o JET_errBadPageLink. Questi errori sono quasi sempre causati da problemi hardware e pertanto non possono essere evitati. La gestione errata dei file si manifesterà più spesso come JET_errMissingLogFile, JET_errAttachedDatabaseMismatch o JET_errDatabaseSharingViolation o JET_errInvalidLogSequence. Questi errori sono evitabili dall'applicazione. L'applicazione deve prestare attenzione a proteggere il repository di questi file dalla manipolazione da forza esterne, ad esempio l'utente o altre applicazioni. Se l'applicazione vuole eliminare completamente un'istanza, è necessario eliminare tutti i file associati all'istanza. Sono inclusi il file del checkpoint, i file di log delle transazioni e tutti i file di database collegati all'istanza.

Nei diversi passaggi del ripristino verranno generate voci del registro eventi, tra cui lo stato di avanzamento della riproduzione del log delle transazioni e il risultato finale del ripristino.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetRestoreW</strong> (Unicode) e <strong>JetRestoreA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)

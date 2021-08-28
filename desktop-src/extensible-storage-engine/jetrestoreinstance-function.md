---
description: Altre informazioni sulla funzione JetRestoreInstance
title: Funzione JetRestoreInstance
TOCTitle: JetRestoreInstance Function
ms:assetid: 7ba2b6ee-96f5-44c5-9842-5e58580f60f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269306(v=EXCHG.10)
ms:contentKeyID: 32765597
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestoreInstanceW
- JetRestoreInstance
- JetRestoreInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 700cbb29fe34700da953df5a20aa94d5a2df4a06
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985664"
---
# <a name="jetrestoreinstance-function"></a>Funzione JetRestoreInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetrestoreinstance-function"></a>Funzione JetRestoreInstance

La **funzione JetRestoreInstance** ripristina e ripristina un backup in streaming di un'istanza, inclusi tutti i database collegati. È progettato per funzionare con un backup creato con la [funzione JetBackupInstance.](./jetbackupinstance-function.md) Si tratta della funzione di ripristino più semplice e incapsulata.

**Windows XP:****JetRestoreInstance** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetRestoreInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Specifica l'istanza di da utilizzare per questa chiamata.

Per Windows XP e versioni successive, l'uso di questo parametro dipende dalla modalità operativa del motore. Se il motore funziona in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza, questo parametro può essere NULL oppure può essere impostato su un buffer di output valido contenente NULL o JET_instanceNil che restituirà l'handle di istanza globale creato come effetto collaterale dell'inizializzazione. Questo handle di istanza può quindi essere passato a qualsiasi altra API che accetta un'istanza di . Se il motore funziona in modalità a istanze multipla, questo parametro deve essere impostato su un buffer di input valido contenente l'handle di istanza restituito da [JetCreateInstance](./jetcreateinstance-function.md) in fase di inizializzazione.

*Sz*

Cartella in cui si trova il backup. Il backup deve essere stato generato usando le API [JetBackup.](./jetbackup-function.md)

*szDest*

Nome della cartella in cui verranno copiati e ripristinati i file di database del set di backup. Se questa proprietà è impostata su NULL (come nel caso di [JetRestore](./jetrestore-function.md)legacy), i file di database verranno copiati e ripristinati nel percorso originale.

*Pfn*

Puntatore facoltativo alla funzione che verrà chiamata come informazioni di notifica sullo stato dell'operazione di ripristino.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>L'operazione non è riuscita perché il motore è già inizializzato per questa istanza.</p> | 
| <p>JET_errInvalidLogSequence</p> | <p>Il set di file di log dal set di backup e dal percorso del log corrente non corrisponde.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Questo errore verrà restituito da <strong>JetRestoreInstance</strong> quando il motore è in modalità a istanze multipla e pinstance fa riferimento a un'istanza non valida Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidPath</p> | <p>L'operazione non è riuscita perché alcuni percorsi specificati non sono validi (il percorso di backup, il percorso di destinazione, il percorso di log o di sistema per l'istanza).</p> | 
| <p>JET_errPageSizeMismatch</p> | <p>L'operazione non è riuscita perché il motore è configurato per l'uso di dimensioni di pagina del database (tramite <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> per <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) che non corrispondono alle dimensioni della pagina del database utilizzate per creare i file di log delle transazioni o i database associati ai file di log delle transazioni.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>L'operazione non è riuscita perché i parametri implicano la modalità a istanza singola (Windows modalità di compatibilità 2000) e il motore è già in modalità a istanza multipla.</p> | 



In caso di esito positivo, i file di database del set di backup verranno ripristinati nel percorso e il ripristino verrà eseguito in modo che i database siano in uno stato di coerenza transazionale pulita. Il ripristino rieseguirà i file di log dal set di backup e i file di log dal percorso del log, se tali file esistono. Questo ripristino comporta modifiche al file del checkpoint, ai file di log delle transazioni e ai database a cui fanno riferimento tali file di log delle transazioni.

In caso di errore, l'istanza rimane in uno stato non inizializzato. È probabile che lo stato dei file di log delle transazioni e di tutti i database a cui fanno riferimento tali file di log delle transazioni sia stato modificato nel tentativo di inizializzare il ripristino e il ripristino dei database.

#### <a name="remarks"></a>Commenti

Il processo di ripristino ricostruirà i database collegati all'istanza durante il backup e salverà le modifiche nei file di database. Il risultato sarà database coerenti con le transazioni. Se possibile, salva anche nel database le modifiche apportate dopo il backup fino alla modifica più recente trovata nei log delle transazioni. Ciò sarebbe possibile se i log delle transazioni generati dopo l'esecuzione del backup sono ancora presenti nella directory del log delle transazioni. Si noti che se per l'istanza è stata abilitata la registrazione circolare, i log delle transazioni generati vengono riutilizzati in modo che il ripristino sia in grado di salvare le modifiche apportate fino al momento del backup. In ogni caso, questo processo può richiedere molto tempo se il numero di file di log delle transazioni da riprodurre nei database è elevato.

**JetRestoreInstance** deve essere chiamato su un'istanza già creata usando [JetCreateInstance](./jetcreateinstance-function.md).

Poiché durante il ripristino verrà usato un numero significativo di pagine di database e log delle transazioni, queste funzioni potrebbero restituire un'intera serie di errori. Tali errori possono essere da errori temporanei di allocazione delle risorse come Jet_errOutOfMemory errori che rappresentano danneggiamenti fisici come JET_errReadVerifyFailure, JET_errLogFileCorrupt o JET_errBadPageLink. Questi errori sono quasi sempre causati da problemi hardware e pertanto non possono essere evitati. La gestione errata dei file si manifesterà più spesso come JET_errMissingLogFile o JET_errAttachedDatabaseMismatch o JET_errDatabaseSharingViolation o JET_errInvalidLogSequence. Questi errori sono evitabili dall'applicazione. L'applicazione deve prestare attenzione a proteggere il repository di questi file dalla manipolazione da parte di forze esterne, ad esempio l'utente o altre applicazioni. Se l'applicazione vuole eliminare completamente un'istanza, è necessario eliminare tutti i file associati all'istanza. tra cui il file del checkpoint, i file di log delle transazioni e tutti i file di database collegati all'istanza.

Nei diversi passaggi del ripristino verranno generate voci del log eventi, tra cui lo stato di riproduzione del log delle transazioni e il risultato finale del ripristino.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetRestoreInstanceW</strong> (Unicode) e <strong>JetRestoreInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)

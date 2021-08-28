---
description: Altre informazioni sulla funzione JetBackup
title: Funzione JetBackup
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e17ee5029da8ac71b5421e44a3647494e676ba71
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982994"
---
# <a name="jetbackup-function"></a>Funzione JetBackup


_**Si applica a:** Windows | Windows Server_

## <a name="jetbackup-function"></a>Funzione JetBackup

La **funzione JetBackup** crea un backup del database mentre il database è online. Questa funzione è principalmente per la compatibilità con le versioni precedenti Windows 2000 e versioni precedenti dei motori di database, in cui è consentita una sola istanza di un database. In questo caso, l'istanza attiva è l'istanza di cui viene eseguito il backup.

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parametri

*szBackupPath*

Directory in cui è archiviato il backup. Se il percorso di backup è NULL, la funzione tronca i log, se possibile.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Crea un backup completo del database. In questo modo è possibile conservare un backup esistente nella stessa directory in caso di errore del nuovo backup.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Crea un backup incrementale anziché un backup completo. Ciò significa che verrà eseguito il backup solo dei file di log dopo l'ultimo backup completo o incrementale.</p> | 



*pfnStatus*

Puntatore alla funzione [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback, che fornisce informazioni di notifica sullo stato di avanzamento dell'operazione di backup.

### <a name="return-value"></a>Valore restituito

La funzione restituisce uno dei [codici](./jet-err.md) JET_ERR di errore. Di seguito sono riportati i valori restituiti più comunemente. Per un elenco completo degli errori per questa API, vedere Codici di errore del motore Archiviazione [estendibile.](./extensible-storage-engine-error-codes.md)


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupInProgress</p> | <p>È già in corso un backup per la stessa istanza. Non sono consentiti più backup contemporaneamente.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>L'istanza non è ancora pronta per il backup durante l'inizializzazione.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong> Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errInvalidBackup</p> | <p>Un backup incrementale non è consentito se la registrazione circolare è attivata.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Le opzioni specificate non sono valide.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Nell'API è stato passato un parametro non valido.</p> | 
| <p>JET_errInvalidPath</p> | <p>Il percorso di destinazione non esiste.</p> | 
| <p>JET_errLoggingDisabled</p> | <p>L'istanza è in esecuzione senza registrazione. Non è consentito alcun backup.</p> | 
| <p>JET_errLogReadVerifyFailure</p> | <p>Si è verificato un errore di verifica del checksum in un file di log.</p> | 
| <p>JET_errLogWriteFail</p> | <p>La registrazione per l'istanza è temporanea o disabilitata in modo permanente a causa di un errore imprevisto.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>Jet_errreadverifyfailure</p> | <p>Si è verificato un errore di verifica del checksum in una pagina del database.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p><strong>Windows XP:</strong> Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



Se la funzione ha esito positivo, tutti i file necessari per un ripristino fino al momento del backup saranno contenuti nella directory di backup. Se si tratta di un backup completo, i file saranno i file di database e i file di log necessari per portare il database a uno stato coerente. Se si tratta di un backup incrementale, solo i file di log verranno aggiunti alle directory, ma i file già esistenti (database e file di log), insieme ai nuovi file di log, potranno essere ripristinati per riportare il database allo stato in cui si trova al momento dell'inizio del backup.

Come effetto collaterale del backup, i file di log che non sono più necessari verranno troncati.

Nello stesso tempo, le intestazioni del database verranno aggiornate con le informazioni quando è stato eseguito l'ultimo backup.

Se la funzione ha esito negativo, non saranno presenti file nella destinazione della directory di backup, quindi non sarà possibile eseguire il ripristino. Contemporaneamente, i file di log correnti non verranno troncati.

#### <a name="remarks"></a>Commenti

Nei diversi passaggi del backup verranno generate voci del registro eventi, inclusi i nomi dei file, il troncamento del log e il risultato finale del backup.

I backup incrementali sono possibili solo dopo l'esecuzione di un backup completo. Inoltre, i backup incrementali sono possibili solo se la registrazione circolare è disattivata. È consigliabile che la directory di backup non contenga file diversi da quello usato nel backup o aggiunto da un backup riuscito precedente.

La directory di backup deve esistere a meno che il parametro *JET_paramCreatePathIfNotExist* impostato per l'istanza. Per informazioni, vedere [Parametri di sistema](./extensible-storage-engine-system-parameters.md).

Il backup verificherà il checksum in tutte le pagine del database usate e a partire da Windows Server 2003, anche nei file di log. Ciò consente di stimare l'integrità del database, anche per le pagine che non vengono lette durante le normali operazioni. Se viene rilevato un tale danneggiamento, il backup avrà esito negativo.

Durante il backup, il file di log corrente verrà completato e verrà generato un nuovo log. In questo modo, tutti i file di log necessari possono essere copie, perché il log corrente non sarà più in uso.

È consigliabile non usare il backup per scopi diversi dal backup e dal ripristino a livello di motore. In questo modo si riduce al minimo la possibilità di errori durante le operazioni di backup e ripristino.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetBackupW</strong> (Unicode) e <strong>JetBackupA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[File extensible Archiviazione Engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)

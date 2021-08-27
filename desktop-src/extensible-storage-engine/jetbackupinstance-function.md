---
description: Altre informazioni sulla funzione JetBackupInstance
title: Funzione JetBackupInstance
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 138d95c80070d8e1b1d7c958534cd93965db47aa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472667"
---
# <a name="jetbackupinstance-function"></a>Funzione JetBackupInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetbackupinstance-function"></a>Funzione JetBackupInstance

La **funzione JetBackupInstance** esegue un backup in streaming di un'istanza, inclusi tutti i database collegati, in una directory. Con più metodi di backup supportati dal motore, questa è la funzione più semplice e incapsulata.

**Windows XP: JetBackupInstance** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Istanza del database di cui eseguire il backup.

*szBackupPath*

Directory in cui è archiviato il backup. Se il percorso di backup è NULL per l'uso della funzione, i log verranno troncati, se possibile.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Crea un backup completo del database. In questo modo è possibile conservare un backup esistente nella stessa directory in caso di errore del nuovo backup.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Crea un backup incrementale anziché un backup completo. Ciò significa che verrà eseguito il backup solo dei file di log creati dopo l'ultimo backup completo o incrementale.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Riservato per utilizzi futuri.</p> | 



*pfnStatus*

Puntatore alla funzione [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback, che fornisce informazioni di notifica sullo stato dell'operazione di backup.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupInProgress</p> | <p>È già in corso un backup per la stessa istanza. Non sono consentiti più backup contemporaneamente.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>L'istanza non è ancora pronta per il backup durante l'inizializzazione.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance.</a></p> | 
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



Dopo che la funzione ha restituito l'esito positivo, nella directory di backup saranno presenti tutti i file necessari per un ripristino fino al momento del backup. Se si tratta di un backup completo, i file saranno i file di database e i file di log necessari per portare il database a uno stato coerente. Se si tratta di un backup incrementale, solo i file di log verranno aggiunti alle directory, ma i file già esistenti (database e file di log) insieme ai nuovi file di log potranno essere ripristinati e ripristinare lo stato del database al momento del backup.

Come effetto collaterale del backup, i file di log che non sono più necessari verranno troncati.

Nello stesso tempo, le intestazioni del database verranno aggiornate con le informazioni quando è stato eseguito l'ultimo backup.

In caso di errore, non saranno presenti file nella destinazione della directory di backup, quindi non sarà possibile eseguire il ripristino. Contemporaneamente, i file di log correnti non verranno troncati.

#### <a name="remarks"></a>Commenti

Nei diversi passaggi del backup verranno generate voci del registro eventi, inclusi i nomi dei file, il troncamento del log e il risultato finale del backup.

Il backup incrementale è possibile solo dopo l'esecuzione di un backup completo. Inoltre, i backup incrementali sono possibili solo se la registrazione circolare è disattivata. È consigliabile che la directory di backup non contenga altri file, quindi quello interessato dal backup o aggiunto da un backup riuscito precedente.

La directory di backup deve esistere a meno che il parametro *JET_paramCreatePathIfNotExist* impostato per l'istanza. Per informazioni, vedere [Parametri di sistema](./extensible-storage-engine-system-parameters.md).

Il backup verificherà il checksum in tutte le pagine del database usate e a partire da Windows Server 2003, anche nei file di log. In questo modo è possibile stimare l'integrità del database anche per le pagine che non vengono lette durante le normali operazioni. Se si verifica un tale danneggiamento, il backup avrà esito negativo.

Durante il backup, il file di log corrente verrà completato e verrà avviata una nuova generazione di log. In questo modo sarà possibile copiare i file di log necessari perché l'ultimo file necessario non sarà più in uso.

È consigliabile non usare il backup per altri scopi e quindi il backup e il ripristino a livello di motore. In questo modo si riduce al minimo la modifica di errori durante le operazioni di backup e ripristino.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetBackupInstanceW</strong> (Unicode) e <strong>JetBackupInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)

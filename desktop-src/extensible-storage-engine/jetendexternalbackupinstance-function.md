---
description: Altre informazioni sulla funzione JetEndExternalBackupInstance
title: Funzione JetEndExternalBackupInstance
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f82af0be3185db36498d9a5888da190e92314184
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479177"
---
# <a name="jetendexternalbackupinstance-function"></a>Funzione JetEndExternalBackupInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetendexternalbackupinstance-function"></a>Funzione JetEndExternalBackupInstance

La **funzione JetEndExternalBackupInstance** termina una sessione di backup esterna. Questa API è l'ultima API di una serie di API che devono essere chiamate per eseguire correttamente un backup online (non basato su VSS).

**Windows XP: JetEndExternalBackupInstance** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Istanza di da utilizzare per questa chiamata.

**Windows 2000:** Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza. L'uso di questa istanza globale è implicito in questo caso.

**Windows XP:** Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza. In caso contrario, l'operazione avrà esito negativo con JET_errRunningInMultiInstanceMode.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupAbortByCaller</p> | <p><strong>Windows XP:</strong> Questo valore restituito è stato introdotto in Windows XP.</p><p>Il chiamante ha terminato un backup al centro della sequenza di backup senza segnalare l'intenzione con <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Questo errore è il risultato di un bug nel client di backup in Windows Server 2003 e versioni successive. In Windows XP questo errore viene restituito per una terminazione intenzionale della sequenza di backup esterna.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p><strong>Windows Server 2003:</strong> Questo valore restituito è stato introdotto in Windows Server 2003.</p><p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup.</a></p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p><strong>Windows XP:</strong> Questo valore restituito è stato introdotto in Windows XP.</p><p>Impossibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p> | 
| <p>JET_errNoBackup</p> | <p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza, quando in realtà esistono già più istanze.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



Se la funzione ha esito positivo, il backup esterno ha avuto esito positivo. Esito positivo indica che tutti i file (ad esempio, database e log) appropriati per il tipo di backup (specificato in [JetBeginExternalBackup)](./jetbeginexternalbackup-function.md)sono stati recuperati dal motore di backup. I file di cui è stato eseguito il backup possono essere ripristinati con il ripristino rigido ([JetExternalRestore](./jetexternalrestore-function.md)).

Se questa funzione ha esito negativo, il backup esterno termina in genere. L'errore indica che il backup non è valido a causa di un client o di un errore di utilizzo dell'applicazione. È importante controllare il codice restituito per questa API per verificare che la sequenza di backup sia riuscita.

#### <a name="remarks"></a>Commenti

Se il motore è configurato per registrare gli eventi, viene registrato un evento per indicare la risoluzione del backup esterno.

Se la sequenza di backup non viene completata nell'ordine e con una chiamata riuscita a [JetEndExternalBackup,](./jetendexternalbackup-function.md)i backup incrementali successivi potrebbero contenere più dati di quanto previsto dall'applicazione.

Per altre informazioni sulla sequenza dell'API di backup esterna, vedere [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

Prima Windows Vista, se il troncamento del log non è stato eseguito, il motore ha considerato che il backup era un backup di copia. Tuttavia, il backup potrebbe essere un backup normale per cui non è stato eseguito il troncamento (ad esempio, se sono presenti database scollegati). L JET_bitBackupTruncateDone'opzione può essere usata per informare il motore di questo problema e consentire le modifiche appropriate all'intestazione del database.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[Parametri di gestione degli errori](./error-handling-parameters.md)  
[Errori del motore Archiviazione estendibile](./extensible-storage-engine-errors.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JET_ERR](./jet-err.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)

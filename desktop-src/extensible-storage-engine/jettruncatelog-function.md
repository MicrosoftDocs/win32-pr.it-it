---
description: Altre informazioni sulla funzione JetTruncateLog
title: Funzione JetTruncateLog
TOCTitle: JetTruncateLog Function
ms:assetid: 60cbf563-4228-452a-9b20-c7b1330c4514
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269263(v=EXCHG.10)
ms:contentKeyID: 32765565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa924a7061e834d4398ed68adb800912261279f7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474357"
---
# <a name="jettruncatelog-function"></a>Funzione JetTruncateLog


_**Si applica a:** Windows | Windows Server_

## <a name="jettruncatelog-function"></a>Funzione JetTruncateLog

La **funzione JetTruncateLog** viene usata durante un backup avviato da [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) per eliminare tutti i file di log delle transazioni che non saranno più necessari al termine del backup corrente.

```cpp
    JET_ERR JET_API JetTruncateLog(void);
```

### <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup.</a></p><p><strong>Windows Server 2003:</strong>  Questo valore restituito è stato introdotto in Windows Server 2003.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza. <strong>JetTruncateLog restituirà</strong> questo errore se sono presenti handle di file in sospeso creati usando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> per l'istanza.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto oppure la combinazione di diversi parametri ha restituito un risultato imprevisto. Ciò può verificarsi per <strong>JetTruncateLog</strong> quando l'handle di istanza specificato non è valido.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errNoBackup</p> | <p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza, quando in realtà esistono già più istanze.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



Se questa funzione ha esito positivo, viene eliminato il set di file di log delle transazioni che non saranno più necessari al termine del backup corrente. La macchina a stati di backup sarà avanzata in modo che il backup dei file di database non sia più consentito. Solo i file di patch del database e i file di log delle transazioni possono essere aperti per il backup oltre questo punto.

Se questa funzione ha esito negativo, la macchina a stati di backup può essere avanzata in modo che il backup dei file di database non sia più consentito. È possibile che venga eliminato un numero di file di log delle transazioni inferiore al numero desiderato, ma che verranno sempre eliminati dal meno recente al più recente.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[File del motore Archiviazione estendibile](./extensible-storage-engine-files.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)

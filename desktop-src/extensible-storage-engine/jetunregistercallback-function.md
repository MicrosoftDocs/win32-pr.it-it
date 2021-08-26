---
description: 'Altre informazioni su: Funzione JetUnregisterCallback'
title: Funzione JetUnregisterCallback
TOCTitle: JetUnregisterCallback Function
ms:assetid: de5c7afa-07e1-4687-989b-b56125a9712e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294116(v=EXCHG.10)
ms:contentKeyID: 32765730
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUnregisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5cb60d8b0d06ff6af9d950c53d8bdf8f4eedb774
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466247"
---
# <a name="jetunregistercallback-function"></a>Funzione JetUnregisterCallback


_**Si applica a:** Windows | Windows Server_

## <a name="jetunregistercallback-function"></a>Funzione JetUnregisterCallback

La **funzione JetUnregisterCallback** consente all'applicazione di configurare il motore di database per arrestare l'invio di notifiche all'applicazione come richiesto in precedenza [tramite JetRegisterCallback.](./jetregistercallback-function.md)

**Windows XP:****JetUnregisterCallback** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetUnregisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_HANDLE hCallbackId
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*cbtyp*

Maschera di bit composta dai motivi di callback per cui l'applicazione non desidera più ricevere notifiche.

Per creare questa maschera di bit, è sufficiente o insieme i motivi di callback validi [dall'JET_CBTYP](./jet-cbtyp.md) predefinita.

*hCallbackId*

Handle del callback registrato restituito da [JetRegisterCallback.](./jetregistercallback-function.md)

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>L'operazione non può essere completata perché tutte le attività nell'istanza associata alla sessione sono scadute in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>L'operazione non può essere completata perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



Se questa funzione ha esito positivo, la registrazione del callback specificato verrà annullata per i motivi di callback specificati con la tabella associata al cursore specificato. Non verrà apportata alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, la registrazione del callback specificato non verrà annullata. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

La maschera di bit specificata deve corrispondere esattamente alla maschera di bit specificata durante la registrazione del callback. Il motore di database attualmente non supporta la rimozione di un subset di queste notifiche e non restituisce un errore quando si tenta di eseguire questa operazione.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRegisterCallback](./jetregistercallback-function.md)  
[JetStopService](./jetstopservice-function.md)

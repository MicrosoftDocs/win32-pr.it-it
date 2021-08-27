---
description: Altre informazioni sulla funzione JetRegisterCallback
title: Funzione JetRegisterCallback
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ef90466b736facf5bd9fefee31c0449964d003b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985804"
---
# <a name="jetregistercallback-function"></a>Funzione JetRegisterCallback


_**Si applica a:** Windows | Windows Server_

## <a name="jetregistercallback-function"></a>Funzione JetRegisterCallback

La **funzione JetRegisterCallback** consente all'applicazione di configurare il motore di database per inviare notifiche all'applicazione per eventi specifici. Queste notifiche sono associate a una tabella specifica e rimangono effettive solo fino a quando l'istanza contenente la tabella non viene arrestata tramite [JetTerm](./jetterm-function.md).

**Windows XP: JetRegisterCallback** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*cbtyp*

Maschera di bit composta dai motivi di callback per cui l'applicazione desidera ricevere notifiche.

Per creare questa maschera di bit, semplicemente o insieme, i motivi di callback validi [dall'JET_CBTYP](./jet-cbtyp.md) predefinita.

*pCallback*

Puntatore a funzione alla funzione di callback per l'applicazione.

*pvContext*

Specifica un puntatore di contesto che verrà assegnato alla funzione di callback per l'applicazione.

*phCallbackId*

Restituisce un handle che può essere usato in un secondo momento per annullare la registrazione della funzione di callback specificata [tramite JetUnregisterCallback.](./jetunregistercallback-function.md)

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Questo errore verrà restituito da <strong>JetRegisterCallback</strong> quando:</p><ul><li><p><em>cbtyp</em> è zero,</p></li><li><p><em>pCallback</em> è NULL.</p></li><li><p><em>phCallbackId</em> è NULL.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, il callback specificato verrà registrato per i motivi di callback specificati con la tabella associata al cursore specificato. Non verrà apportata alcuna modifica allo stato del database.

In caso di errore, il callback non verrà registrato. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Questo metodo consente all'applicazione di associare callback volatili a una tabella in un database. Se l'applicazione vuole associare i callback persistenti a una tabella nel database, deve passare il callback a [JET_TABLECREATE](./jet-tablecreate-structure.md) [tramite JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetTerm](./jetterm-function.md)  
[JetUnregisterCallback](./jetunregistercallback-function.md)

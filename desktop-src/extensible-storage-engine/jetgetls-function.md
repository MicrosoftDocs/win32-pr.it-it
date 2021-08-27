---
description: 'Altre informazioni su: Funzione JetGetLS'
title: Funzione JetGetLS
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9eb6eed0bbec7be0acd377fa3b34d1b91a8b3fed
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982544"
---
# <a name="jetgetls-function"></a>Funzione JetGetLS


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetls-function"></a>Funzione JetGetLS

La **funzione JetGetLS** consente all'applicazione di recuperare l'handle di contesto noto come Local Archiviazione associato a un cursore o alla tabella associata a tale cursore. Questo handle di contesto deve essere stato impostato in precedenza [tramite JetSetLS.](./jetsetls-function.md) **JetGetLS può essere** usato anche per recuperare contemporaneamente l'handle di contesto corrente per un cursore o una tabella e reimpostare tale handle di contesto.

**Windows XP: JetGetLS** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*pls*

Buffer di output che riceve l'handle di contesto attualmente associato al cursore o alla tabella.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitLSCursor</p> | <p>Indica che deve essere recuperato l'handle di contesto associato al cursore specificato.</p><p>Se non JET_bitLSCursor né JET_bitLSTable vengono specificati, JET_bitLSCursor viene presupposto.</p><p>Questa opzione non può essere usata con JET_bitLSTable. L'operazione avrà esito negativo JET_errInvalidgrbit se si tenta di eseguire questa operazione.</p> | 
| <p>JET_bitLSTable</p> | <p>Indica che deve essere recuperato l'handle di contesto associato alla tabella che contiene il cursore specificato. Non è valido usare questa opzione con JET_bitLSCursor. L'operazione avrà esito negativo JET_errInvalidgrbit se si tenta di eseguire questa operazione.</p> | 
| <p>JET_bitLSReset</p> | <p>Indica che l'handle di contesto per l'oggetto scelto deve essere reimpostato su JET_LSNil. Il valore corrente dell'handle di contesto viene restituito nel buffer di output.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Una delle opzioni richieste non è valida, usata in modo non valido o non è implementata.</p><p>Questa operazione può verificarsi <strong>per JetGetLS</strong> quando JET_bitLSCursor e JET_bitLSTable sono impostate.</p> | 
| <p>JET_errLSNotSet</p> | <p>Impossibile restituire l'handle di contesto perché nessun handle di contesto è attualmente associato all'oggetto richiesto.</p><p><strong>Nota  </strong> Questo errore non viene restituito se JET_bitLSReset specificato ma non è stato associato alcun handle di contesto all'oggetto richiesto.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, l'handle di contesto è stato recuperato correttamente dall'oggetto richiesto. Se JET_bitLSReset stato specificato, anche l'handle di contesto è stato rimosso correttamente dall'oggetto . Non verrà apportata alcuna modifica allo stato del database.

In caso di errore, non si è verificata alcuna modifica allo stato dell'oggetto richiesto. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetLS](./jetsetls-function.md)

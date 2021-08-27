---
description: Altre informazioni sulla funzione JetSetLS
title: Funzione JetSetLS
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c24a0d1cf45d370482b4890451569900aac946e3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465298"
---
# <a name="jetsetls-function"></a>Funzione JetSetLS


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetls-function"></a>Funzione JetSetLS

La **funzione JetSetLS** consente all'applicazione di associare un handle di contesto noto come Archiviazione locale a un cursore o alla tabella associata a tale cursore. Questo handle di contesto può essere usato dall'applicazione per archiviare i dati ausiliari associati a un cursore o a una tabella. L'applicazione viene successivamente notificata usando un callback di runtime quando l'handle di contesto deve essere rilasciato. In questo modo è possibile associare lo stato allocato dinamicamente a un cursore o a una tabella.

**Windows XP:****JetSetLS** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*ls*

Handle di contesto da associare al cursore o alla tabella.

Quando JET_bitLSReset viene specificato, il valore effettivo di questo parametro viene ignorato e viene JET_LSNil usato.

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitLSCursor</p> | <p>Questa opzione indica che l'handle di contesto deve essere associato al cursore specificato.</p><p>Se non JET_bitLSCursor né JET_bitLSTable specificato, JET_bitLSCursor si presuppone.</p><p>Non è valido usare questa opzione con JET_bitLSTable. L'operazione avrà esito negativo JET_errInvalidgrbit se viene tentata.</p> | 
| <p>JET_bitLSReset</p> | <p>Questa opzione indica che l'handle di contesto specificato deve essere ignorato e che l'handle di contesto per l'oggetto scelto deve essere reimpostato JET_LSNil.</p><p>È importante notare che questa azione non comporta un callback per pulire il valore precedente dell'handle di contesto per l'oggetto scelto. È possibile eseguire la pulizia corretta dell'handle di contesto precedente <a href="gg269234(v=exchg.10).md">usando JetGetLS</a> con JET_bitLSReset. Per <a href="gg269234(v=exchg.10).md">altre informazioni, vedere JetGetLS.</a></p> | 
| <p>JET_bitLSTable</p> | <p>Questa opzione indica che l'handle di contesto deve essere associato alla tabella associata al cursore specificato.</p><p>Non è valido usare questa opzione con JET_bitLSCursor. L'operazione avrà esito negativo JET_errInvalidgrbit se viene tentata.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInvalidgrbit</p> | <p>Una delle opzioni richieste non è valida, è stata usata in modo non corretto o non è stata implementata. Questo problema può verificarsi <strong>per JetSetLS</strong> quando JET_bitLSCursor e JET_bitLSTable sono entrambi specificati.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errLSAlreadySet</p> | <p>Impossibile associare l'handle di contesto specificato all'oggetto richiesto perché a esso era già associato un handle di contesto.</p> | 
| <p>JET_errLSCallbackNotSpecified</p> | <p>Impossibile associare l'handle di contesto specificato all'oggetto richiesto perché il callback di runtime non è stato configurato per l'istanza associata alla sessione.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, l'handle di contesto specificato è stato associato correttamente all'oggetto richiesto. Non verrà apportata alcuna modifica allo stato del database.

In caso di errore, non è stata apportata alcuna modifica allo stato dell'oggetto richiesto. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

L'Archiviazione locale per un cursore o una tabella deve essere visualizzato come cache volatile. L'applicazione deve prima provare a recuperare l'handle di contesto usando [JetGetLS.](./jetgetls-function.md) Se il valore non è impostato,ovvero è JET_LSNil), l'applicazione deve creare un nuovo contesto e caricarlo nella cache usando **JetSetLS**. L'applicazione può ripulire la cache usando una chiamata a [JetGetLS](./jetgetls-function.md) con JET_bitLSReset. Se il motore di database elimina la cache, verrà generato un callback di runtime per offrire all'applicazione la possibilità di pulire il contesto. Il tipo di callback verrà JET_cbtypFreeCursorLS handle di contesto associato a un cursore e JET_cbtypFreeTableLS per un handle di contesto associato a una tabella. In entrambi i casi, l'handle di contesto verrà passato come pvArg1. Vedere [JET_CALLBACK](./jet-callback-callback-function.md) per altre informazioni.

Il callback di runtime deve essere configurato correttamente per l'istanza associata alla sessione specificata prima di Archiviazione possibile usare localmente. Questo callback può essere impostato usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramRuntimeCallback](./callback-parameters.md). Per altre informazioni, vedere [JetSetSystemParameter](./jetsetsystemparameter-function.md) [e JET_paramRuntimeCallback](./callback-parameters.md) parametri di sistema.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLS](./jetgetls-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)

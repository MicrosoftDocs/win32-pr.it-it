---
description: Altre informazioni sulla funzione JetEndSession
title: Funzione JetEndSession
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b96ae49ef907cea158d1496339a740e1026ffea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472567"
---
# <a name="jetendsession-function"></a>Funzione JetEndSession


_**Si applica a:** Windows | Windows Server_

## <a name="jetendsession-function"></a>Funzione JetEndSession

La **funzione JetEndSession** termina la sessione e pulisce e dealloca tutte le risorse associate alla sessione specificata.

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da terminare. Le risorse associate vengono rilasciate al termine della sessione.

*grbit*

Riservato. Questo parametro può contenere il flag JET_bitForceSessionClosed, ma questo flag è riservato e l'impostazione non ha alcun effetto.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto.</p> | 
| <p>JET_errInvalidSesid</p> | <p>La sessione non è una sessione JET valida.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L'operazione non è riuscita perché non è stato possibile allocare memoria.</p> | 
| <p>JET_errSessionInUse</p> | <p>Ciò significa che la sessione era in uso in un altro thread o che la sessione non è stata impostata o reimpostata correttamente.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errOutOfBuffers</p> | <p>Errore di sistema che indica che non sono presenti altri buffer.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, l'handle di sessione viene chiuso e non disponibile e tutte le risorse correlate a questa sessione vengono pulite.

In caso di errore, potrebbero verificarsi diversi errori aggiuntivi durante la chiusura della tabella di ordinamento, la chiusura del cursore e il rollback delle transazioni. Questi errori sono piuttosto improbabile ed estremamente improbabile se le sessioni non sono completamente in uso quando **viene chiamato JetEndSession.** Questi errori verranno restituiti se non è stato possibile pulire correttamente una parte della sessione.

#### <a name="remarks"></a>Commenti

Questa API consente di eseguire il rollback di tutte le transazioni aperte (di cui non è stato eseguito il commit al livello 0). Verranno inoltre puliti tutti i cursori associati a questa sessione e tutte le tabelle di ordinamento create o aperte.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)

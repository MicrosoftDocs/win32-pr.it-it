---
description: 'Altre informazioni su: Funzione JetDupSession'
title: Funzione JetDupSession
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c22be08630c446f6c5ba106b38be6bc24415325
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466628"
---
# <a name="jetdupsession-function"></a>Funzione JetDupSession


_**Si applica a:** Windows | Windows Server_

## <a name="jetdupsession-function"></a>Funzione JetDupSession

La **funzione JetDupSession** avvia una sessione e inizializza e restituisce un handle di sessione ESE ([JET_SESID](./jet-sesid.md)). Le sessioni controllano tutti gli accessi al database e vengono usate per controllare l'ambito delle transazioni. La sessione può essere usata per avviare, eseguire il commit o interrompere le transazioni. La sessione viene usata anche per collegare, creare o aprire un database. La sessione viene usata come contesto per tutte le operazioni DDL e DML. Per aumentare la concorrenza e l'accesso parallelo al database, è possibile iniziare più sessioni.

**Nota:** Questa API agirà in tutti i modi come [una sessione JetBeginSession](./jetbeginsession-function.md) chiamata sull'istanza della sessione passata. Questa funzione non è consigliata, [è preferibile utilizzare JetBeginSession.](./jetbeginsession-function.md)

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare come origine per la duplicazione o l'avvio della sessione.

*psesid*

Puntatore alla variabile inizializzata dall'handle di sessione al completamento della restituzione.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L'operazione non è riuscita perché non è stato possibile allocare memoria.</p> | 
| <p>JET_errOutOfSessions</p> | <p>Il numero di sessioni che il motore consentirà al client di avviare è limitato. Questo valore può essere modificato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con la <em>JET_paramMaxSessions</em> costante. Il numero predefinito di sessioni è 16. Vedere <a href="gg294139(v=exchg.10).md">Parametri di sistema</a> per informazioni dettagliate <em>JET_paramMaxSessions</em>.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, l'handle di sessione viene inizializzato e può essere usato per le operazioni di database.

In caso di errore, non sono disponibili sessioni o non è stato possibile inizializzare una nuova sessione.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)

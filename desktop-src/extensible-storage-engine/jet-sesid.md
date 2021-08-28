---
description: 'Altre informazioni su: JET_SESID'
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da7acc706017c0346e5a701144d60bcbbfd7cf40
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983794"
---
# <a name="jet_sesid"></a>JET_SESID


_**Si applica a:** Windows | Windows Server_

## <a name="jet_sesid"></a>JET_SESID

Il **JET_SESID** dati contiene un handle per la sessione da usare per una chiamata all'API JET.

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a>Tipi di dati

JET_SESID

È **possibile** usare [NULL o JET_sesidNil](./invalid-handle-constants.md) per indicare un handle di sessione non valido.

### <a name="remarks"></a>Commenti

Una sessione è il contesto della transazione del motore di database. Può essere usato per avviare, eseguire il commit o interrompere le transazioni che influiscono sulla visibilità e sulla durabilità delle modifiche apportate da questa o altre sessioni.

Una transazione può essere avviata [tramite JetBeginTransaction.](./jetbegintransaction-function.md) È possibile creare una sessione usando [JetBeginSession](./jetbeginsession-function.md). Il numero massimo di sessioni che è possibile creare in qualsiasi momento è controllato da [JET_paramMaxSessions](./resource-parameters.md), che può essere configurato tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Una sessione viene terminata in modo esplicito da una chiamata a [JetEndSession](./jetendsession-function.md) o in modo implicito da una chiamata a [JetTerm](./jetterm-function.md).

Ogni sessione può essere usata solo da un thread alla volta. Inoltre, il comportamento predefinito del motore è limitare l'uso di una sessione allo stesso thread dal momento in cui viene effettuata la prima chiamata a [JetBeginTransaction](./jetbegintransaction-function.md) fino al momento in cui viene effettuata la chiamata corrispondente a [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback.](./jetrollback-function.md) Questo comportamento può essere modificato per rimuovere questa seconda restrizione impostando un contesto di sessione personalizzato usando [JetSetSessionContext](./jetsetsessioncontext-function.md) [e JetResetSessionContext](./jetresetsessioncontext-function.md).

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_paramMaxSessions](./resource-parameters.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)

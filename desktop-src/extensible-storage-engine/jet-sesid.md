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
ms.openlocfilehash: 60920995e72fdc1f45dcc6c083be7bcc1a91b3fa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466408"
---
# <a name="jet_sesid"></a>JET_SESID


_**Si applica a:** Windows | Windows Server_

## <a name="jet_sesid"></a>JET_SESID

Il **JET_SESID** dati contiene un handle per la sessione da utilizzare per una chiamata all'API JET.

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a>Tipi di dati

JET_SESID

È **possibile** usare [NULL o JET_sesidNil](./invalid-handle-constants.md) per indicare un handle di sessione non valido.

### <a name="remarks"></a>Commenti

Una sessione è il contesto della transazione del motore di database. Può essere utilizzato per avviare, eseguire il commit o interrompere le transazioni che influiscono sulla visibilità e la durabilità delle modifiche apportate da questa o da altre sessioni.

È possibile iniziare una transazione [usando JetBeginTransaction.](./jetbegintransaction-function.md) È possibile creare una sessione usando [JetBeginSession.](./jetbeginsession-function.md) Il numero massimo di sessioni che è possibile creare contemporaneamente è controllato da [JET_paramMaxSessions](./resource-parameters.md), che può essere configurato tramite [JetSetSystemParameter.](./jetsetsystemparameter-function.md)

Una sessione viene terminata in modo esplicito da una chiamata a [JetEndSession](./jetendsession-function.md) o in modo implicito da una chiamata a [JetTerm.](./jetterm-function.md)

Ogni sessione può essere usata da un solo thread alla volta. Inoltre, il comportamento predefinito del motore è limitare l'uso di una sessione allo stesso thread dal momento in cui viene effettuata la prima chiamata a [JetBeginTransaction](./jetbegintransaction-function.md) fino al momento in cui viene effettuata la chiamata corrispondente a [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback.](./jetrollback-function.md) Questo comportamento può essere modificato per rimuovere questa seconda restrizione impostando un contesto di sessione personalizzato usando [JetSetSessionContext](./jetsetsessioncontext-function.md) [e JetResetSessionContext.](./jetresetsessioncontext-function.md)

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



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

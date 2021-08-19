---
title: Struttura Connections (NapEnforcementClient.h)
description: Contiene informazioni sull'elenco di connessioni gestite da un applicatore.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- Struttura delle connessioni Nap
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f91e2dc404ff50c7edc3ba80a3c772ac6be762c1fe49575d8503a783e83bbef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800148"
---
# <a name="connections-structure"></a>Struttura delle connessioni

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

La **struttura Connections** contiene informazioni sull'elenco di connessioni gestite da un applicatore.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a>Members

<dl> <dt>

**count**
</dt> <dd>

Numero di connessioni attive attualmente gestite da un'applicazione nell'intervallo compreso tra 0 (zero) [**e maxConnectionCountPerEnforcer**](nap-type-constants.md).

</dd> <dt>

**Connessioni**
</dt> <dd>

Puntatore COM a un elenco di [**interfacce INapEnforcementClientConnection**](inapenforcementclientconnection.md) che rappresentano le connessioni client.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> <dt>

[Strutture di Protezione accesso alla rete](nap-structures.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 






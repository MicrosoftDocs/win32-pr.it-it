---
title: Struttura Connections (NapEnforcementClient. h)
description: Contiene informazioni sull'elenco di connessioni gestite da un Enforcer.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- Struttura delle connessioni NAP
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
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964985"
---
# <a name="connections-structure"></a>Struttura Connections

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

La struttura **Connections** contiene informazioni sull'elenco di connessioni gestite da un Enforcer.

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

Il numero di connessioni attive attualmente gestite da un Enforcer compreso nell'intervallo 0 (zero) a [**maxConnectionCountPerEnforcer**](nap-type-constants.md).

</dd> <dt>

**connessioni**
</dt> <dd>

Puntatore COM a un elenco di interfacce [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) che rappresentano le connessioni client.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento NAP](nap-reference.md)
</dt> <dt>

[Strutture NAP](nap-structures.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 






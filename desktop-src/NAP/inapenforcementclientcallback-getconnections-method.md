---
title: Metodo GetConnection INapEnforcementClientCallback (NapEnforcementClient. h)
description: Viene chiamato da NapAgent e implementato dal client di imposizione per restituire un set di connessioni.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- Metodo GetConnection NAP
- Metodo GetConnection NAP, interfaccia INapEnforcementClientCallback
- Interfaccia NAP di INapEnforcementClientCallback, Metodo GetConnection
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acdc68dbc69cabe710414f3fa2501585f3e384e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874582"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a>Metodo INapEnforcementClientCallback:: GetConnection

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapEnforcementClientCallback:: GetConnection** viene chiamato da napagent e implementato dal client di imposizione per restituire un set di connessioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connessioni* \[ di out\]
</dt> <dd>

Puntatore al set corrente di [**connessioni**](connections-struct.md)gestite.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo di callback deve restituire uno dei codici di errore seguenti.



| Codice restituito                                                                                                | Descrizione                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Restituisce questo valore se l'operazione ha esito positivo.<br/>                                                                                                                                                              |
| <dl> <dt>**\_server RPC \_ non \_ disponibile**</dt> </dl> | Se si restituisce questo valore, l'imposizione viene rimossa dall'elenco associato-SHA e viene scaricata la voce della cache NapAgent corrispondente. L'SHA in errore può quindi reinizializzarsi con NapAgent.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 






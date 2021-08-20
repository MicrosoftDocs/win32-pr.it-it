---
title: Metodo GetConnections INapEnforcementClientCallback (NapEnforcementClient.h)
description: Viene chiamato da NapAgent e implementato dal client di imposizione per restituire un set di connessioni.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- Metodo GetConnections nap
- Metodo GetConnections NAP, interfaccia INapEnforcementClientCallback
- Interfaccia INapEnforcementClientCallback NAP, metodo GetConnections
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
ms.openlocfilehash: e4f6c6fdb4adc416cb25fa0e402c8fee2d8baf3270400f15a8de67966eff7a9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134030"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a>Metodo INapEnforcementClientCallback::GetConnections

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapEnforcementClientCallback::GetConnections** viene chiamato da NapAgent e implementato dal client di imposizione per restituire un set di connessioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connessioni* \[ Cambio\]
</dt> <dd>

Puntatore al set corrente di connessioni [**gestite.**](connections-struct.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo di callback deve restituire uno dei codici di errore seguenti.



| Codice restituito                                                                                                | Descrizione                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Restituisce questo valore se l'operazione ha avuto esito positivo.<br/>                                                                                                                                                              |
| <dl> <dt>**SERVER \_ RPC S NON \_ \_ DISPONIBILE**</dt> </dl> | Se si restituisce questo valore, l'applicatore viene rimosso dall'elenco bound-SHA e la voce della cache NapAgent corrispondente viene scaricata. L'SHA che ha esito negativo può quindi inizializzarsi nuovamente con NapAgent.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 






---
title: Metodo GetFlags INapEnforcementClientConnection (NapEnforcementClient.h)
description: Viene usato per distinguere le risposte per la prima volta dalle risposte a causa di SoHRequest memorizzate nella cache dagli imponitori. | Metodo GetFlags INapEnforcementClientConnection (NapEnforcementClient.h)
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- Metodo GetFlags nap
- Metodo GetFlags NAP , interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aea1815a8892f5d072f72d32d433070038b35cd663f10dfba08422a81153660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781051"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a>Metodo INapEnforcementClientConnection::GetFlags

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapEnforcementClientConnection::GetFlags** viene usato per distinguere le risposte per la prima volta dalle risposte a causa di SoHRequests memorizzate nella cache dagli imponitori.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ Cambio\]
</dt> <dd>

Puntatore a un flag che determina se [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) è dovuto a un oggetto **SoHRequest memorizzato nella** cache. Se *flags* ha valore [**freshSoHRequest**](nap-type-constants.md), si tratta di una nuova richiesta. in caso contrario, si tratta di una richiesta memorizzata nella cache.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 






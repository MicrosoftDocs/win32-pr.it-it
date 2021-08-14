---
title: Metodo INapSystemHealthAgentBinding NotifySoHChange (NapSystemHealthAgent.h)
description: Viene usato dagli sha quando il relativo soH cambia.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- Metodo NotifySoHChange NAP
- Metodo NotifySoHChange NAP, interfaccia INapSystemHealthAgentBinding
- Interfaccia INapSystemHealthAgentBinding NAP, metodo NotifySoHChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a418a78e0d21178f3dd1889816873afb1c7ec7212da48be5d75e44d40d0a61d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367839"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a>Metodo INapSystemHealthAgentBinding::NotifySoHChange

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentBinding::NotifySoHChange** viene usato dagli sha quando il relativo soH cambia.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                             | Descrizione                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione riuscita.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>         | Errore di autorizzazione, accesso negato.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/>                                                             |
| <dl> <dt>**PROTEZIONE \_ ACCESSO ALLA RETE E NON \_ \_ INIZIALIZZATA**</dt> </dl> | L'sha non è stato inizializzato in precedenza.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ DISCONNESSO**</dt> </dl>     | NapAgent è stato arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, dopo il riavvio.<br/> |



 

## <a name="remarks"></a>Commenti

Gli sha non devono chiamare questa API in modo speculativo perché comportano uno scambio SoH in transito. Le chiamate a questa API devono essere effettuate solo quando necessario.

NapAgent non contiene questo thread per elaborare la modifica soh. Restituisce invece immediatamente ed elabora la modifica in modo asincrono.

L'SHA deve [**chiamare Initialize**](inapsystemhealthagentbinding-initialize-method.md) prima di chiamare questo metodo o qualsiasi altro metodo dell'interfaccia [**INapSystemHealthAgentBinding2.**](inapsystemhealthagentbinding2.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 






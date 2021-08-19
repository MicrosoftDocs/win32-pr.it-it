---
title: Metodo INapSystemHealthAgentBinding2 GetSystemIsolationInfoEx (NapSystemHealthAgent.h)
description: Viene chiamato dagli amministratori del servizio per determinare lo stato di isolamento del sistema e lo stato di isolamento esteso.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- Metodo GetSystemIsolationInfoEx nap
- Metodo GetSystemIsolationInfoEx NAP, interfaccia INapSystemHealthAgentBinding2
- Metodo GetSystemIsolationInfoEx dell'interfaccia INapSystemHealthAgentBinding2 nap
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ac81d00bb953ddf3ab415e90724adcca34b302d8cc268699d8f2a820e0f34ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367829"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a>Metodo INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx** viene chiamato dagli sha per determinare lo stato di isolamento del sistema e lo stato di isolamento esteso.

> [!Note]  
> Usare [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) per determinare solo lo stato di isolamento del sistema.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isolationInfo* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a [**una struttura IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) che contiene lo stato di isolamento esteso del sistema per le connessioni note. *isolationInfo* indica se il sistema si trova in uno stato di accesso limitato, di prova o di accesso senza restrizioni, nonché di informazioni [**su ExtendedIsolationState.**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate)

</dd> <dt>

*unknownConnections* \[ Cambio\]
</dt> <dd>

Puntatore a un **oggetto BOOL** **che è TRUE** se le connessioni sono in uno stato sconosciuto e FALSE in caso **contrario.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                             | Descrizione                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione riuscita.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>         | Errore di autorizzazioni, accesso negato.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite risorse di sistema: impossibile eseguire l'operazione.<br/>                                                             |
| <dl> <dt>**PROTEZIONE \_ ACCESSO ALLA RETE NON \_ \_ INIZIALIZZATA**</dt> </dl> | L'SHA non è stato inizializzato in precedenza.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ DISCONNESSO**</dt> </dl>     | NapAgent è stato arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, dopo il riavvio.<br/> |



 

## <a name="remarks"></a>Commenti

L'SHA deve liberare [**la struttura IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chiamando [**FreeIsolationInfoEx**](freeisolationinfoex.md).

L'SHA deve chiamare [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) prima di chiamare questo metodo o qualsiasi altro metodo dell'interfaccia [**INapSystemHealthAgentBinding2.**](inapsystemhealthagentbinding2.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 






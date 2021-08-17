---
title: Metodo INapSystemHealthAgentRequest GetSoHRequest (NapSystemHealthAgent.h)
description: Può essere usato dagli SHAs per ottenere soh precedentemente memorizzati nella cache da NapAgent.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- Metodo GetSoHRequest nap
- Metodo GetSoHRequest NAP, interfaccia INapSystemHealthAgentRequest
- Interfaccia INapSystemHealthAgentRequest NAP, metodo GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c784ec520180f3524f49fa95644b03fa5f982651bd4c2322542dc46cc3f85a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133520"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a>Metodo INapSystemHealthAgentRequest::GetSoHRequest

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentRequest::GetSoHRequest** può essere usato dagli SHAs che ottengono SoHs memorizzati in precedenza nella cache da NapAgent.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohRequest* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a un [**oggetto SoHRequest.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                            | Descrizione                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione riuscita.<br/>                                        |
| <dl> <dt>**NAP \_ E \_ NO \_ CACHED \_ SOH**</dt> </dl> | Il file SoH non è stato trovato. NapAgent non dispone di una copia memorizzata nella cache.<br/> |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>        | Errore di autorizzazioni, accesso negato.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 






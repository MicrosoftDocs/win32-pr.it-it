---
title: Metodo INapSystemHealthAgentRequest GetCorrelationId (NapSystemHealthAgent.h)
description: Viene usato dagli agenti di integrità del sistema per correlare SoH e SoH-Responses.
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- Metodo GetCorrelationId NAP
- Metodo GetCorrelationId NAP, interfaccia INapSystemHealthAgentRequest
- Metodo GetCorrelationId dell'interfaccia INapSystemHealthAgentRequest NAP
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf02a6d72aaa2744cc5a1329d791bdb9e8fa31f7453b131268245e120d7087e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686161"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a>Metodo INapSystemHealthAgentRequest::GetCorrelationId

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentRequest::GetCorrelationId** viene usato dagli agenti di integrità del sistema per correlare SoH e SoH-Responses.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*correlationId* \[ Cambio\]
</dt> <dd>

Puntatore a un [**CorrelationId univoco**](/windows/win32/api/naptypes/ns-naptypes-correlationid) per lo scambio SoH.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 






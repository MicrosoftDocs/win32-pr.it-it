---
title: Metodo INapSystemHealthValidationRequest GetStringCorrelationId (NapSystemHealthValidator.h)
description: Viene usato dai validator dell'integrità del sistema che devono registrare queste informazioni.
ms.assetid: c3e45857-463b-4048-a178-ec26a318b63b
keywords:
- Metodo GetStringCorrelationId nap
- Metodo GetStringCorrelationId NAP, interfaccia INapSystemHealthValidationRequest
- Metodo GetStringCorrelationId dell'interfaccia INapSystemHealthValidationRequest nap
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetStringCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5818ebd219dd38633da92a269e63d5641f393371cfa67b6910844523c37929ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939362"
---
# <a name="inapsystemhealthvalidationrequestgetstringcorrelationid-method"></a>Metodo INapSystemHealthValidationRequest::GetStringCorrelationId

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthValidationRequest::GetStringCorrelationId** viene usato dai validator dell'integrità del sistema che devono registrare queste informazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*correlationId* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a un [**stringCorrelationId univoco**](nap-type-constants.md) per lo scambio SoH.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 






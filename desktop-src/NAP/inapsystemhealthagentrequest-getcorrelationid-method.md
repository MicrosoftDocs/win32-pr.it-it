---
title: Metodo INapSystemHealthAgentRequest GetCorrelationId (NapSystemHealthAgent. h)
description: Viene usato dagli agenti di integrità del sistema per correlare le risposte SOH e SoH.
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- NAP metodo GetCorrelationId
- Metodo GetCorrelationId NAP, interfaccia INapSystemHealthAgentRequest
- Interfaccia INapSystemHealthAgentRequest NAP, metodo GetCorrelationId
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
ms.openlocfilehash: 7af5b182df738ec22c75f2afffd1adb3591007be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519270"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a>Metodo INapSystemHealthAgentRequest:: GetCorrelationId

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentRequest:: GetCorrelationId** viene usato dagli agenti di integrità del sistema per correlare le risposte SoH e SOH.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

ID correlazione  \[ out\]
</dt> <dd>

Puntatore a un [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) univoco per lo scambio di rapporto di integrità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 






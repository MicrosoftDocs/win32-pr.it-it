---
title: Metodo INapSystemHealthAgentRequest SetSoHRequest (NapSystemHealthAgent. h)
description: Viene usato dagli agenti di integrità per scrivere la richiesta di rapporto di integrità risultante dalla chiamata a INapSystemHealthAgentCallback GetSoHRequest.
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- NAP metodo SetSoHRequest
- Metodo SetSoHRequest NAP, interfaccia INapSystemHealthAgentRequest
- Interfaccia INapSystemHealthAgentRequest NAP, metodo SetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0fd1dcccad2a402d8455bcdf4f66052d41160b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301363"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a>Metodo INapSystemHealthAgentRequest:: SetSoHRequest

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentRequest:: SetSoHRequest** viene usato dagli agenti di integrità per scrivere la richiesta di rapporto di integrità risultante dalla chiamata a [**INapSystemHealthAgentCallback:: GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohRequest* \[ in\]
</dt> <dd>

Puntatore a un pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*cacheSohForLaterUse* \[ in\]
</dt> <dd>

**Bool** che è **true** se il napagent deve memorizzare nella cache il rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** in caso contrario.

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

 

 






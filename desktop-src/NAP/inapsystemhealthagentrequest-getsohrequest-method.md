---
title: Metodo INapSystemHealthAgentRequest GetSoHRequest (NapSystemHealthAgent. h)
description: Può essere usato da SHAs Get invieranno precedentemente memorizzato nella cache da NapAgent.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- NAP metodo GetSoHRequest
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
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048690"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a>Metodo INapSystemHealthAgentRequest:: GetSoHRequest

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentRequest:: GetSoHRequest** può essere usato da Shas Get invieranno precedentemente memorizzato nella cache da napagent.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohRequest* \[ out\]
</dt> <dd>

Puntatore a un puntatore a un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                            | Descrizione                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione riuscita.<br/>                                        |
| <dl> <dt>**NAP \_ E \_ nessun rapporto di \_ integrità memorizzato nella cache \_**</dt> </dl> | Il rapporto di integrità non è stato trovato. NapAgent non dispone di una copia memorizzata nella cache.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Errore delle autorizzazioni, accesso negato.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/>     |



 

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

 

 






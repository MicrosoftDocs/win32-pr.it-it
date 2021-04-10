---
title: Metodo INapSystemHealthAgentCallback GetFixupInfo (NapSystemHealthAgent. h)
description: Viene chiamato da NapAgent per determinare lo stato dell'agente integrità sistema durante l'elaborazione di un SoHResponse.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- NAP metodo GetFixupInfo
- Metodo GetFixupInfo NAP, interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback NAP, metodo GetFixupInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227cbe870c722189c995bff0c967eb187548cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120078"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a>Metodo INapSystemHealthAgentCallback:: GetFixupInfo

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentCallback:: GetFixupInfo** viene chiamato da napagent per determinare lo stato dell'agente integrità sistema durante l'elaborazione di un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*informazioni* \[ su out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) che contiene lo stato di correzione dell'agente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                          | Descrizione                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Indica l'esito positivo dell'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo di callback viene dichiarato dal sistema NAP e deve essere implementato dal writer SHA.

L'agente integrità sistema deve restituire immediatamente **S \_ OK** senza bloccarsi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 






---
title: Metodo INapSystemHealthAgentCallback GetFixupInfo (NapSystemHealthAgent.h)
description: Viene chiamato da NapAgent per determinare lo stato dell'agente di integrità del sistema, durante l'elaborazione di soHResponse.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- Metodo GetFixupInfo nap
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
ms.openlocfilehash: 9d82f84acbc759f8459c7eeb904ab4f08a108093fa30c3b27c033fbfef1dcf15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037751"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a>Metodo INapSystemHealthAgentCallback::GetFixupInfo

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentCallback::GetFixupInfo** viene chiamato da NapAgent per determinare lo stato dell'agente di integrità del sistema, durante l'elaborazione di [**un oggetto SoHResponse.**](/windows/win32/api/naptypes/ns-naptypes-soh)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*info* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a [**una struttura FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) che contiene lo stato di correzione dell'agente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                          | Descrizione                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Indica l'esito positivo dell'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo di callback viene dichiarato dal sistema di Protezione accesso alla rete e deve essere implementato dal writer SHA.

L'agente di integrità del sistema deve restituire **immediatamente S \_ OK** senza bloccarsi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 






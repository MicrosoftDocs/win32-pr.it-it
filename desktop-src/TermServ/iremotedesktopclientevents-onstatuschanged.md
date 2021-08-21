---
title: Metodo OnStatusChanged IRemoteDesktopClientEvents (Locationapi.h)
description: Chiamato quando il controllo client ha aggiornato lo stato.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- Metodo OnStatusChanged Servizi Desktop remoto
- Metodo OnStatusChanged Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto , metodo OnStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d08b15eb2b8112afcef6c98a841a249672df2ae3fbb7f36ceea513d53a5b0478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351623"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a>Metodo IRemoteDesktopClientEvents::OnStatusChanged

Chiamato quando il controllo client ha aggiornato lo stato.

## <a name="syntax"></a>Sintassi


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*statusCode* 
</dt> <dd>

Nuovo codice di stato.

</dd> <dt>

*statusMessage* 
</dt> <dd>

Testo del messaggio di stato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                           |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>Locationapi.h</dt> </dl>       |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 






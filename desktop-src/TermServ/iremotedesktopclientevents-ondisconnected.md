---
title: Metodo disconnected IRemoteDesktopClientEvents
description: Chiamato quando il controllo client è stato disconnesso da una sessione remota.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- Metodo disconnected Servizi Desktop remoto
- Metodo disconnected Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, metodo disconnected
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742383"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a>Metodo IRemoteDesktopClientEvents:: disconnected

Chiamato quando il controllo client è stato disconnesso da una sessione remota.

## <a name="syntax"></a>Sintassi


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*disconnectReason* \[ in\]
</dt> <dd>

Motivo dell'evento di disconnessione.

</dd> <dt>

*ExtendedDisconnectReason* \[ in\]
</dt> <dd>

Informazioni estese per l'evento di disconnessione.

</dd> <dt>

*disconnectErrorMessage* \[ in\]
</dt> <dd>

Messaggio di errore per l'evento di disconnessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                           |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                 |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 






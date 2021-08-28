---
title: Metodo OnDisconnected IRemoteDesktopClientEvents
description: Chiamato quando il controllo client è stato disconnesso da una sessione remota.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- Metodo OnDisconnected Servizi Desktop remoto
- Metodo OnDisconnected Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto , metodo OnDisconnected
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
ms.openlocfilehash: 5e93ebf7c85e4015539cbbcc15723cdfed9c7d181741925c1a97c93ccc4326eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124901"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a>Metodo IRemoteDesktopClientEvents::OnDisconnected

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

*disconnectReason* \[ Pollici\]
</dt> <dd>

Motivo dell'evento di disconnessione.

</dd> <dt>

*ExtendedDisconnectReason* \[ Pollici\]
</dt> <dd>

Informazioni estese per l'evento di disconnessione.

</dd> <dt>

*disconnectErrorMessage* \[ Pollici\]
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

 

 






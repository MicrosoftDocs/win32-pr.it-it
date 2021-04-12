---
title: Metodo IRemoteDesktopClientEvents OnAutoReconnecting
description: Chiamato quando il controllo client tenta di ristabilire automaticamente una connessione a una sessione remota.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnAutoReconnecting
- Metodo OnAutoReconnecting Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, metodo OnAutoReconnecting
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74c37919384727fdf51aad004349478798a3ffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519006"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a>Metodo IRemoteDesktopClientEvents:: OnAutoReconnecting

Chiamato quando il controllo client tenta di ristabilire automaticamente una connessione a una sessione remota.

## <a name="syntax"></a>Sintassi


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
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

</dd> <dt>

*NetworkAvailable* \[ in\]
</dt> <dd>

Indica se la rete è disponibile.

</dd> <dt>

*attemptCount* \[ in\]
</dt> <dd>

Il tentativo è.

</dd> <dt>

*maxAttemptCount* \[ in\]
</dt> <dd>

Verrà eseguito il numero massimo di tentativi di riconnessione.

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

 

 






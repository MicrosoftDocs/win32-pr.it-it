---
title: Metodo IRemoteDesktopClientEvents OnNetworkStatusChanged
description: Chiamato quando lo stato della rete viene modificato. | Metodo IRemoteDesktopClientEvents OnNetworkStatusChanged
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- Metodo OnNetworkStatusChanged Servizi Desktop remoto
- Metodo OnNetworkStatusChanged Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto metodo , OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d14519f5da78a0d42b5bd7e52abf790c21406bfe20848235d2639beed2e215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515111"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a>Metodo IRemoteDesktopClientEvents::OnNetworkStatusChanged

Chiamato quando lo stato della rete viene modificato.

## <a name="syntax"></a>Sintassi


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*qualityLevel* \[ Pollici\]
</dt> <dd>

Nuovo livello di qualità della connessione. Il livello di qualità è determinato dai valori della larghezza di banda e del tempo di round trip (rtt).

Uno dei valori seguenti.



| Valore                                                                        | Significato                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Non è stato possibile determinare il livello di qualità.<br/>       |
| <dl> <dt>1</dt> </dl> | La qualità della connessione è scadente (una barra).<br/>        |
| <dl> <dt>2</dt> </dl> | La qualità della connessione è equa (due barre).<br/>       |
| <dl> <dt>3</dt> </dl> | La qualità della connessione è buona (tre barre).<br/>     |
| <dl> <dt>4</dt> </dl> | La qualità della connessione è eccellente (quattro barre).<br/> |



 

</dd> <dt>

*larghezza di banda* \[ Pollici\]
</dt> <dd>

Specifica la nuova larghezza di banda della connessione, in kilobit al secondo (Kbps).

</dd> <dt>

*rtt* \[ Pollici\]
</dt> <dd>

Specifica il nuovo tempo di roundtrip della connessione (latenza), espresso in millisecondi.

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

 

 






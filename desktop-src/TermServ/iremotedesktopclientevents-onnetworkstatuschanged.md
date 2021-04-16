---
title: Metodo IRemoteDesktopClientEvents OnNetworkStatusChanged
description: Chiamato quando lo stato della rete è stato modificato. | Metodo IRemoteDesktopClientEvents OnNetworkStatusChanged
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnNetworkStatusChanged
- Metodo OnNetworkStatusChanged Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, metodo OnNetworkStatusChanged
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
ms.openlocfilehash: de64d8b16ea9acf9defc976d4baa91afd64f8fa7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530661"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a>Metodo IRemoteDesktopClientEvents:: OnNetworkStatusChanged

Chiamato quando lo stato della rete è stato modificato.

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

*qualityLevel* \[ in\]
</dt> <dd>

Nuovo livello di qualità della connessione. Il livello di qualità è determinato dai valori della larghezza di banda e del tempo di round trip (RTT).

Uno dei valori seguenti.



| Valore                                                                        | Significato                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Non è stato possibile determinare il livello di qualità.<br/>       |
| <dl> <dt>1</dt> </dl> | La qualità della connessione è scadente (una barra).<br/>        |
| <dl> <dt>2</dt> </dl> | La qualità della connessione è equa (due barre).<br/>       |
| <dl> <dt>3</dt> </dl> | La qualità della connessione è corretta (tre barre).<br/>     |
| <dl> <dt>4</dt> </dl> | La qualità della connessione è eccellente (quattro barre).<br/> |



 

</dd> <dt>

*larghezza di banda* \[ in\]
</dt> <dd>

Specifica la nuova larghezza di banda della connessione, in kilobit al secondo (Kbps).

</dd> <dt>

*RTT* \[ in\]
</dt> <dd>

Specifica il nuovo tempo di round trip della connessione (latenza), in millisecondi.

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

 

 






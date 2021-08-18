---
title: Metodo IMsTscAxEvents OnRemoteProgramDisplayed
description: Chiamato quando viene visualizzato un programma RemoteApp.
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- Metodo OnRemoteProgramDisplayed Servizi Desktop remoto
- Metodo OnRemoteProgramDisplayed Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto metodo , OnRemoteProgramDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df50f9a536b367b203f395d9c856562b8967d8a5830704a2e9bbb4c69152f202
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058819"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a>Metodo IMsTscAxEvents::OnRemoteProgramDisplayed

Chiamato quando viene visualizzato un programma RemoteApp.

## <a name="syntax"></a>Sintassi


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vbDisplayed* \[ Pollici\]
</dt> <dd>

Indica se il programma RemoteApp è visualizzato o nascosto.

</dd> <dt>

*uDisplayInformation* \[ Pollici\]
</dt> <dd>

Informazioni visualizzate.

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**RAIL \_ APPDISPLAY \_ AUTORECONNECT**


</dt> <dd>

È in corso la riconnessione automatica.

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**RAIL \_ APPDISPLAY \_ DESKTOPHOOKED**


</dt> <dd>

Il conteggio di RemoteApp è appena passato a zero.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Implementare questo metodo nel sink di evento per ricevere la notifica che è stata visualizzata una remoteapp.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



 

 






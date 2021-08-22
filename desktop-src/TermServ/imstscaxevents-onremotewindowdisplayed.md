---
title: Metodo IMsTscAxEvents OnRemoteWindowDisplayed
description: Chiamato quando viene visualizzata una finestra di RemoteApp.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Metodo OnRemoteWindowDisplayed Servizi Desktop remoto
- Metodo OnRemoteWindowDisplayed Servizi Desktop remoto , interfaccia IMsTscAxEvents
- Metodo OnRemoteWindowDisplayed dell'Servizi Desktop remoto IMsTscAxEvents
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6985a71fe6351a81b2daef69401dfd5c65543e9984fd64c28a120704a34d5a8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512111"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a>Metodo IMsTscAxEvents::OnRemoteWindowDisplayed

Chiamato quando viene visualizzata una finestra di RemoteApp.

## <a name="syntax"></a>Sintassi


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vbDisplayed* \[ Pollici\]
</dt> <dd>

Tipo: **VARIANT \_ BOOL**

Indica se la finestra RemoteApp è visualizzata o nascosta.

</dd> <dt>

*hwnd* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

Handle della finestra visualizzata.

</dd> <dt>

*windowAttribute* \[ Pollici\]
</dt> <dd>

Tipo: **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**

Valore [**dell'enumerazione RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) che specifica altre informazioni sull'evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 






---
title: Metodo IMsTscAxEvents OnRemoteWindowDisplayed
description: Chiamato quando viene visualizzata una finestra di RemoteApp.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnRemoteWindowDisplayed
- Metodo OnRemoteWindowDisplayed Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnRemoteWindowDisplayed
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
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400735"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a>Metodo IMsTscAxEvents:: OnRemoteWindowDisplayed

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

*vbDisplayed* \[ in\]
</dt> <dd>

Tipo: **Variant \_ bool**

Indica se la finestra RemoteApp è visualizzata o nascosta.

</dd> <dt>

*HWND* \[ in\]
</dt> <dd>

Tipo: **HWND**

Handle della finestra visualizzata.

</dd> <dt>

*windowAttribute* \[ in\]
</dt> <dd>

Tipo: **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**

Valore dell'enumerazione [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) che specifica ulteriori informazioni sull'evento.

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

 

 






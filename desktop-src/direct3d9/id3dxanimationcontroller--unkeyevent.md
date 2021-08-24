---
description: Rimuove un evento specificato da una traccia di animazione, impedendo l'esecuzione dell'evento.
ms.assetid: 658ffe91-44ba-4bde-b78c-c545dff27ab1
title: Metodo ID3DXAnimationController::UnkeyEvent (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2565091213108c6dcc563d23df9cad50faed6b30d46af08cadfacb4fc60d3989
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564151"
---
# <a name="id3dxanimationcontrollerunkeyevent-method"></a>Metodo ID3DXAnimationController::UnkeyEvent

Rimuove un evento specificato da una traccia di animazione, impedendo l'esecuzione dell'evento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnkeyEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hEvent* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per l'evento da rimuovere dalla traccia di animazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 





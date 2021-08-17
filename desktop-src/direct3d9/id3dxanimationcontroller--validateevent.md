---
description: Controlla se un handle di evento specificato è valido e se l'evento di animazione non è ancora stato completato.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: Metodo ID3DXAnimationController::ValidateEvent (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 24c5195d38aeaebefd1713df31f23b6b2ec7b2324a31381027f3442b541678c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094178"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a>Metodo ID3DXAnimationController::ValidateEvent

Controlla se un handle di evento specificato è valido e se l'evento di animazione non è ancora stato completato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hEvent* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per un evento di animazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce S \_ OK se l'handle dell'evento è valido e l'evento non è ancora stato completato.

Restituisce E \_ FAIL se l'handle dell'evento non è valido e/o se l'evento è stato completato.

## <a name="remarks"></a>Commenti

Il metodo indicherà che un handle di evento è valido anche se l'evento è in esecuzione ma non è ancora stato completato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 





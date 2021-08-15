---
description: Ottiene una descrizione di un evento di animazione specificato.
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: Metodo ID3DXAnimationController::GetEventDesc (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bc113788a8eb6b64accfcba8c58dd3a3512e17601ec02ce5dd33349628c69212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987941"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a>Metodo ID3DXAnimationController::GetEventDesc

Ottiene una descrizione di un evento di animazione specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hEvent* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Handle di evento per un evento di animazione da descrivere.

</dd> <dt>

*pDesc* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXEVENT \_ DESC**](d3dxevent-desc.md)**

Puntatore a una [**struttura \_ DESC D3DXEVENT**](d3dxevent-desc.md) che contiene una descrizione dell'evento di animazione.

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

 

 





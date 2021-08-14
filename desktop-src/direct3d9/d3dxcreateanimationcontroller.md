---
description: Crea un oggetto controller di animazione.
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: Funzione D3DXCreateAnimationController (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateAnimationController
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0edda07aa5ae443a268bd5df50a154aa2a7f2ec9ca1873dc486e8e46532ae468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526636"
---
# <a name="d3dxcreateanimationcontroller-function"></a>Funzione D3DXCreateAnimationController

Crea un oggetto controller di animazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateAnimationController(
  _In_  UINT                      MaxNumAnimationOutputs,
  _In_  UINT                      MaxNumAnimationSets,
  _In_  UINT                      MaxNumTracks,
  _In_  UINT                      MaxNumEvents,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MaxNumAnimationOutputs* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero massimo di output di animazione che il controller può supportare.

</dd> <dt>

*MaxNumAnimationSets* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero massimo di set di animazione che possono essere misti.

</dd> <dt>

*MaxNumTracks* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero massimo di set di animazioni che possono essere misti contemporaneamente.

</dd> <dt>

*MaxNumEvents* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero massimo di eventi in sospeso che il controller supporterà.

</dd> <dt>

*ppAnimController* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Puntatore all'oggetto controller di animazione creato. Vedere [**ID3DXAnimationController.**](id3dxanimationcontroller.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Un controller di animazione controlla un mixer di animazione. Il controller aggiunge metodi per modificare i parametri di fusione nel tempo per abilitare transizioni uniformi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di animazione](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 

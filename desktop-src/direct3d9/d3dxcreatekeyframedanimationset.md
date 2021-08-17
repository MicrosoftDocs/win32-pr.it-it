---
description: Crea un'interfaccia del set di animazioni con fotogrammi chiave ID3DXKeyframedAnimationSet.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: Funzione D3DXCreateKeyframedAnimationSet (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c4fbfb31b712e1521930fa468bae315a443105f3a6bc0863fe3267f9586f874a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804567"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a>Funzione D3DXCreateKeyframedAnimationSet

Crea un'interfaccia del set di animazioni con fotogrammi chiave [**ID3DXKeyframedAnimationSet.**](id3dxkeyframedanimationset.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome del set di animazioni.

</dd> <dt>

*TicksPerSecond* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Numero di tick dei fotogrammi chiave che sono trascorsi al secondo.

</dd> <dt>

*Riproduzione* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXPLAYBACK \_ TYPE**](./d3dxplayback-type.md)**

Tipo del ciclo di riproduzione del set di animazioni. Vedere [**D3DXPLAYBACK \_ TYPE**](./d3dxplayback-type.md).

</dd> <dt>

*NumAnimations* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di set di animazione di ridimensionamento, rotazione e traslazione (SRT).

</dd> <dt>

*NumCallbackKeys* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di chiavi di callback.

</dd> <dt>

*pCallKeys* \[ Pollici\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ CALLBACK**](d3dxkey-callback.md) \***

Puntatore a una [**struttura CALLBACK D3DXKEY \_**](d3dxkey-callback.md) che archivia i dati di callback dell'utente.

</dd> <dt>

*ppAnimationSet* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***

Indirizzo di un puntatore all'interfaccia del set di animazioni con fotogrammi chiave [**ID3DXKeyframedAnimationSet.**](id3dxkeyframedanimationset.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è S \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di animazione](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 

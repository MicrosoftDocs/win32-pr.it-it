---
description: Ottiene un numero intero.
ms.assetid: 8074758a-f650-4698-8a75-aa0ffb14cb21
title: Metodo ID3DXBaseEffect::GetInt (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetInt
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6ccd892a7563d4fce300f177a63f5e0cb82601e711f7046e9b9475977409926b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296767"
---
# <a name="id3dxbaseeffectgetint-method"></a>Metodo ID3DXBaseEffect::GetInt

Ottiene un numero intero.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetInt(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [Handle (Direct3D 9).](handles.md)

</dd> <dt>

*pn* \[ Cambio\]
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)\***

Restituisce un numero intero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetInt**](id3dxbaseeffect--setint.md)
</dt> </dl>

 

 

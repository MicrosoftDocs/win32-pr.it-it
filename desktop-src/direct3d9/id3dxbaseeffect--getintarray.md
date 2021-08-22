---
description: Ottiene una matrice di numeri interi.
ms.assetid: c02b5343-db4f-4e8c-989c-6aba8c19c234
title: Metodo ID3DXBaseEffect::GetIntArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7f9f360c51007d7bc51fe39dfeeb13a2c0a5f4de0b3da1582075c865a3ff1e21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279001"
---
# <a name="id3dxbaseeffectgetintarray-method"></a>Metodo ID3DXBaseEffect::GetIntArray

Ottiene una matrice di numeri interi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIntArray(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn,
  [in]  UINT       Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [Handle (Direct3D 9)](handles.md).

</dd> <dt>

*pn* \[ Cambio\]
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)\***

Restituisce una matrice di numeri interi.

</dd> <dt>

*Conteggio* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di numeri interi nella matrice.

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

[**SetIntArray**](id3dxbaseeffect--setintarray.md)
</dt> </dl>

 

 

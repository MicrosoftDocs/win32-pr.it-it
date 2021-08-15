---
description: Ottiene un vettore.
ms.assetid: 55f5512f-42f2-4588-abd4-1cdea530b9bf
title: Metodo ID3DXBaseEffect::GetVector (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e72c02ed1bc8f29ed8809a7a4733914860a6c9c058795f8a02661f29b9607f69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119459961"
---
# <a name="id3dxbaseeffectgetvector-method"></a>Metodo ID3DXBaseEffect::GetVector

Ottiene un vettore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVector(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [Handle (Direct3D 9).](handles.md)

</dd> <dt>

*pVector* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Restituisce un vettore 4D.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Se il vettore di destinazione è più grande del vettore di origine, verranno riempiti solo i componenti iniziali del vettore di destinazione e i componenti rimanenti verranno impostati su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetVector**](id3dxbaseeffect--setvector.md)
</dt> </dl>

 

 





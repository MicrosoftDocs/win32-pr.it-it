---
description: Imposta una matrice di vettori 4D.
ms.assetid: 45bc5cb1-b44a-468b-8c80-a639da8a033f
title: 'Metodo ID3DXTextureShader:: SetVectorArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c91a012cda9d1aa992682b5cb5aa769bf41de180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322546"
---
# <a name="id3dxtextureshadersetvectorarray-method"></a>Metodo ID3DXTextureShader:: SetVectorArray

Imposta una matrice di vettori 4D.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConstant* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco della matrice di costanti vettoriali. Vedere [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pVector* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Matrice di vettori 4D. Vedere [**D3DXVECTOR4**](d3dxvector4.md).

</dd> <dt>

*Numero* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di vettori nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 

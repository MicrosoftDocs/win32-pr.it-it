---
description: 'Metodo ID3DXTextureShader::SetFloatArray: imposta una matrice di numeri a virgola mobile.'
ms.assetid: 8e64b569-a6bf-4925-9d21-4df0b6661ee2
title: Metodo ID3DXTextureShader::SetFloatArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd42455e16cbfc203f76de868a82935e0e25401f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090249"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a>Metodo ID3DXTextureShader::SetFloatArray

Imposta una matrice di numeri a virgola mobile.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConstant* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco della matrice di costanti. Vedere [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pf* \[ Pollici\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Matrice di numeri a virgola mobile.

</dd> <dt>

*Conteggio* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di valori a virgola mobile nella matrice.

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

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 

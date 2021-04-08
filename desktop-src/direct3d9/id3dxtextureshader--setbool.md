---
description: Imposta un valore BOOL.
ms.assetid: 0d3c1f3a-f497-4e92-81e9-8647006910e1
title: 'Metodo ID3DXTextureShader:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49fbc2d2841957e75a8bc3adaf40ce0fdf5e2a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762251"
---
# <a name="id3dxtextureshadersetbool-method"></a>Metodo ID3DXTextureShader:: SetValue

Imposta un valore BOOL.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hConstant,
  [in] BOOL       b
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConstant* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco della costante. Vedere [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*b* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Valore BOOL.

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

 

 

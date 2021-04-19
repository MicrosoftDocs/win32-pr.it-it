---
description: Ottiene un pixel shader.
ms.assetid: 173a20a5-dda0-493f-a161-2dc2881e71f2
title: 'Metodo ID3DXBaseEffect:: GetPixelShader (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e555bac2e20ebab1cb0aec3d313cab8ad05e833e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323589"
---
# <a name="id3dxbaseeffectgetpixelshader-method"></a>Metodo ID3DXBaseEffect:: GetPixelShader

Ottiene un pixel shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPixelShader(
  [in]  D3DXHANDLE             hParameter,
  [out] LPDIRECT3DPIXELSHADER9 *ppPShader
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*ppPShader* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)\***

Restituisce un oggetto pixel shader. Vedere l'oggetto [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9) .

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

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 

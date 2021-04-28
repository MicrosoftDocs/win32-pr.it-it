---
description: 'Funzione D3DXFillVolumeTextureTX: usa una funzione HLSL (High-Level Shader Language) compilata per riempire ogni texel di ogni livello mipmap di una trama.'
ms.assetid: f082e1d2-c433-482c-9288-58e5c558cdc5
title: Funzione D3DXFillVolumeTextureTX (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 30aac53aa6451885bbd4ae2cac63050b01157974
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107629"
---
# <a name="d3dxfillvolumetexturetx-function"></a>Funzione D3DXFillVolumeTextureTX

Usa una funzione HLSL (High-Level Shader Language) compilata per riempire ogni texel di ogni livello mipmap di una trama.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTexture* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Puntatore a [**un oggetto IDirect3DVolumeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) che rappresenta la trama da riempire.

</dd> <dt>

*pTextureShader* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**

Puntatore a un oggetto shader di trama [**ID3DXTextureShader.**](id3dxtextureshader.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

La destinazione della trama deve essere una funzione HLSL che accetta contiene la semantica seguente:

-   Un parametro di input deve usare una semantica POSITION.
-   Un parametro di input deve usare una semantica PSIZE.
-   La funzione deve restituire un parametro che usa la semantica COLOR.

I parametri di input possono essere in qualsiasi ordine. Per un esempio, vedere [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillTextureTX**](d3dxfilltexturetx.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 

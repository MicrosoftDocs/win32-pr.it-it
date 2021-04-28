---
description: 'Funzione D3DXFillTextureTX: usa una funzione HLSL (High Level Shader Language) compilata per riempire ogni texel di ogni livello mipmap di una trama.'
ms.assetid: 013660ce-865e-4acf-a1ea-670e70377ff5
title: Funzione D3DXFillTextureTX (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 419dc0e7b4266a2fe32557c52ed4323b51a25843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107639"
---
# <a name="d3dxfilltexturetx-function"></a>Funzione D3DXFillTextureTX

Usa una funzione HLSL (High-Level Shader Language) compilata per riempire ogni texel di ogni livello mipmap di una trama.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXFillTextureTX(
  _Inout_ LPDIRECT3DTEXTURE9  pTexture,
  _In_    LPD3DXTEXTURESHADER pTextureShader
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTexture* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a [**un oggetto IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la trama da riempire.

</dd> <dt>

*pTextureShader* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**

Puntatore a un oggetto shader con trama [**ID3DXTextureShader.**](id3dxtextureshader.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

La destinazione della trama deve essere una funzione HLSL che accetta contiene la semantica seguente:

-   Un parametro di input deve usare una semantica POSITION.
-   Un parametro di input deve usare una semantica PSIZE.
-   La funzione deve restituire un parametro che usa la semantica COLOR.

Di seguito è riportato un esempio di tale funzione HLSL:


```
float4 TextureGradientFill(
  float2 vTexCoord : POSITION, 
  float2 vTexelSize : PSIZE) : COLOR 
  {
    float r,g, b, xSq,ySq, a;
    xSq = 2.f*vTexCoord.x-1.f; xSq *= xSq;
    ySq = 2.f*vTexCoord.y-1.f; ySq *= ySq;
    a = sqrt(xSq+ySq);
    if (a > 1.0f) {
        a = 1.0f-(a-1.0f);
    }
    else if (a < 0.2f) {
        a = 0.2f;
    }
    r = 1-vTexCoord.x;
    g = 1-vTexCoord.y;
    b = vTexCoord.x;
    return float4(r, g, b, a);
    
  };
```



Si noti che i parametri di input possono essere in qualsiasi ordine, ma è necessario rappresentare entrambe le semantiche di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> <dt>

[**D3DXFillVolumeTextureTX**](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 

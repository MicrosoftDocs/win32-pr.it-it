---
description: Usa una funzione fornita dall'utente per riempire ogni texel di ogni livello mip di una determinata trama del volume.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: Funzione D3DXFillVolumeTexture (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e0ef21c3fb9b5443cc488a3b6fc953953cffee6e5d0dc417dee69969907f86e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123291"
---
# <a name="d3dxfillvolumetexture-function"></a>Funzione D3DXFillVolumeTexture

Usa una funzione fornita dall'utente per riempire ogni texel di ogni livello mip di una determinata trama del volume.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTexture* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Puntatore a [**un'interfaccia IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) che rappresenta la trama riempita.

</dd> <dt>

*pFunction* \[ Pollici\]
</dt> <dd>

Tipo: **[LPD3DXFILL3D](lpd3dxfill3d.md)**

Puntatore a una funzione dell'analizzatore fornita dall'utente, che verrà usata per calcolare il valore di ogni texel. La funzione segue il prototipo [di LPD3DXFILL3D](lpd3dxfill3d.md).

</dd> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore a un blocco arbitrario di dati definiti dall'utente. Questo puntatore verrà passato alla funzione fornita in *pFunction*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Se il volume è non dinamico (perché l'utilizzo è impostato su 0 al momento della creazione) e si trova nella memoria video (il pool di memoria impostato su D3DPOOL \_ DEFAULT), **D3DXFillVolumeTexture** avrà esito negativo perché il volume non può essere bloccato.

Questo esempio crea una funzione denominata ColorVolumeFill, che si basa su D3DXFillVolumeTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
{
       return hr;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

---
description: Usa una funzione fornita dall'utente per riempire ogni Texel di ogni livello MIP di una determinata trama.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: Funzione D3DXFillTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20790a9e4c1a9ce242a5e067dd617c7871a70b7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354864"
---
# <a name="d3dxfilltexture-function"></a>D3DXFillTexture (funzione)

Usa una funzione fornita dall'utente per riempire ogni Texel di ogni livello MIP di una determinata trama.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta la trama compilata.

</dd> <dt>

*pFunction* \[ in\]
</dt> <dd>

Tipo: **[LPD3DXFILL2D](lpd3dxfill2d.md)**

Puntatore a una funzione dell'analizzatore fornita dall'utente, che verrà usata per calcolare il valore di ogni Texel. La funzione segue il prototipo di [LPD3DXFILL2D](lpd3dxfill2d.md).

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore a un blocco arbitrario di dati definiti dall'utente. Questo puntatore verrà passato alla funzione fornita in *pFunction*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Di seguito è riportato un esempio in cui viene creata una funzione denominata ColorFill, che si basa su D3DXFillTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

---
description: Converte una mappa di altezza in una mappa normale. Ai componenti (x, y, z) di ogni normale viene eseguito il mapping ai canali (r, g, b) della trama di output.
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: Funzione D3DXComputeNormalMap (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormalMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e22418f5a023dbe70fee8ea0fba8a449abbcc8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323265"
---
# <a name="d3dxcomputenormalmap-function"></a>D3DXComputeNormalMap (funzione)

Converte una mappa di altezza in una mappa normale. Ai componenti (x, y, z) di ogni normale viene eseguito il mapping ai canali (r, g, b) della trama di output.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeNormalMap(
  _Out_       LPDIRECT3DTEXTURE9 pTexture,
  _In_        LPDIRECT3DTEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY       *pSrcPalette,
  _In_        DWORD              Flags,
  _In_        DWORD              Channel,
  _In_        FLOAT              Amplitude
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta la trama di destinazione.

</dd> <dt>

*pSrcTexture* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta la trama della mappa dell'altezza di origine.

</dd> <dt>

*pSrcPalette* \[ in\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a un tipo [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) che contiene la tavolozza di origine di 256 colori o **null**.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uno o più [flag \_ normalmap D3DX](d3dx-normalmap.md) che controllano la generazione di mappe normali.

</dd> <dt>

*Canale* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Un flag del [ \_ canale D3DX](d3dx-channel.md) che specifica l'origine delle informazioni sull'altezza.

</dd> <dt>

*Ampiezza* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore costante moltiplicatore che aumenta (o diminuisce) i valori nella mappa normale. I valori più elevati in genere rendono più visibili i riscontri, mentre i valori più bassi rendono meno visibili i riscontri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo calcola la normalità usando la differenza centrale con una dimensione del kernel di 3x3. Il denominatore differenze centrale usato è 2,0. I canali RGB nella destinazione contengono i componenti parziali (x, y, z) del normale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

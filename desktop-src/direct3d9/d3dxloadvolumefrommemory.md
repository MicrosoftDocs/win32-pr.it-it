---
description: Carica un volume dalla memoria.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: Funzione D3DXLoadVolumeFromMemory (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c473d5194a20a7de7e20d76fbde18d0a974ff8f314dc93822f57bfef2a4a6a5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122965"
---
# <a name="d3dxloadvolumefrommemory-function"></a>Funzione D3DXLoadVolumeFromMemory

Carica un volume dalla memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDestVolume* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Puntatore a [**un'interfaccia IDirect3DVolume9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) Specifica il volume di destinazione che riceve l'immagine.

</dd> <dt>

*pDestPalette* \[ Pollici\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a [**una struttura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) la tavolozza di destinazione di 256 colori o **NULL.**

</dd> <dt>

*pDestBox* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntatore a [**una struttura D3DBOX.**](d3dbox.md) Specifica la casella di destinazione. Impostare questo parametro su **NULL per** specificare l'intero volume.

</dd> <dt>

*pSrcMemory* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore all'angolo superiore sinistro del volume di origine in memoria.

</dd> <dt>

*SrcFormat* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro del [tipo enumerato D3DFORMAT,](d3dformat.md) il formato pixel del volume di origine.

</dd> <dt>

*SrcRowPitch* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Passo dell'immagine di origine, in byte. Per i formati DXT (formati di trama compressa), questo numero deve rappresentare le dimensioni di una riga di celle, in byte.

</dd> <dt>

*SrcSlicePitch* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Passo dell'immagine di origine, in byte. Per i formati DXT (formati di trama compressa), questo numero deve rappresentare le dimensioni di una sezione di celle, in byte.

</dd> <dt>

*pSrcPalette* \[ Pollici\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a una [**struttura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) la tavolozza di origine di 256 colori o **NULL.**

</dd> <dt>

*pSrcBox* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntatore a [**una struttura D3DBOX.**](d3dbox.md) Specifica la casella di origine. **NULL** non è un valore valido per questo parametro.

</dd> <dt>

*Filtro* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [filtri D3DX \_ che](d3dx-filter.md) controllano la modalità di filtro dell'immagine. Specificare D3DX DEFAULT per questo parametro equivale a specificare \_ D3DX \_ \_ FILTER TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*ColorKey* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Valore D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare la chiave di colore. Si tratta sempre di un colore ARGB a 32 bit, indipendentemente dal formato dell'immagine di origine. Il valore alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache. Pertanto, per il nero opaco, il valore sarebbe uguale a 0xFF000000.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

La scrittura su una superficie diversa da zero della trama del volume non causerà l'aggiornamento del rettangolo dirty. Se viene chiamato **D3DXLoadVolumeFromMemory** e la trama non era già dirty (questo è improbabile in scenari di utilizzo normale), l'applicazione deve chiamare in modo esplicito [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sulla trama del volume.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

---
description: Carica una superficie dalla memoria.
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: Funzione D3DXLoadSurfaceFromMemory (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1b2bcb98f5fd64da221f73bf2cee4222d8925797acd4c7e01914e8e068d6e381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123049"
---
# <a name="d3dxloadsurfacefrommemory-function"></a>Funzione D3DXLoadSurfaceFromMemory

Carica una superficie dalla memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadSurfaceFromMemory(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPCVOID            pSrcMemory,
  _In_       D3DFORMAT          SrcFormat,
  _In_       UINT               SrcPitch,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDestSurface* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Puntatore a [**un'interfaccia IDirect3DSurface9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) Specifica la superficie di destinazione, che riceve l'immagine.

</dd> <dt>

*pDestPalette* \[ Pollici\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a [**una struttura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) la tavolozza di destinazione di 256 colori o **NULL.**

</dd> <dt>

*pDestRect* \[ Pollici\]
</dt> <dd>

Tipo: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Puntatore a una [**struttura RECT.**](/previous-versions//dd162897(v=vs.85)) Specifica il rettangolo di destinazione. Impostare questo parametro su **NULL per** specificare l'intera superficie.

</dd> <dt>

*pSrcMemory* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore all'angolo superiore sinistro dell'immagine di origine in memoria.

</dd> <dt>

*SrcFormat* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro del tipo [enumerato D3DFORMAT,](d3dformat.md) il formato pixel dell'immagine di origine.

</dd> <dt>

*SrcPitch* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Passo dell'immagine di origine, in byte. Per i formati DXT, questo numero deve rappresentare la larghezza di una riga di celle, in byte.

</dd> <dt>

*pSrcPalette* \[ Pollici\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a una [**struttura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) la tavolozza di origine di 256 colori o **NULL.**

</dd> <dt>

*pSrcRect* \[ Pollici\]
</dt> <dd>

Tipo: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Puntatore a una [**struttura RECT.**](/previous-versions//dd162897(v=vs.85)) Specifica le dimensioni dell'immagine di origine in memoria. Questo valore non può essere **NULL.**

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

Questa funzione gestisce la conversione da e verso formati di trama compressi.

La scrittura su una superficie non di livello zero non causerà l'aggiornamento del rettangolo dirty. Se viene chiamato **D3DXLoadSurfaceFromMemory** e la superficie non era già dirty (questo è improbabile in scenari di utilizzo normale), l'applicazione deve chiamare in modo esplicito [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sulla superficie.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

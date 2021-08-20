---
description: Carica una superficie da una risorsa.
ms.assetid: 16d49f61-8c84-4e15-aacc-1d26099e65e0
title: Funzione D3DXLoadSurfaceFromResource (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9aef57ec03066e8783f104282c770f1143c00b87fd0221b5c477ca5227fe398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095992"
---
# <a name="d3dxloadsurfacefromresource-function"></a>Funzione D3DXLoadSurfaceFromResource

Carica una superficie da una risorsa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadSurfaceFromResource(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          HMODULE            hSrcModule,
  _In_          LPCTSTR            pSrcResource,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
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

*hSrcModule* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle al modulo in cui si trova la risorsa oppure **NULL** per il modulo associato all'immagine usata dal sistema operativo per creare il processo corrente.

</dd> <dt>

*pSrcResource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome della risorsa. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati stringa viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*pSrcRect* \[ Pollici\]
</dt> <dd>

Tipo: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Puntatore a una [**struttura RECT.**](/previous-versions//dd162897(v=vs.85)) Specifica il rettangolo di origine. Impostare questo parametro su **NULL per** specificare l'intera immagine.

</dd> <dt>

*Filtro* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [filtri D3DX \_ che](d3dx-filter.md) controllano la modalità di filtro dell'immagine. Specificare D3DX DEFAULT per questo parametro equivale a specificare \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*ColorKey* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Valore D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare la chiave di colore. Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato dell'immagine di origine. Alpha è significativo e in genere deve essere impostato su FF per le chiavi di colore opaco. Pertanto, per il nero opaco, il valore sarebbe uguale a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Puntatore a [**una struttura D3DXIMAGE \_ INFO**](d3dximage-info.md) da riempire con una descrizione dei dati nel file di immagine di origine oppure **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se unicode è definito, la chiamata di funzione viene risolta in D3DXLoadSurfaceFromResourceW. In caso contrario, la chiamata di funzione viene risolta in D3DXLoadSurfaceFromResourceA perché vengono usate stringhe ANSI.

La risorsa caricata deve essere di tipo RT \_ BITMAP o RT \_ RCDATA. Il tipo di risorsa RT RCDATA viene usato per caricare formati diversi da bitmap, ad esempio \_ .tga, .jpg e .dds.

Questa funzione gestisce la conversione da e verso formati di trama compressi.

La scrittura in una superficie non di livello zero non causerà l'aggiornamento del rettangolo dirty. Se viene chiamato [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) e la superficie non era già dirty (questo è improbabile nei normali scenari di utilizzo), l'applicazione deve chiamare in modo esplicito [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sulla superficie.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

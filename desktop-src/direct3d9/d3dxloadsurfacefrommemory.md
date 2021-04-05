---
description: Carica una superficie dalla memoria.
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: Funzione D3DXLoadSurfaceFromMemory (D3dx9tex. h)
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
ms.openlocfilehash: ffb7be05301ae807505242153be902ab30eecf14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058588"
---
# <a name="d3dxloadsurfacefrommemory-function"></a>D3DXLoadSurfaceFromMemory (funzione)

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

*pDestSurface* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Puntatore a un'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) . Specifica la superficie di destinazione che riceve l'immagine.

</dd> <dt>

*pDestPalette* \[ in\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di destinazione di 256 colori o **null**.

</dd> <dt>

*pDestRect* \[ in\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) . Specifica il rettangolo di destinazione. Impostare questo parametro su **null** per specificare l'intera superficie.

</dd> <dt>

*pSrcMemory* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore all'angolo superiore sinistro dell'immagine di origine in memoria.

</dd> <dt>

*SrcFormat* \[ in\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , il formato pixel dell'immagine di origine.

</dd> <dt>

*SrcPitch* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Pitch of source image, in bytes. Per i formati DXT, questo numero deve rappresentare la larghezza di una riga di celle, in byte.

</dd> <dt>

*pSrcPalette* \[ in\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di origine di 256 colori o **null**.

</dd> <dt>

*pSrcRect* \[ in\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) . Specifica le dimensioni dell'immagine di origine in memoria. Questo valore non può essere **null**.

</dd> <dt>

*Filtro* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata. Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .

</dd> <dt>

*ColorKey* \[ in\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey. Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine. Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache. Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Questa funzione gestisce la conversione da e verso formati di trama compressi.

La scrittura in una superficie non di livello zero non comporterà l'aggiornamento del rettangolo modificato. Se viene chiamato **D3DXLoadSurfaceFromMemory** e la superficie non è già sporca (si tratta di un problema improbabile in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sulla superficie.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

---
description: Carica un volume da una risorsa.
ms.assetid: 3fa1243b-5e31-4737-8d3c-08852d6528d9
title: Funzione D3DXLoadVolumeFromResource (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941aaa775a3f286bf25187bbb0ce75e3d39037be9c3ce33571aff755335a3ad5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122911"
---
# <a name="d3dxloadvolumefromresource-function"></a>Funzione D3DXLoadVolumeFromResource

Carica un volume da una risorsa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadVolumeFromResource(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       HMODULE           hSrcModule,
  _In_       LPCSTR            pSrcResource,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDestVolume* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Puntatore a [**un'interfaccia IDirect3DVolume9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) Specifica il volume di destinazione.

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

*hSrcModule* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle per il modulo in cui si trova la risorsa o **NULL** per il modulo associato all'immagine usata dal sistema operativo per creare il processo corrente.

</dd> <dt>

*pSrcResource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome file dell'immagine di origine. Se sono definiti \_ unicode o UNICODE, questo tipo di parametro è LPCWSTR. In caso contrario, il tipo è LPCSTR.

</dd> <dt>

*pSrcBox* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntatore a [**una struttura D3DBOX.**](d3dbox.md) Specifica la casella di origine. Impostare questo parametro su **NULL per** specificare l'intero volume.

</dd> <dt>

*Filtro* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [filtri D3DX, \_ ](d3dx-filter.md)che controllano la modalità di filtro dell'immagine. Specificare D3DX DEFAULT per questo parametro equivale a specificare \_ D3DX \_ \_ FILTER TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*ColorKey* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Valore D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare la chiave di colore. Si tratta sempre di un colore ARGB a 32 bit, indipendentemente dal formato dell'immagine di origine. Il valore alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache. Pertanto, per il nero opaco, il valore sarebbe uguale a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Puntatore a [**una struttura D3DXIMAGE \_ INFO**](d3dximage-info.md) da riempire con una descrizione dei dati nel file di immagine di origine oppure **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

La risorsa caricata deve essere una risorsa bitmap (RT \_ BITMAP).

Questa funzione gestisce la conversione da e verso formati di trama compressi.

La scrittura su una superficie diversa da zero della trama del volume non causerà l'aggiornamento del rettangolo dirty. Se viene chiamato [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) e la trama non era già dirty (questo è improbabile in scenari di utilizzo normale), l'applicazione deve chiamare in modo esplicito [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sulla trama del volume.

Questa funzione supporta sia stringhe Unicode che ANSI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromFileInMemory**](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromMemory**](d3dxloadvolumefrommemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

---
description: Filtra i livelli mipmap di una trama.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: Funzione D3DXFilterTexture (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc07336edb5f7bb8672fbbec415b0a3b312335a3a3a4b0de32aec4fdde558363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988501"
---
# <a name="d3dxfiltertexture-function"></a>Funzione D3DXFilterTexture

Filtra i livelli mipmap di una trama.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBaseTexture* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Puntatore a [**un'interfaccia IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) che rappresenta l'oggetto trama da filtrare.

</dd> <dt>

*pPalette* \[ Cambio\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a [**una struttura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) che rappresenta una tavolozza di 256 colori da compilare o **NULL** per i formati non apalettizzati. Se non viene specificata una tavolozza, viene fornita la tavolozza Direct3D predefinita ,ovvero una tavolozza bianca opaca. Vedere la sezione Osservazioni.

</dd> <dt>

*SrcLevel* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Livello la cui immagine viene usata per generare i livelli successivi. Specificare D3DX \_ DEFAULT per questo parametro equivale a specificare 0.

</dd> <dt>

*MipFilter* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [filtri D3DX \_ che](d3dx-filter.md) controllano la modalità di filtro della mappa mipmap. Specificare D3DX DEFAULT per questo parametro equivale a specificare D3DX FILTER BOX se le dimensioni della trama sono due \_ \_ e \_ D3DX \_ FILTER BOX \_ \| D3DX \_ FILTER DITHER \_ in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Un filtro viene applicato in modo ricorsivo a ogni livello di trama per generare il livello di trama successivo.

La scrittura in una superficie non di livello zero della trama non causerà l'aggiornamento del rettangolo dirty. Se viene chiamato **D3DXFilterTexture** e la superficie non era già dirty (questo è improbabile nei normali scenari di utilizzo), l'applicazione deve chiamare in modo esplicito [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sulla trama.

Le trame create nel pool predefinito (D3DPOOL DEFAULT) non possono essere usate con \_ **D3DXFilterTexture** (a meno che non siano state create con D3DUSAGE DYNAMIC) perché è necessaria un'operazione di blocco \_ sull'oggetto. Si noti che i blocchi non sono consentiti per le trame nel pool predefinito (a meno che non siano dinamici).

Per informazioni [**dettagliate su PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)vedere Platform SDK. Si noti che a data di DirectX 8.0, il membro peFlags della struttura **PALETTEENTRY** non funziona come documentato in Platform SDK. Il membro peFlags è ora il canale alfa per i formati con palettizzazione a 8 bit.

Esiste una sola funzione di filtro trame, ma due macro che chiamano questo metodo.


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
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

 

 

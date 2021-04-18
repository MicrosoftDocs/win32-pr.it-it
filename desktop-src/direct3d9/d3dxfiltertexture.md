---
description: Filtra i livelli di mipmap di una trama.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: Funzione D3DXFilterTexture (D3dx9tex. h)
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
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322696"
---
# <a name="d3dxfiltertexture-function"></a>D3DXFilterTexture (funzione)

Filtra i livelli di mipmap di una trama.

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

*pBaseTexture* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Puntatore a un'interfaccia [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) che rappresenta l'oggetto trama da filtrare.

</dd> <dt>

*pPalette* \[ out\]
</dt> <dd>

Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) che rappresenta una tavolozza dei colori 256 da compilare o **null** per i formati nonpalettized. Se non si specifica una tavolozza, viene fornita la tavolozza Direct3D predefinita, ovvero una tavolozza bianca completamente opaca. Vedere la sezione Osservazioni.

</dd> <dt>

*SrcLevel* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Livello la cui immagine viene utilizzata per generare i livelli successivi. Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare 0.

</dd> <dt>

*MipFilter* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano la modalità di filtraggio del mipmap. Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare la \_ casella di filtro D3DX \_ se la dimensione della trama è una potenza di due e la \_ casella di filtro D3DX \_ \| D3DX \_ filtrare \_ in altro modo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Un filtro viene applicato in modo ricorsivo a ogni livello di trama per generare il livello di trama successivo.

Se si scrive in una superficie non di livello zero della trama, il rettangolo modificato non verrà aggiornato. Se viene chiamato **D3DXFilterTexture** e la superficie non è già sporca (si tratta di un problema improbabile in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sulla trama.

Le trame create nel pool predefinito ( \_ impostazione predefinita D3DPOOL) non possono essere usate con **D3DXFilterTexture** (a meno che non vengano create con D3DUSAGE \_ Dynamic) perché è necessaria un'operazione di blocco sull'oggetto. Si noti che i blocchi non sono consentiti nelle trame del pool predefinito (a meno che non siano dinamici).

Per informazioni dettagliate su [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), vedere Platform SDK. Si noti che, a partire da DirectX 8,0, il membro peFlags della struttura **PaletteEntry** non funziona come documentato in Platform SDK. Il membro peFlags è ora il canale alfa per i formati pallettizzati a 8 bit.

Esiste una sola funzione di filtro di trama, ma due macro che chiamano questo metodo.


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
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

 

 

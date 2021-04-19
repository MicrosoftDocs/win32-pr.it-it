---
description: Prepara un dispositivo per il disegno degli sprite.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'Metodo ID3DXSprite:: begin (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322973"
---
# <a name="id3dxspritebegin-method"></a>Metodo ID3DXSprite:: Begin

Prepara un dispositivo per il disegno degli sprite.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di zero o più flag che descrivono le opzioni di rendering sprite. Per questo metodo, i flag validi sono:

-   \_AlphaBlend D3DXSPRITE
-   \_ \_ TABELLONe D3DXSPRITE
-   D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE
-   \_DONOTSAVESTATE D3DXSPRITE
-   \_OBJECTSPACE D3DXSPRITE
-   \_ \_ Profondità di ordinamento D3DXSPRITE \_ \_ BACKTOFRONT
-   \_ \_ Profondità di ordinamento D3DXSPRITE \_ \_ FRONTTOBACK
-   \_ \_ Trama di ordinamento D3DXSPRITE \_

Per una descrizione dei flag e per informazioni su come controllare le trasformazioni di acquisizione dello stato del dispositivo e visualizzazione dispositivi, vedere [D3DXSPRITE](d3dxsprite.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato dall'interno di [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) . . . Sequenza [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) . Impossibile utilizzare **ID3DXSprite:: Begin** come sostituto di **IDirect3DDevice9:: BeginScene** o [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md).

Questo metodo consente di impostare gli Stati seguenti nel dispositivo.

Stati di rendering:



| Tipo ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)) | Valore                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| \_ALPHABLENDENABLE D3DRS                                       | true                                                                                                              |
| \_ALPHAFUNC D3DRS                                              | D3DCMP \_ maggiore                                                                                                   |
| \_ALPHAREF D3DRS                                               | 0x00                                                                                                              |
| \_ALPHATESTENABLE D3DRS                                        | AlphaCmpCaps                                                                                                      |
| \_BLENDOP D3DRS                                                | D3DBLENDOP \_ aggiungere                                                                                                   |
| Ritaglio D3DRS \_                                               | true                                                                                                              |
| \_CLIPPLANEENABLE D3DRS                                        | FALSE                                                                                                             |
| \_COLORWRITEENABLE D3DRS                                       | D3DCOLORWRITEENABLE \_ alfa \| D3DCOLORWRITEENABLE \_ blu \| D3DCOLORWRITEENABLE \_ verde \| D3DCOLORWRITEENABLE \_ rosso |
| \_CULLMODE D3DRS                                               | D3DCULL \_ None                                                                                                     |
| \_DESTBLEND D3DRS                                              | \_INVSRCALPHA D3DBLEND                                                                                             |
| \_DIFFUSEMATERIALSOURCE D3DRS                                  | \_COLOR1 D3DMCS                                                                                                    |
| \_ENABLEADAPTIVETESSELLATION D3DRS                             | FALSE                                                                                                             |
| \_FillMode D3DRS                                               | D3DFILL \_ Solid                                                                                                    |
| \_FOGENABLE D3DRS                                              | FALSE                                                                                                             |
| \_INDEXEDVERTEXBLENDENABLE D3DRS                               | FALSE                                                                                                             |
| \_Illuminazione D3DRS                                               | FALSE                                                                                                             |
| \_RANGEFOGENABLE D3DRS                                         | FALSE                                                                                                             |
| \_SEPARATEALPHABLENDENABLE D3DRS                               | FALSE                                                                                                             |
| \_MODOOMBRA D3DRS                                              | \_Gouraud D3DSHADE                                                                                                 |
| \_SPECULARENABLE D3DRS                                         | FALSE                                                                                                             |
| \_SRCBLEND D3DRS                                               | \_SRCALPHA D3DBLEND                                                                                                |
| \_SRGBWRITEENABLE D3DRS                                        | FALSE                                                                                                             |
| \_STENCILENABLE D3DRS                                          | FALSE                                                                                                             |
| \_VERTEXBLEND D3DRS                                            | FALSE                                                                                                             |
| \_WRAP0 D3DRS                                                  | 0                                                                                                                 |



 

Stati della fase trama:



| Identificatore fase | Tipo ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)) | Valore            |
|------------------|---------------------------------------------------------------------------|------------------|
| 0                | \_ALPHAARG1 D3DTSS                                                         | \_Trama D3DTA   |
| 0                | \_ALPHAARG2 D3DTSS                                                         | D3DTA \_ diffuse   |
| 0                | \_ALPHAOP D3DTSS                                                           | \_Modulazione D3DTOP |
| 0                | \_COLORARG1 D3DTSS                                                         | \_Trama D3DTA   |
| 0                | \_COLORARG2 D3DTSS                                                         | D3DTA \_ diffuse   |
| 0                | \_COLOROP D3DTSS                                                           | \_Modulazione D3DTOP |
| 0                | \_TEXCOORDINDEX D3DTSS                                                     | 0                |
| 0                | \_TEXTURETRANSFORMFLAGS D3DTSS                                             | \_Disabilitazione D3DTTFF |
| 1                | \_ALPHAOP D3DTSS                                                           | \_Disabilitazione D3DTOP  |
| 1                | \_COLOROP D3DTSS                                                           | \_Disabilitazione D3DTOP  |



 

Stati campionatore:



| Indice fase campionatore | Tipo ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)) | Valore                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 0                   | \_Indirizzo D3DSAMP                                               | \_Clamp D3DTADDRESS                                                                                             |
| 0                   | \_ADDRESSV D3DSAMP                                               | \_Clamp D3DTADDRESS                                                                                             |
| 0                   | \_MAGFILTER D3DSAMP                                              | D3DTEXF \_ anisotropico se TextureFilterCaps include D3DPTFILTERCAPS \_ MAGFANISOTROPIC; in caso contrario, D3DTEXF \_ lineare |
| 0                   | \_MAXMIPLEVEL D3DSAMP                                            | 0                                                                                                              |
| 0                   | \_MAXANISOTROPY D3DSAMP                                          | MaxAnisotropy                                                                                                  |
| 0                   | \_MINFILTER D3DSAMP                                              | D3DTEXF \_ anisotropico se TextureFilterCaps include D3DPTFILTERCAPS \_ MINFANISOTROPIC; in caso contrario, D3DTEXF \_ lineare |
| 0                   | \_MIPFILTER D3DSAMP                                              | D3DTEXF \_ lineare se TextureFilterCaps include D3DPTFILTERCAPS \_ MIPFLINEAR; in caso contrario, punto di D3DTEXF \_            |
| 0                   | \_MIPMAPLODBIAS D3DSAMP                                          | 0                                                                                                              |
| 0                   | \_SRGBTEXTURE D3DSAMP                                            | 0                                                                                                              |



 

> [!Note]  
> Questo metodo Disabilita le N-patch.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[D3DXSPRITE](d3dxsprite.md)
</dt> </dl>

 

 

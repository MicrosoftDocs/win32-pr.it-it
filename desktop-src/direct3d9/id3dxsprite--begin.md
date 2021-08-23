---
description: Prepara un dispositivo per il disegno di sprite.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: Metodo ID3DXSprite::Begin (D3dx9core.h)
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
ms.openlocfilehash: 94d3ee659937508f52e38513006701494a01ed4ff95fe6c75c56bd9638137160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119277831"
---
# <a name="id3dxspritebegin-method"></a>Metodo ID3DXSprite::Begin

Prepara un dispositivo per il disegno di sprite.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di zero o più flag che descrivono le opzioni di rendering dello sprite. Per questo metodo, i flag validi sono:

-   D3DXSPRITE \_ ALPHABLEND
-   D3DXSPRITE \_ \_ BILLBOARD
-   D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE
-   D3DXSPRITE \_ DONOTSAVESTATE
-   SPAZIO OGGETTI D3DXSPRITE \_
-   D3DXSPRITE \_ \_ SORT \_ DEPTH \_ BACKTOFRONT
-   D3DXSPRITE \_ \_ SORT \_ DEPTH \_ FRONTTOBACK
-   TRAMA DI ORDINAMENTO D3DXSPRITE \_ \_ \_

Per una descrizione dei flag e per informazioni su come controllare l'acquisizione dello stato del dispositivo e le trasformazioni della visualizzazione del dispositivo, vedere [D3DXSPRITE](d3dxsprite.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato dall'interno di [**un oggetto IDirect3DDevice9::BeginScene**](/windows/desktop/api) . . . [**Sequenza IDirect3DDevice9::EndScene.**](/windows/desktop/api) **ID3DXSprite::Begin** non può essere usato come sostituto di **IDirect3DDevice9::BeginScene** o [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).

Questo metodo imposta gli stati seguenti nel dispositivo.

Stati di rendering:



| Tipo ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)) | Valore                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3DRS \_ ALPHABLENDENABLE                                       | true                                                                                                              |
| D3DRS \_ ALPHAFUNC                                              | D3DCMP \_ GREATER                                                                                                   |
| D3DRS \_ ALPHAREF                                               | 0x00                                                                                                              |
| D3DRS \_ ALPHATESTENABLE                                        | AlphaCmpCaps                                                                                                      |
| D3DRS \_ BLENDOP                                                | D3DBLENDOP \_ ADD                                                                                                   |
| RITAGLIO \_ D3DRS                                               | true                                                                                                              |
| D3DRS \_ CLIPPLANEENABLE                                        | FALSE                                                                                                             |
| D3DRS \_ COLORWRITEENABLE                                       | D3DCOLORWRITEENABLE \_ ALPHA \| D3DCOLORWRITEENABLE \_ BLUE \| D3DCOLORWRITEENABLE \_ GREEN \| D3DCOLORWRITEENABLE \_ RED |
| D3DRS \_ CULLMODE                                               | D3DCULL \_ NONE                                                                                                     |
| D3DRS \_ DESTBLEND                                              | D3DBLEND \_ INVSRCALPHA                                                                                             |
| D3DRS \_ DIFFUSEMATERIALSOURCE                                  | D3DMCS \_ COLOR1                                                                                                    |
| D3DRS \_ ENABLEADAPTIVETESSELLATION                             | FALSE                                                                                                             |
| D3DRS \_ FILLMODE                                               | D3DFILL \_ SOLID                                                                                                    |
| D3DRS \_ FOGENABLE                                              | FALSE                                                                                                             |
| D3DRS \_ INDEXEDVERTEXBLENDENABLE                               | FALSE                                                                                                             |
| ILLUMINAZIONE \_ D3DRS                                               | FALSE                                                                                                             |
| D3DRS \_ RANGEFOGENABLE                                         | FALSE                                                                                                             |
| D3DRS \_ SEPARATEALPHABLENDENABLE                               | FALSE                                                                                                             |
| D3DRS \_ SHADEMODE                                              | D3DSHADE \_ GOURAUD                                                                                                 |
| D3DRS \_ SPECULARENABLE                                         | FALSE                                                                                                             |
| D3DRS \_ SRCBLEND                                               | D3DBLEND \_ SRCALPHA                                                                                                |
| D3DRS \_ SRGBWRITEENABLE                                        | FALSE                                                                                                             |
| D3DRS \_ STENCILENABLE                                          | FALSE                                                                                                             |
| D3DRS \_ VERTEXBLEND                                            | FALSE                                                                                                             |
| D3DRS \_ WRAP0                                                  | 0                                                                                                                 |



 

Stati della fase di trama:



| Identificatore di fase | Tipo ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)) | Valore            |
|------------------|---------------------------------------------------------------------------|------------------|
| 0                | D3DTSS \_ ALPHAARG1                                                         | TRAMA D3DTA \_   |
| 0                | D3DTSS \_ ALPHAARG2                                                         | D3DTA \_ DIFFUSE   |
| 0                | D3DTSS \_ ALPHAOP                                                           | MODULAZIONE \_ D3DTOP |
| 0                | D3DTSS \_ COLORARG1                                                         | TRAMA D3DTA \_   |
| 0                | D3DTSS \_ COLORARG2                                                         | D3DTA \_ DIFFUSE   |
| 0                | D3DTSS \_ COLOROP                                                           | MODULAZIONE \_ D3DTOP |
| 0                | D3DTSS \_ TEXCOORDINDEX                                                     | 0                |
| 0                | D3DTSS \_ TEXTURETRANSFORMFLAGS                                             | D3DTTFF \_ DISABLE |
| 1                | D3DTSS \_ ALPHAOP                                                           | D3DTOP \_ DISABLE  |
| 1                | D3DTSS \_ COLOROP                                                           | D3DTOP \_ DISABLE  |



 

Stati del campionatore:



| Indice della fase di campionamento | Tipo ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)) | Valore                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 0                   | D3DSAMP \_ ADDRESSU                                               | D3DTADDRESS \_ CLAMP                                                                                             |
| 0                   | D3DSAMP \_ ADDRESSV                                               | D3DTADDRESS \_ CLAMP                                                                                             |
| 0                   | D3DSAMP \_ MAGFILTER                                              | D3DTEXF \_ ANISOTROP se TextureFilterCaps include D3DPTFILTERCAPS \_ MAGFANISOTROP; in caso contrario D3DTEXF \_ LINEAR |
| 0                   | D3DSAMP \_ MAXMIPLEVEL                                            | 0                                                                                                              |
| 0                   | D3DSAMP \_ MAXANISOTROPY                                          | MaxAnisotropy                                                                                                  |
| 0                   | D3DSAMP \_ MINFILTER                                              | D3DTEXF \_ ANISOTROP se TextureFilterCaps include D3DPTFILTERCAPS \_ MINFANISOTROP; in caso contrario D3DTEXF \_ LINEAR |
| 0                   | D3DSAMP \_ MIPFILTER                                              | D3DTEXF \_ LINEAR se TextureFilterCaps include D3DPTFILTERCAPS \_ MIPFLINEAR; in caso contrario D3DTEXF \_ POINT            |
| 0                   | D3DSAMP \_ MIPMAPLODBIAS                                          | 0                                                                                                              |
| 0                   | D3DSAMP \_ SRGBTEXTURE                                            | 0                                                                                                              |



 

> [!Note]  
> Questo metodo disabilita N patch.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[D3DXSPRITE](d3dxsprite.md)
</dt> </dl>

 

 

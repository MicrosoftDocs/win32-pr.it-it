---
description: Un blocco di stato può essere usato per acquisire solo lo stato del pixel (vedere lo stato di salvataggio e ripristino di blocchi di stato (Direct3D 9)).
ms.assetid: 30624c0a-e30f-4383-bc0c-b43f42403e72
title: Salvataggio dello stato dei pixel con un StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80741d9f17939d5795163a3e84c58bcdb9003c70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522386"
---
# <a name="saving-pixel-state-with-a-stateblock-direct3d-9"></a>Salvataggio dello stato dei pixel con un StateBlock (Direct3D 9)

Un blocco di stato può essere usato per acquisire solo lo stato del pixel (vedere lo stato di [salvataggio e ripristino di blocchi di stato (Direct3D 9)](state-blocks-save-and-restore-state.md)). Lo stato seguente è stato pixel:

-   Stato di rendering pixel (vedere [pipeline pixel: stato di rendering](#pixel-pipeline-render-state)).
-   Stato trama pixel (vedere [pipeline pixel: stato trama](#pixel-pipeline-texture-state)).
-   Stato campionatore pixel (vedere [pipeline pixel: stato campionatore](#pixel-pipeline-sampler-state)).
-   Pixel shader corrente e ognuna delle costanti pixel shader.

Per acquisire lo stato dei pixel con un blocco di stato, specificare D3DSBT \_ PIXELSTATE quando si chiama [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="pixel-pipeline-render-state"></a>Pipeline pixel: stato di rendering

Gli Stati di rendering del dispositivo influiscono sul comportamento di quasi tutte le parti della pipeline. Gli Stati di rendering vengono impostati chiamando [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

Nella tabella seguente sono inclusi tutti gli Stati di rendering che consentono di impostare lo stato dei pixel:



| Stati di rendering                              | Valore predefinito      |
|--------------------------------------------|--------------------|
| \_ZENABLE D3DRS                             | D3DZB \_ false       |
| \_SPECULARENABLE D3DRS                      | **FALSE**          |
| [**D3DFILLMODE**](./d3dfillmode.md)   | D3DFILL \_ Solid     |
| [**D3DSHADEMODE**](./d3dshademode.md) | \_Gouraud D3DSHADE  |
| \_ZWRITEENABLE D3DRS                        | **TRUE**           |
| \_ALPHATESTENABLE D3DRS                     | **FALSE**          |
| \_LASTPIXEL D3DRS                           | **TRUE**           |
| \_SRCBLEND D3DRS                            | D3DBLEND \_ One      |
| \_DESTBLEND D3DRS                           | D3DBLEND \_ zero     |
| \_ZFUNC D3DRS                               | \_LESSEQUAL D3DCMP  |
| \_ALPHAREF D3DRS                            | 0                  |
| \_ALPHAFUNC D3DRS                           | D3DCMP \_ sempre     |
| \_DITHERENABLE D3DRS                        | **FALSE**          |
| \_FOGSTART D3DRS                            | 0                  |
| \_FOGEND D3DRS                              | 1                  |
| \_FOGDENSITY D3DRS                          | 1                  |
| \_ALPHABLENDENABLE D3DRS                    | **FALSE**          |
| \_DEPTHBIAS D3DRS                           | 0                  |
| \_STENCILENABLE D3DRS                       | **FALSE**          |
| \_STENCILFAIL D3DRS                         | D3DSTENCILOP \_ Keep |
| \_STENCILZFAIL D3DRS                        | D3DSTENCILOP \_ Keep |
| \_STENCILPASS D3DRS                         | D3DSTENCILOP \_ Keep |
| \_STENCILFUNC D3DRS                         | D3DCMP \_ sempre     |
| \_STENCILREF D3DRS                          | 0                  |
| \_STENCILMASK D3DRS                         | 0xFFFFFFFF         |
| \_STENCILWRITEMASK D3DRS                    | 0xFFFFFFFF         |
| \_TEXTUREFACTOR D3DRS                       | 0xFFFFFFFF         |
| \_WRAP0 D3DRS                               | 0                  |
| \_WRAP1 D3DRS                               | 0                  |
| \_WRAP2 D3DRS                               | 0                  |
| \_WRAP3 D3DRS                               | 0                  |
| \_WRAP4 D3DRS                               | 0                  |
| \_WRAP5 D3DRS                               | 0                  |
| \_WRAP6 D3DRS                               | 0                  |
| \_WRAP7 D3DRS                               | 0                  |
| \_WRAP8 D3DRS                               | 0                  |
| \_WRAP9 D3DRS                               | 0                  |
| \_WRAP10 D3DRS                              | 0                  |
| \_WRAP11 D3DRS                              | 0                  |
| \_WRAP12 D3DRS                              | 0                  |
| \_WRAP13 D3DRS                              | 0                  |
| \_WRAP14 D3DRS                              | 0                  |
| \_WRAP15 D3DRS                              | 0                  |
| \_LOCALVIEWER D3DRS                         | **TRUE**           |
| \_EMISSIVEMATERIALSOURCE D3DRS              | \_Materiale D3DMCS   |
| \_AMBIENTMATERIALSOURCE D3DRS               | \_Materiale D3DMCS   |
| \_DIFFUSEMATERIALSOURCE D3DRS               | \_COLOR1 D3DMCS     |
| \_SPECULARMATERIALSOURCE D3DRS              | \_Color2 D3DMCS     |
| \_COLORWRITEENABLE D3DRS                    | 0x0000000f         |
| [**D3DBLENDOP**](./d3dblendop.md)     | D3DBLENDOP \_ aggiungere    |
| \_SCISSORTESTENABLE D3DRS                   | **FALSE**          |
| \_SLOPESCALEDEPTHBIAS D3DRS                 | 0                  |
| \_ANTIALIASEDLINEENABLE D3DRS               | **FALSE**          |
| \_TWOSIDEDSTENCILMODE D3DRS                 | **FALSE**          |
| D3DRS \_ CCW \_ STENCILFAIL                    | D3DSTENCILOP \_ Keep |
| D3DRS \_ CCW \_ STENCILZFAIL                   | D3DSTENCILOP \_ Keep |
| D3DRS \_ CCW \_ STENCILPASS                    | D3DSTENCILOP \_ Keep |
| D3DRS \_ CCW \_ STENCILFUNC                    | D3DCMP \_ sempre     |
| \_COLORWRITEENABLE1 D3DRS                   | 0x0000000f         |
| \_COLORWRITEENABLE2 D3DRS                   | 0x0000000f         |
| \_COLORWRITEENABLE3 D3DRS                   | 0x0000000f         |
| \_BLENDFACTOR D3DRS                         | 0xFFFFFFFF         |
| \_SRGBWRITEENABLE D3DRS                     | 0                  |
| \_SEPARATEALPHABLENDENABLE D3DRS            | **FALSE**          |
| \_SRCBLENDALPHA D3DRS                       | D3DBLEND \_ One      |
| \_DESTBLENDALPHA D3DRS                      | D3DBLEND \_ zero     |
| \_BLENDOPALPHA D3DRS                        | D3DBLENDOP \_ aggiungere    |



 

## <a name="pixel-pipeline-sampler-state"></a>Pipeline pixel: stato campionatore

Gli Stati del campionatore controllano argomenti correlati al campionamento, ad esempio le modalità di filtro, affiancamento e coordinate di trama. Usare [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) per impostare lo stato del campionatore (incluso quello usato nell'unità mosaico per campionare le mappe di spostamento). Gli Stati del campionatore sono stati rinominati con un \_ prefisso "D3DSAMP" per abilitare il rilevamento degli errori in fase di compilazione durante il trasferimento da DirectX 8.

La tabella seguente include tutti gli Stati del campionatore che configurano lo stato dei pixel:



| Stati campionatore         | Valore predefinito     |
|------------------------|-------------------|
| \_Indirizzo D3DSAMP      | D3DTADDRESS a \_ capo |
| \_ADDRESSV D3DSAMP      | D3DTADDRESS a \_ capo |
| \_ADDRESSW D3DSAMP      | D3DTADDRESS a \_ capo |
| \_BorderColor D3DSAMP   | 0x00000000        |
| \_MAGFILTER D3DSAMP     | Punto di D3DTEXF \_    |
| \_MINFILTER D3DSAMP     | Punto di D3DTEXF \_    |
| \_MIPFILTER D3DSAMP     | D3DTEXF \_ None     |
| \_MIPMAPLODBIAS D3DSAMP | 0                 |
| \_MAXMIPLEVEL D3DSAMP   | 0                 |
| \_MAXANISOTROPY D3DSAMP | 1                 |
| \_SRGBTEXTURE D3DSAMP   | 0                 |
| \_ELEMENTINDEX D3DSAMP  | 0                 |



 

## <a name="pixel-pipeline-texture-state"></a>Pipeline pixel: stato trama

Gli Stati della trama controllano le operazioni di blending del Blender a più trame. Usare [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) per impostare gli Stati della fase della trama. Usare [**IDirect3DDevice9:: Setrame**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) per associare una trama a una fase del campionatore.

La tabella seguente include tutti gli Stati di trama che configurano lo stato dei pixel:



| Stati di trama                | Valore predefinito    |
|-------------------------------|------------------|
| \_COLOROP D3DTSS               | \_Disabilitazione D3DTOP  |
| \_COLORARG1 D3DTSS             | \_Trama D3DTA   |
| \_COLORARG2 D3DTSS             | D3DTA \_ corrente   |
| \_ALPHAOP D3DTSS               | \_Disabilitazione D3DTOP  |
| \_ALPHAARG1 D3DTSS             | \_Trama D3DTA   |
| \_ALPHAARG2 D3DTSS             | D3DTA \_ corrente   |
| \_BUMPENVMAT00 D3DTSS          | 0                |
| \_BUMPENVMAT01 D3DTSS          | 0                |
| \_BUMPENVMAT10 D3DTSS          | 0                |
| \_BUMPENVMAT11 D3DTSS          | 0                |
| \_TEXCOORDINDEX D3DTSS         | 0                |
| \_BUMPENVLSCALE D3DTSS         | 0                |
| \_BUMPENVLOFFSET D3DTSS        | 0                |
| \_TEXTURETRANSFORMFLAGS D3DTSS | \_Disabilitazione D3DTTFF |
| \_COLORARG0 D3DTSS             | D3DTA \_ corrente   |
| \_ALPHAARG0 D3DTSS             | D3DTA \_ corrente   |
| \_RESULTARG D3DTSS             | D3DTA \_ corrente   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stato di salvataggio e ripristino del blocco di stato](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 

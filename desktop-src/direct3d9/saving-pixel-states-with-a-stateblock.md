---
description: Un blocco di stato può essere usato per acquisire solo lo stato dei pixel (vedere State Blocks Save and Restore State (Direct3D 9)).
ms.assetid: 30624c0a-e30f-4383-bc0c-b43f42403e72
title: Salvataggio dello stato dei pixel con stateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebc7cc408fe919b1569d51f5cdd4e3e5916968d05b90557a17a22377673fdfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797918"
---
# <a name="saving-pixel-state-with-a-stateblock-direct3d-9"></a>Salvataggio dello stato dei pixel con stateBlock (Direct3D 9)

Un blocco di stato può essere usato per acquisire solo lo stato dei pixel (vedere [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)). Lo stato seguente è lo stato pixel:

-   Stato di rendering pixel (vedere [Pipeline pixel: stato di rendering](#pixel-pipeline-render-state)).
-   Stato trama pixel (vedere [Pipeline pixel: Stato trama](#pixel-pipeline-texture-state)).
-   Stato del campionatore pixel (vedere [Pixel Pipeline: Sampler State).](#pixel-pipeline-sampler-state)
-   L'pixel shader corrente e ognuna delle costanti pixel shader.

Per acquisire lo stato dei pixel con un blocco di stato, specificare D3DSBT PIXELSTATE quando si \_ chiama [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="pixel-pipeline-render-state"></a>Pipeline pixel: stato di rendering

Gli stati di rendering del dispositivo influiscono sul comportamento di quasi tutte le parti della pipeline. Gli stati di rendering vengono impostati chiamando [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

La tabella seguente include tutti gli stati di rendering che configurano lo stato dei pixel:



| Stati di rendering                              | Valore predefinito      |
|--------------------------------------------|--------------------|
| D3DRS \_ ZENABLE                             | D3DZB \_ FALSE       |
| D3DRS \_ SPECULARENABLE                      | **FALSE**          |
| [**D3DFILLMODE**](./d3dfillmode.md)   | D3DFILL \_ SOLID     |
| [**D3DSHADEMODE**](./d3dshademode.md) | D3DSHADE \_ GOURAUD  |
| D3DRS \_ ZWRITEENABLE                        | **TRUE**           |
| D3DRS \_ ALPHATESTENABLE                     | **FALSE**          |
| D3DRS \_ LASTPIXEL                           | **TRUE**           |
| D3DRS \_ SRCBLEND                            | D3DBLEND \_ ONE      |
| D3DRS \_ DESTBLEND                           | D3DBLEND \_ ZERO     |
| D3DRS \_ ZFUNC                               | D3DCMP \_ LESSEQUAL  |
| D3DRS \_ ALPHAREF                            | 0                  |
| D3DRS \_ ALPHAFUNC                           | D3DCMP \_ ALWAYS     |
| D3DRS \_ DITHERENABLE                        | **FALSE**          |
| D3DRS \_ FOGSTART                            | 0                  |
| D3DRS \_ OSANNA                              | 1                  |
| D3DRS \_ OSANNA                          | 1                  |
| D3DRS \_ ALPHABLENDENABLE                    | **FALSE**          |
| D3DRS \_ DEPTHBIAS                           | 0                  |
| D3DRS \_ STENCILENABLE                       | **FALSE**          |
| D3DRS \_ STENCILFAIL                         | D3DSTENCILOP \_ KEEP |
| D3DRS \_ STENCILZFAIL                        | D3DSTENCILOP \_ KEEP |
| D3DRS \_ STENCILPASS                         | D3DSTENCILOP \_ KEEP |
| D3DRS \_ STENCILFUNC                         | D3DCMP \_ ALWAYS     |
| D3DRS \_ STENCILREF                          | 0                  |
| MASCHERA DI STENCIL D3DRS \_                         | 0xffffffff         |
| STENCIL \_ D3DRSWRITEMASK                    | 0xffffffff         |
| D3DRS \_ TEXTUREFACTOR                       | 0xffffffff         |
| D3DRS \_ WRAP0                               | 0                  |
| D3DRS \_ WRAP1                               | 0                  |
| D3DRS \_ WRAP2                               | 0                  |
| WRAP D3DRS3 \_                               | 0                  |
| D3DRS \_ WRAP4                               | 0                  |
| WRAP D3DRS5 \_                               | 0                  |
| WRAP D3DRS6 \_                               | 0                  |
| WRAP D3DRS7 \_                               | 0                  |
| WRAP D3DRS8 \_                               | 0                  |
| WRAP D3DRS9 \_                               | 0                  |
| D3DRS \_ WRAP10                              | 0                  |
| D3DRS \_ WRAP11                              | 0                  |
| D3DRS \_ WRAP12                              | 0                  |
| D3DRS \_ WRAP13                              | 0                  |
| WRAP \_ D3DRS14                              | 0                  |
| D3DRS \_ WRAP15                              | 0                  |
| D3DRS \_ LOCALVIEWER                         | **TRUE**           |
| D3DRS \_ EMISSIVEMATERIALSOURCE              | MATERIALE D3DMCS \_   |
| D3DRS \_ AMBIENTMATERIALSOURCE               | MATERIALE D3DMCS \_   |
| D3DRS \_ DIFFUSEMATERIALSOURCE               | COLORE 1 DI D3DMCS \_     |
| D3DRS \_ SPECULARMATERIALSOURCE              | D3DMCS \_ COLOR2     |
| D3DRS \_ COLORWRITEENABLE                    | 0x0000000f         |
| [**D3DBLENDOP**](./d3dblendop.md)     | D3DBLENDOP \_ ADD    |
| D3DRS \_ SCISSORTESTENABLE                   | **FALSE**          |
| D3DRS \_ SLOPESCALEDEPTHBIAS                 | 0                  |
| D3DRS \_ ANTIALIASEDLINEENABLE               | **FALSE**          |
| D3DRS \_ TWOSIDEDSTENCILMODE                 | **FALSE**          |
| STENCIL \_ CCW D3DRSFAIL \_                    | D3DSTENCILOP \_ KEEP |
| \_STENCIL CCW D3DRSZFAIL \_                   | D3DSTENCILOP \_ KEEP |
| D3DRS \_ CCW \_ STENCILPASS                    | D3DSTENCILOP \_ KEEP |
| D3DRS \_ CCW \_ STENCILFUNC                    | D3DCMP \_ ALWAYS     |
| D3DRS \_ COLORWRITEENABLE1                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE2                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE3                   | 0x0000000f         |
| D3DRS \_ BLENDFACTOR                         | 0xffffffff         |
| D3DRS \_ SRGBWRITEENABLE                     | 0                  |
| D3DRS \_ SEPARATEALPHABLENDENABLE            | **FALSE**          |
| D3DRS \_ SRCBLENDALPHA                       | D3DBLEND \_ ONE      |
| D3DRS \_ DESTBLENDALPHA                      | D3DBLEND \_ ZERO     |
| D3DRS \_ BLENDOPALPHA                        | D3DBLENDOP \_ ADD    |



 

## <a name="pixel-pipeline-sampler-state"></a>Pipeline pixel: stato del campionatore

Gli stati del campionatore controllano gli argomenti correlati al campionamento, ad esempio le modalità di filtro, affiancamento e indirizzo delle coordinate della trama. Usare [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) per configurare lo stato del campionatore(incluso quello usato nell'unità a tessellatore per campionare le mappe di spostamento). Gli stati del campionatore sono stati rinominati con un prefisso "D3DSAMP" per abilitare il rilevamento degli errori in fase di compilazione durante la \_ portabilità da DirectX 8.

La tabella seguente include tutti gli stati del campionatore che configurano lo stato pixel:



| Stati del campionatore         | Valore predefinito     |
|------------------------|-------------------|
| D3DSAMP \_ ADDRESSU      | D3DTADDRESS \_ WRAP |
| D3DSAMP \_ ADDRESSV      | D3DTADDRESS \_ WRAP |
| D3DSAMP \_ ADDRESSW      | D3DTADDRESS \_ WRAP |
| D3DSAMP \_ BORDERCOLOR   | 0x00000000        |
| D3DSAMP \_ MAGFILTER     | PUNTO D3DTEXF \_    |
| D3DSAMP \_ MINFILTER     | PUNTO D3DTEXF \_    |
| D3DSAMP \_ MIPFILTER     | D3DTEXF \_ NONE     |
| D3DSAMP \_ MIPMAPLODBIAS | 0                 |
| D3DSAMP \_ MAXMIPLEVEL   | 0                 |
| D3DSAMP \_ MAXANISOTROPY | 1                 |
| D3DSAMP \_ SRGBTEXTURE   | 0                 |
| ELEMENTO D3DSAMPINDEX \_  | 0                 |



 

## <a name="pixel-pipeline-texture-state"></a>Pipeline pixel: stato della trama

Gli stati della trama controllano le operazioni di fusione della trama del blender a più trame. Usare [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) per configurare gli stati della fase della trama. Usare [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) per associare una trama a una fase del campionatore.

La tabella seguente include tutti gli stati di trama che configurano lo stato dei pixel:



| Stati della trama                | Valore predefinito    |
|-------------------------------|------------------|
| D3DTSS \_ COLOROP               | D3DTOP \_ DISABLE  |
| D3DTSS \_ COLORARG1             | TRAMA D3DTA \_   |
| D3DTSS \_ COLORARG2             | D3DTA \_ CURRENT   |
| D3DTSS \_ ALPHAOP               | D3DTOP \_ DISABLE  |
| D3DTSS \_ ALPHAARG1             | TRAMA D3DTA \_   |
| D3DTSS \_ ALPHAARG2             | D3DTA \_ CURRENT   |
| D3DTSS \_ BUMPENVMAT00          | 0                |
| D3DTSS \_ BUMPENVMAT01          | 0                |
| D3DTSS \_ BUMPENVMAT10          | 0                |
| D3DTSS \_ BUMPENVMAT11          | 0                |
| D3DTSS \_ TEXCOORDINDEX         | 0                |
| D3DTSS \_ BUMPENVLSCALE         | 0                |
| D3DTSS \_ BUMPENVLOFFSET        | 0                |
| D3DTSS \_ TEXTURETRANSFORMFLAGS | D3DTTFF \_ DISABLE |
| D3DTSS \_ COLORARG0             | D3DTA \_ CURRENT   |
| D3DTSS \_ ALPHAARG0             | D3DTA \_ CURRENT   |
| D3DTSS \_ RESULTARG             | D3DTA \_ CURRENT   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[State Blocks Save and Restore State](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
